---
title: 성능 데이터를 기반으로 콘텐츠 최적화
description: 하나의 AI 세션에서 CJA과 AEM을 함께 사용하면 도구를 전환하지 않고도 전환되지 않는 캠페인을 찾고 원인을 진단하고 콘텐츠를 업데이트할 수 있습니다.
last-substantial-update: 2026-06-08T00:00:00Z
index: false
source-git-commit: 093448ea6a9840d1d2027b76e177b145400a9202
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 1%

---


# 성능 데이터를 기반으로 콘텐츠 최적화
<!-- last-modified: 2026-06-08 -->

![성능 데이터를 기반으로 콘텐츠 최적화](https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data)

캠페인 성과 데이터와 콘텐츠 업데이트 간의 루프를 닫는다는 것은 일반적으로 분석 도구와 CMS 간에 전환하는 것을 의미합니다. 이 연습에서는 동일한 AI 세션에서 Customer Journey Analytics과 AEM을 연결하는 방법을 보여 줍니다. 즉, 전환에 차이가 있는 캠페인을 표시하고, 이러한 캠페인을 유발하는 요소를 진단하고, 콘텐츠를 검사하고, 타깃팅된 추천을 받고, 대화를 종료하지 않고 변경 사항을 적용하는 것입니다.

| | |
| --- | --- |
| CX 엔터프라이즈 애플리케이션 | Customer Journey Analytics, Adobe Experience Manager as a Cloud Service |
| 무생식 도구 | CX 엔터프라이즈 MCP 게이트웨이, AEM Content MCP 서버 |
| 대상자 | 캠페인 관리자, 콘텐츠 전략가, 마케팅 운영 |
| 사전 요구 사항 | MCP 호환 AI 클라이언트, CJA 액세스, AEM as a Cloud Service 액세스 |

각 단계에는 하나의 대표적인 프롬프트와 예제 AI 응답이 표시됩니다. 같은 세션에서 추가 탐색을 위해 **수행할 수 있는 추가** 섹션이 다음과 같습니다.


## 시작하기에 앞서

>[!BEGINTABS]

>[!TAB 클라우드.ai]

두 MCP 서버를 사용자 지정 커넥터로 연결합니다. 각각 하나씩 추가합니다.

1. Cloud.ai의 **설정 > 통합**(으)로 이동합니다.
2. **사용자 지정 커넥터 추가**&#x200B;를 선택하고 서버 URL을 입력한 다음 **연결**&#x200B;을 선택합니다.
3. Adobe ID으로 로그인한 다음, 두 번째 서버에 대해 이 과정을 반복합니다.

| 서버 | 엔드포인트 |
| --- | --- |
| CX 엔터프라이즈 MCP 게이트웨이 | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP 서버 | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

