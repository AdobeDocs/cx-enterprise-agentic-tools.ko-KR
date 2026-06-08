---
title: 성능 데이터를 기반으로 콘텐츠 최적화
description: CJA 및 AEM MCP 서버를 함께 사용하여 도구 간에 전환하지 않고도 성과가 낮은 콘텐츠를 식별하고 업데이트합니다.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 3%

---


# 성능 데이터를 기반으로 콘텐츠 최적화

<!-- last-modified: 2026-05-21 -->

![성능 데이터를 기반으로 콘텐츠 최적화](https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data)

컨텐츠 성능 데이터와 컨텐츠 업데이트 간의 루프를 닫는다는 것은 일반적으로 analytics와 CMS 간에 전환하는 것을 의미합니다. 이 연습에서는 동일한 AI 세션에서 Customer Journey Analytics과 AEM을 연결하여 성과가 낮은 페이지를 표시하고 대화를 종료하지 않고 업데이트하는 방법을 보여줍니다.

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

## 1단계: 성과가 낮은 콘텐츠 식별

CX 엔터프라이즈 MCP 게이트웨이를 사용하여 Customer Journey Analytics의 참여 및 전환 지표에 따라 페이지 등급을 매깁니다. 목표는 주의가 필요한 명확하고 우선 순위가 지정된 콘텐츠 목록입니다.

```
Show me the 10 pages with the lowest engagement rate over the last 60 days.
```

+++예제 응답 보기

최하위 참여 페이지(2026년 3월 22일 - 5월 21일):

| 순위 | 페이지 | 참여율 | 바운스 비율 | 평균 페이지에서 시간 |
| --- | --- | --- | --- | --- |
| 1 | /en/products/analytics | 8.2% | 74% | 0:42 |
| 2 | /en/resources/whitepapers | 9.1% | 71% | 0:38 |
| 3 | /en/solutions/retail | 10.4% | 69% | 0:51 |
| 4 | /en/blog/2025-q4-recapp | 11.0% | 68% | 0:44 |
| 5-10 | ... | 12.3-14.1% | 63-67% | 0:35-1:10 |

사이트 평균 참여율은 34.7%입니다. 이 페이지는 평균보다 2~4배 낮습니다.

+++

## 2단계: AEM에서 컨텐츠 검토

AI 세션을 종료하지 않고 AEM에서 해당 페이지의 현재 상태를 가져옵니다. 내용이 말하는 것을 이해하는 것은 무엇을 변화시켜야 하는지를 아는 첫 단계이다.

```
Show me the current content on the /en/products/analytics page in AEM.
```

+++예제 응답 보기

**페이지:** `/en/products/analytics`
**마지막 수정 날짜:** T. MacMillan의 2026년 4월 30일
**상태:** 게시됨

**영웅 섹션:**
Headline: &quot;모든 팀을 위한 데이터 기반 결정&quot;
서브헤드라인: &quot;Adobe Analytics은 조직에 적용할 수 있는 통찰력을 제공합니다.&quot;
CTA: &quot;데모 요청&quot; → /contact/demo

**본문:** 3개의 기능 블록 뒤에 고객 로고 스트립과 보조 CTA이 옵니다. 비디오 또는 대화형 요소가 없습니다. 페이지가 21일 동안 업데이트되지 않았습니다.

**Meta 설명:** &quot;Adobe Analytics: 엔터프라이즈 팀을 위한 실시간 보고 및 AI 인사이트&quot;

+++

## 3단계: 타깃팅된 업데이트

성능 데이터와 현재 콘텐츠를 보고 데이터가 공개한 내용에 기반을 둔 업데이트를 수행합니다.

```
Update the hero headline on the analytics product page to Make faster decisions with AI-powered analytics.
```

+++예제 응답 보기

**제안된 변경 내용:**

| 필드 | 현재 값 | 새 값 |
| --- | --- | --- |
| 영웅 제목 | 모든 팀을 위한 데이터 기반 의사 결정 | AI 기반 분석으로 더 빠른 의사 결정 |

페이지: `/en/products/analytics`

이 변경 사항을 확인하시겠습니까? &quot;예&quot;라고 답장을 보내면 AEM에 업데이트가 기록됩니다. 페이지는 명시적으로 다시 게시할 때까지 현재 상태로 게시된 상태로 유지됩니다.

+++

