---
title: 크로스 채널 캠페인 검토 실행
description: 단일 AI 세션에서 CX 엔터프라이즈 MCP 게이트웨이를 사용하면 여정, 대상 및 성능 전반에 걸쳐 AJO, CJA 및 Real-Time CDP 캠페인 상태를 전체적으로 확인할 수 있습니다.
index: false
source-git-commit: 14488b494c454ce6d1207e2d21024749d93db669
workflow-type: tm+mt
source-wordcount: '1433'
ht-degree: 4%

---


# 크로스 채널 캠페인 검토 실행

<!-- last-modified: 2026-05-21 -->

![크로스 채널 캠페인 검토 실행](https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review)

캠페인 상태에 대한 전체 그림에는 AJO의 활성 여정, Real-Time CDP의 대상 활성화 상태 및 CJA의 성능 지표와 같은 여러 시스템의 데이터가 필요합니다. 이 연습에서는 세 가지 를 단일 AI 세션에서 모두 연결하는 방법을 보여 주기 때문에 세 가지 개별 도구가 아닌 한 대화에서 여정 상태에서 대상 상태로 전환하고 성능 트렌드를 볼 수 있습니다.

| | |
| --- | --- |
| CX 엔터프라이즈 애플리케이션 | Adobe Journey Optimizer, Customer Journey Analytics, Real-Time CDP |
| 무생식 도구 | CX 엔터프라이즈 MCP 게이트웨이 |
| 대상자 | 캠페인 관리자, 마케팅 운영 |
| 사전 요구 사항 | MCP 호환 AI 클라이언트, AJO, CJA 및 Real-Time CDP 액세스 |

각 단계에는 하나의 대표적인 프롬프트와 예제 AI 응답이 표시됩니다. 같은 세션에서 추가 탐색을 위해 **수행할 수 있는 추가** 섹션이 다음과 같습니다.

## 시작하기에 앞서

>[!BEGINTABS]

>[!TAB 클라우드.ai]

CX 엔터프라이즈 MCP 게이트웨이를 사용자 지정 커넥터로 연결합니다. 하나의 연결을 통해 AJO, CJA 및 Real-Time CDP 도구에 액세스할 수 있습니다.

1. Cloud.ai의 **설정 > 통합**(으)로 이동합니다.
2. **사용자 지정 커넥터 추가**&#x200B;를 선택하고 서버 URL을 입력하십시오. `https://cx-enterprise.adobe.io/mcp`
3. **연결**&#x200B;을 선택하고 Adobe ID으로 로그인하세요.