전체 설정: [Claude.ai 사용자 지정 커넥터 설명서](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

ChatGPT 개발자 모드(Pro, Plus, 비즈니스, 엔터프라이즈 또는 교육 계획 필요)를 사용하여 두 MCP 서버를 연결합니다. 각 서버를 별도로 추가합니다.

1. **ChatGPT 설정**&#x200B;에서 **개발자 모드**&#x200B;를 사용하도록 설정합니다.
2. **설정 > 통합**(으)로 이동하여 **사용자 지정 커넥터 추가 > 원격 MCP 서버**&#x200B;를 선택합니다.
3. 서버 URL을 입력하고 **연결**&#x200B;을 선택한 다음 Adobe ID으로 로그인하세요.
4. 두 번째 서버에 대해 이 작업을 반복합니다.

| 서버 | 엔드포인트 |
| --- | --- |
| CX 엔터프라이즈 MCP 게이트웨이 | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP 서버 | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

전체 설정: [ChatGPT MCP 설명서](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB 기타 AI 클라이언트]

Gemini, Microsoft Copilot, Cursor, Claude Code 또는 다른 MCP 호환 환경을 사용하시겠습니까? 다음 끝점을 사용하여 두 MCP 서버에 연결합니다.

| 서버 | 엔드포인트 |
| --- | --- |
| CX 엔터프라이즈 MCP 게이트웨이 | `https://cx-enterprise.adobe.io/mcp` |
| AEM Content MCP 서버 | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

지원되는 모든 클라이언트에 대한 전체 설치 지침: [AI 클라이언트에 연결](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>메시지가 표시되면 Adobe ID으로 로그인하고 CJA 및 AEM 환경에 연결된 IMS 조직을 선택합니다. 잘못된 조직을 선택하는 것이 인증 오류의 가장 일반적인 원인입니다.
>
>첫 번째 연결 시 AI 클라이언트가 IMS 조직을 선택하거나 샌드박스를 지정하도록 요청할 수 있습니다. 컨텍스트가 설정되면 MCP 서버는 세션의 나머지 부분에 컨텍스트를 사용합니다.
>
>일부 도구는 실행 전에 승인을 묻는 메시지를 표시합니다. 요청을 검토하고 승인 또는 거절합니다. 확인 없이는 아무 작업도 수행되지 않습니다.


## 1단계: 전환 간격이 있는 캠페인 찾기

CJA을 사용하여 클릭스루는 강하지만 전환율이 낮은 캠페인을 표시합니다. 이 패턴(높은 의도의 낮은 완료)은 일반적으로 랜딩 페이지의 콘텐츠 또는 경험 문제를 가리킵니다.

```
Which campaigns have strong click-through but low conversion in the last 30 days?
```

+++예제 응답 보기

![CJA에서 클릭스루가 높지만 전환율이 낮은 AI 클라이언트 표시 캠페인](../assets/use-cases/optimize-content-with-performance-data/optimize-content-step1-campaigns.png)

+++



## 2단계: 근본 원인 진단

차이를 유발하는 것이 무엇인지 이해하기 위해 후속 작업을 수행하십시오. 드롭오프가 특정 장치 유형, 대상 세그먼트 또는 컨텐츠 상호 작용에 집중되는지 묻습니다.

```
What's causing the conversion drop-off, is it device, segment, or content?
```

+++예제 응답 보기

![AI 클라이언트가 장치, 세그먼트 및 콘텐츠 인자별로 전환 드롭오프를 진단](../assets/use-cases/optimize-content-with-performance-data/optimize-content-step2-diagnosis.png)

+++



## 3단계: AEM에서 컨텐츠 검토

성과가 낮은 캠페인이 식별되면 동일한 세션에서 AEM에서 랜딩 페이지를 가져옵니다. 페이지에 현재 나와 있는 내용을 확인하는 것은 변경할 내용을 이해하는 시작점입니다.

```
Show me the Bali Surf Camp page.
```

+++예제 응답 보기

![AEM에서 랜딩 페이지의 현재 콘텐츠를 표시하는 AI 클라이언트](../assets/use-cases/optimize-content-with-performance-data/optimize-content-step3-page-content.png)

+++



## 4단계: 타깃팅된 권장 사항 가져오기

데이터에 표시된 내용을 페이지의 내용과 연결하도록 AI 클라이언트에 요청합니다. 두 소스 모두에서 AI가 드롭오프의 원인이 될 수 있는 콘텐츠 섹션과 변경할 콘텐츠를 식별하는 이유입니다.

```
Which content sections are underperforming, and what changes would you recommend?
```

+++예제 응답 보기

![성과가 낮은 콘텐츠 섹션을 식별하고 특정 변경 사항을 추천하는 AI 클라이언트](../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step4.gif)

+++



## 5단계: 변경 사항 적용 및 검토

AI 클라이언트에게 권장 사항을 기반으로 최적화된 페이지 버전을 제작하도록 요청하고 변경된 사항과 이유를 요약합니다.

```
Create an optimized version of the Bali Surf Camp page and summarize the proposed changes.
```

+++예제 응답 보기

![AI 클라이언트가 페이지의 최적화된 버전을 만들고 변경 내용을 요약](../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5.gif)

+++


>[!CAUTION]
>
>확인하기 전에 제안된 변경 사항의 전체 요약을 검토하십시오. AEM Content MCP 서버는 AEM 환경에 변경 사항을 기록합니다. 페이지는 명시적으로 다시 게시할 때까지 게시된 상태로 유지됩니다.


## 수행한 작업

단일 AI 세션에서 Customer Journey Analytics과 AEM을 연결하고 도구를 전환하지 않고 캠페인 데이터에서 배포된 콘텐츠 변경 사항으로 이동했습니다. 전환 간격이 있는 캠페인을 식별하고, 근본 원인을 진단하고, 랜딩 페이지를 검사하고, 데이터와 콘텐츠 모두에 기반을 둔 타겟팅 권장 사항을 수신하고, 동일한 대화에서 변경 사항을 적용했습니다. 이렇게 하면 analytics insight과 게시된 콘텐츠 간의 피드백 루프가 짧아지고, 동일한 세션에서 성과가 낮은 페이지 수로 확장됩니다.


## 수행할 수 있는 작업 더 보기

CJA과 AEM이 동일한 세션에 연결되어 있으므로 문제 식별부터 배송 수정 사항까지의 전체 주기를 처리할 수 있습니다. 시도할 수 있는 프롬프트를 보려면 아래 시나리오를 확장하십시오.

+++성능을 저해하는 콘텐츠 찾기

참여도가 낮은 트래픽이 많으면 트래픽 문제가 아닌 콘텐츠 문제를 알리는 신호입니다. 이러한 프롬프트는 캠페인 마감에 따라 문제가 발생하기 전에 주의가 필요한 특정 페이지 및 패턴을 표시하는 데 도움이 됩니다.

**프롬프트**

```
Which campaigns have the highest traffic but lowest conversion rate this quarter?
```

```
Which pages have a high bounce rate but also high traffic?
```

```
Compare engagement rates for landing pages across email and paid social campaigns.
```

```
Find AEM pages linked from active campaigns that haven't been updated in over 60 days.
```

+++

+++데이터가 수정하라고 지시하는 사항 수정

성과가 낮은 항목을 알게 되면 성능 데이터가 공개한 내용에 따라 타겟팅된 변경을 수행합니다. 이러한 프롬프트를 통해 진단에 따라 특정 섹션을 업데이트할 수 있습니다.

**프롬프트**

```
Update the CTA on the [page name] page to better match the campaign audience.
```

```
Rewrite the hero headline on the [page name] page to address the mobile drop-off.
```

```
Add a trust signal to the [page name] page above the conversion form.
```

```
Which pages updated in this session still need to be published?
```

+++

+++다음 캠페인 전에 개선 사항 발송

세션 중간에 변경한 사항이 신속하게 쌓일 수 있습니다. 이러한 프롬프트는 준비된 항목을 검토하고, 검토를 위해 그룹 업데이트를 검토하고, 캠페인이 라이브로 전환되기 전에 깔끔하게 프로모션하는 데 도움이 됩니다.

**프롬프트**

```
Show me all pages updated in this session that are still unpublished.
```

```
Create a launch with all changes from this session for review before publishing.
```

```
Give me a summary of all changes made in this session.
```

```
Publish all confirmed changes and share the updated URLs.
```

+++



## 추가 정보

| 리소스 | 찾을 내용 |
| --- | --- |
| [CJA MCP 서버 설명서](https://developer.adobe.com/analytics-mcp/docs/cja/) | CJA MCP 설정 및 도구 참조 |
| [AEM Content MCP 서버 설명서](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | AEM Content MCP 설치 및 사용 안내서 |
| [AI 레지스트리의 CJA MCP 서버](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | CJA MCP 서버 도구 및 가용성 |
| [AI 레지스트리의 AEM Content MCP 서버](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) | AEM Content MCP 서버 도구 및 가용성 |
| [MCP 서버](../tools/mcp-servers.md) | AI 클라이언트를 Adobe MCP 서버에 연결 |