>[!CAUTION]
>
>메시지가 표시되면 각 콘텐츠 변경을 확인합니다. 라이브 페이지에 대한 업데이트를 승인하기 전에 전체 차이를 검토하십시오.

## 4단계: 유효성 검사 및 게시

업데이트에 만족하면 모든 변경 사항을 확인하고 콘텐츠를 프로모션하여 루프를 닫습니다.

```
Show me a summary of all changes made in this session.
```

+++예제 응답 보기

**세션 요약 — 2026년 5월 21일:**

| 페이지 | 변경 | 상태 |
| --- | --- | --- |
| /en/products/analytics | 영웅 헤드라인 업데이트됨 | 저장됨, 게시 취소됨 |

1페이지가 업데이트되었습니다. 확인되면 게시할 준비가 되었습니다.

**낮은 참여 목록에서 남은 항목:** 9페이지가 이 세션에서 업데이트되지 않았습니다. 다음 페이지로 계속 진행하시겠습니까? 아니면 게시하기 전에 일괄 검토를 위해 론치를 만드시겠습니까?

+++

## 수행한 작업

단일 AI 세션에서 Customer Journey Analytics 및 AEM을 연결하고 성능 데이터를 사용하여 콘텐츠 변경 사항을 직접 알렸습니다. 도구를 전환하지 않고 지표에서 업데이트로 이동하여 analytics insight과 게시된 콘텐츠 간의 피드백 루프를 단축했습니다. 이는 수십 페이지에 달하는 주의가 필요하고 수동 교차 도구 워크플로우가 지연을 만들 수 있는 캠페인 규모에서 가장 중요합니다.

## 수행할 수 있는 작업 더 보기

CJA 및 AEM MCP 서버는 문제 식별부터 배송 수정 사항까지의 전체 주기를 함께 지원합니다. 동일한 세션에서 시도할 수 있는 프롬프트를 보려면 아래 시나리오를 확장하십시오.

+++성능을 저해하는 콘텐츠 찾기

참여도가 낮은 트래픽이 많으면 트래픽 문제가 아닌 콘텐츠 문제를 알리는 신호입니다. 이러한 프롬프트는 캠페인 마감에 따라 문제가 발생하기 전에 주의가 필요한 특정 페이지 및 패턴을 표시하는 데 도움이 됩니다.

**프롬프트**

```
Show me the 10 pages with the lowest conversion rate this quarter.
```

```
Which pages have a high bounce rate but also high traffic?
```

```
Compare engagement rates for blog posts versus product pages.
```

```
Find AEM pages that haven't been updated in over 60 days.
```

+++

+++데이터가 수정하라고 지시하는 사항 수정

성과가 낮은 항목을 알게 되면 다음 단계에서 타깃팅된 변경을 수행합니다. 이러한 프롬프트를 통해 성능 데이터가 공개한 내용을 기반으로 헤드라인, CTA 및 메타 설명을 업데이트할 수 있습니다.

**프롬프트**

```
Update the CTA on the /en/solutions/retail page to 'See how it works'.
```

```
Add a note to the hero subheadline on the analytics page: Now with AI-powered anomaly detection.
```

```
Update the meta description on all pages in /en/products/ that contain the word 'legacy'.
```

```
Which pages updated in this session still need their CTAs reviewed?
```

+++

+++다음 캠페인 전에 개선 사항 발송

세션 중간에 변경한 사항이 신속하게 쌓일 수 있습니다. 이러한 프롬프트는 준비된 항목을 검토하고, 볼 수 있는 론치로 그룹 업데이트를 검토하고, 캠페인이 라이브로 전환되기 전에 완전히 홍보하는 데 도움이 됩니다.

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
Promote everything in the current launch to production.
```

+++

## 추가 정보

| 리소스 | 찾을 내용 |
| --- | --- |
| [Analytics MCP 설명서](https://developer.adobe.com/analytics-mcp/docs/) | CJA MCP 설정 및 도구 참조 |
| [AEM as a Cloud Service 설명서](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service) | 전체 AEM 설명서 |
| [AI 레지스트리의 CJA MCP 서버](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | CJA MCP 서버 도구 및 가용성 |
| [AI 레지스트리의 AEM Content MCP 서버](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) | AEM Content MCP 서버 도구 및 가용성 |
| [MCP 서버](../tools/mcp-servers.md) | AI 클라이언트를 Adobe MCP 서버에 연결 |