전체 설정: [Claude.ai 사용자 지정 커넥터 설명서](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

ChatGPT 개발자 모드(Pro, Plus, 비즈니스, 엔터프라이즈 또는 교육 계획 필요)를 사용하여 CX 엔터프라이즈 MCP 게이트웨이를 연결합니다.

1. **ChatGPT 설정**&#x200B;에서 **개발자 모드**&#x200B;를 사용하도록 설정합니다.
2. **설정 > 통합**(으)로 이동하여 **사용자 지정 커넥터 추가 > 원격 MCP 서버**&#x200B;를 선택합니다.
3. 서버 URL 입력: `https://cx-enterprise.adobe.io/mcp`
4. **연결**&#x200B;을 선택하고 Adobe ID으로 로그인하세요.

전체 설정: [ChatGPT MCP 설명서](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB 기타 AI 클라이언트]

Gemini, Microsoft Copilot, Cursor, Claude Code 또는 다른 MCP 호환 환경을 사용하시겠습니까? 다음 끝점을 사용하여 CX 엔터프라이즈 MCP 게이트웨이에 연결합니다.

```
https://cx-enterprise.adobe.io/mcp
```

지원되는 모든 클라이언트에 대한 전체 설치 지침: [AI 클라이언트에 연결](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>메시지가 표시되면 Adobe ID으로 로그인하고 AJO, CJA 및 Real-Time CDP 환경에 연결된 IMS 조직을 선택합니다. 잘못된 조직을 선택하는 것이 인증 오류의 가장 일반적인 원인입니다.
>
>첫 번째 연결 시 AI 클라이언트가 IMS 조직을 선택하거나 샌드박스를 지정하도록 요청할 수 있습니다. 컨텍스트가 설정되면 MCP 서버는 세션의 나머지 부분에 컨텍스트를 사용합니다.
>
>일부 도구는 실행 전에 승인을 묻는 메시지를 표시합니다. 요청을 검토하고 승인 또는 거절합니다. 확인 없이는 아무 작업도 수행되지 않습니다.

## 1단계: 활성 여정 및 캠페인 검토

AJO으로 시작하여 현재 실행 중인 항목을 설정합니다. 어떤 여정이 라이브이고 최근에 수정되었는지 알면 나머지 검토에 필요한 기반을 제공할 수 있습니다.

```
What journeys are currently active in AJO?
```

+++예제 응답 보기

AJO 조직에서 8개의 활성 여정을 찾았습니다.

| 여정 | 채널 | 마지막 수정일 |
| --- | --- | --- |
| 시작 시리즈 - 새 멤버 | 이메일, 푸시 | 2026년 5월 18일 |
| 구매 후 후속 작업 | 이메일, SMS | 2026년 5월 14일 |
| 충성도 재참여 | 이메일 | 2026년 5월 20일 |
| 포기한 장바구니 — 24시간 | 이메일, SMS | 2026년 5월 10일 |
| 봄 프로모션 | 이메일, 푸시 | 2026년 5월 19일 |
| Win-Back — 90일 비활성 | 이메일 | 2026년 4월 28일 |
| 생일 보상 | 이메일 | 2026년 4월 15일 |
| 재참여 — 푸시 옵트아웃 | SMS | 2026년 5월 12일 |

지난 7일 동안 3개의 여정이 수정되었습니다. 이 중 하나라도 자세히 알고 싶으신가요?

+++


## 2단계: 대상 활성화 상태 확인

여정을 볼 때 해당 캠페인을 지원하는 대상이 대상으로 올바르게 이동하는지 확인하십시오.

```
Show me the activation status for the high-value loyalty segment.
```

+++예제 응답 보기

**높은 값 충성도 세그먼트** — 대상 간 활성화 상태:

| 대상 | 상태 | 마지막으로 성공한 실행 | 대상자 크기 |
| --- | --- | --- | --- |
| Google Ads | 활성 | 2026년 5월 21일 오전 02:14 | 48,320 |
| Meta 광고 | 활성 | 2026년 5월 21일 오전 01:58 | 48,295 |
| Salesforce Marketing Cloud | 활성 | 2026년 5월 20일 오후 11:30 | 47,940 |
| Adobe Target | 활성 | 2026년 5월 21일 오전 12:00 | 48,320 |

감지된 데이터 흐름 오류가 없습니다. 지난 3시간 내에 모든 활성화가 완료되었습니다.

+++


## 3단계: CJA에서 성능 지표 가져오기

여정 및 대상 컨텍스트를 설정한 상태에서 CJA을 사용하여 이러한 캠페인이 전환하는 방식과 참여 감소 위치를 평가합니다.

```
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
```

+++예제 응답 보기

**충성도 재참여 캠페인** — 2026년 4월 21일부터 5월 21일까지:

| 채널 | 전송 횟수 | CTR | 전환 | 콘브 속도 |
| --- | --- | --- | --- | --- |
| 이메일 | 48,320 | 8.4% | 1,973 | 4.1% |
| 푸시 | 31,200 | 12.1% | 987 | 3.2% |

통합 전환율: 3.8%. 이메일 CTR은 이전 30일 기간에 비해 1.2% 증가했습니다. 푸시 전환은 균일합니다.

+++


## 4단계: 캠페인 상태 요약 합성

AI 클라이언트에게 세 가지 소스 모두에서 그림을 가져오도록 요청하고 주의가 필요한 모든 것을 표시하십시오.

```
Give me a summary of our campaign health: what is running, which audiences are activated, and how performance looks against last month.
```

+++예제 응답 보기

다음은 AJO, Real-Time CDP 및 CJA의 현재 캠페인 상태 요약입니다.

**활성 여정:** 8개, 이번 주 수정됨. 충성도 재참여 여정이 가장 최근에 업데이트되었습니다.

**대상자 활성화:** 모든 세그먼트가 4개의 대상으로 올바르게 흐릅니다. 감지된 데이터 흐름 오류가 없습니다.

**성능:** 이메일 CTR이 충성도 캠페인에서 작동합니다. 푸시 전환이 균일합니다. 어떤 채널도 크게 감소하지 않고 있습니다.

**주의 플래그:**

- Win-Back 여정(90일 비활성)는 23일 전에 마지막으로 수정되었으며 최근에 검토되지 않았습니다.
- 푸시 전환율은 3회 연속 균일했습니다. 메시징이나 타이밍을 검토할 가치가 있습니다.

감지된 심각한 문제가 없습니다. 다음 선거 운동 시작 전에 영장실질심사에서 두 가지 항목.

+++


이 경우 다중 서버 접근 방식이 효과를 발휘합니다. 즉, 단일 대화에서 여정 구성, 대상 상태 및 성능 데이터에 대한 AI 클라이언트 사유가 됩니다.

## 5단계: 찾은 항목 실행

리뷰에는 두 가지 항목이 표시되었습니다. AI 클라이언트에게 각 항목에 대한 우선 순위 지정 및 라우팅을 지원하도록 요청합니다.

```
For each flag you identified, what should I do and where should I go to do it?
```

+++예제 응답 보기

다음은 두 플래그에 대한 우선 순위 작업 계획입니다.

**1. 다시 시작 여정 — 다시 시작 조건 검토(AJO MCP, 변경 사항이 필요한 경우 AJO 애플리케이션)**

윈-백 여정이 23일 동안 수정되지 않았습니다. 현재 재진입 조건과 종료 논리를 살펴보도록 요청하십시오. 조건이 진부하거나 잘못된 것 같은 경우 여정 흐름을 구조적으로 변경하려면 AJO을 열어야 합니다. 여기에서 빈도 제한 및 대상 업데이트를 수행할 수 있습니다.

**2. 3개 기간 동안 푸시 전환 플랫 — 메시지 업데이트 또는 변형 테스트**

플랫 변환은 일반적으로 오퍼와 대상자 간의 메시지 피로도 또는 불일치를 나타냅니다. 두 개의 경로:

- **지금 푸시 콘텐츠 업데이트(AEM MCP):** 푸시 알림이 랜딩 페이지에 연결되는 경우 AEM Content MCP 서버를 추가하고 도구를 전환하지 않고 페이지 사본 또는 CTA을 업데이트합니다.
- **푸시 A/B 테스트 실행(AJO 애플리케이션):** 다른 메시징을 사용하여 캠페인 수준 변형을 만들어 콘텐츠인지 아니면 타깃팅인지를 구분합니다. 이렇게 하려면 AJO으로 직접 이동해야 합니다.

어떤 것부터 시작하시겠습니까?

+++


## 수행한 작업

AJO, Real-Time CDP 및 CJA을 단일 AI 세션에 연결하여 크로스 채널 캠페인 상태 검토를 실행했습니다. 세 개의 애플리케이션을 열고 사진을 수동으로 조립하는 대신 한 번의 대화에서 여정 상태, 대상자 활성화 및 성능 데이터를 이동했습니다. 합성된 요약은 캠페인 관리자가 작동 중인 항목, 조정이 필요한 항목 및 다음에 집중할 위치를 식별하는 빠른 경로를 제공합니다.

## 수행할 수 있는 작업 더 보기

AJO, CJA 및 Real-Time CDP을 동일한 세션에서 연결하면 연습 이상의 작업을 수행할 수 있습니다. 시도할 수 있는 프롬프트를 보려면 아래 시나리오를 확장하십시오.

+++새로운 기능을 실행하기 전에 정확히 실행 중인 작업 파악

겹치는 여정, 최근에 수정한 캠페인 및 검토하지 않은 채널이 모두 새 론치에 영향을 줄 수 있습니다. 이러한 프롬프트는 추가하기 전에 현재 상태를 명확하게 파악할 수 있도록 해줍니다.

**프롬프트**

```
Which journey has the most active profiles right now?
```

```
Show me all journeys modified in the last 7 days.
```

```
Which campaigns are scheduled to end this week?
```

```
Are any journeys targeting the same segment as the campaign I'm about to launch?
```

+++

+++대상이 올바른 대상에 도달하고 있는지 확인합니다.

활성화 문제는 침묵합니다. 세그먼트 흐름이 중지되고 캠페인이 경고 없이 더 작은 목록으로 전송됩니다. 이러한 프롬프트는 결과에 영향을 미치기 전에 간격과 오류를 표시합니다.

**프롬프트**

```
Which audiences have grown the most in the last 30 days?
```

```
Are there any dataflow errors across my active destinations?
```

```
How many records were exported to each destination in the last 7 days?
```

```
Are there any audiences with no active destinations?
```

+++

+++작동 중인 내용과 다음에 집중해야 할 위치를 파악합니다.

채널 전반의 성능 트렌드는 어디에 투자하고 어떤 것을 철회해야 하는지를 알려줍니다. 이러한 프롬프트는 결과를 유도하는 내용과 다음 분기의 주의가 필요한 위치를 식별하는 데 도움이 됩니다.

**프롬프트**

```
Show me email performance trends for the last 90 days.
```

```
Which campaigns are underperforming against their conversion targets?
```

```
What is the average revenue per conversion this month compared to last month?
```

```
Which channel has the highest conversion rate across all active campaigns?
```

+++


## 추가 정보

| 리소스 | 찾을 내용 |
| --- | --- |
| [AJO 설명서](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/ajo-home) | 전체 AJO 애플리케이션 설명서 |
| [Analytics MCP 설명서](https://developer.adobe.com/analytics-mcp/docs/) | CJA MCP 설정 및 도구 참조 |
| [Real-Time CDP MCP 설명서](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) | RTCDP MCP 설치 안내서 |
| [AI 레지스트리의 AJO MCP 서버](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) | AJO MCP 서버 도구 및 가용성 |
| [AI 레지스트리의 CJA MCP 서버](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | CJA MCP 서버 도구 및 가용성 |
| [MCP 서버](../tools/mcp-servers.md) | AI 클라이언트를 Adobe MCP 서버에 연결 |
