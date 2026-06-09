---
title: 대상자 및 대상자 활성화 위치 이해
description: CX Enterprise MCP 를 사용하여 대상자 활성화 상태를 모니터링하고, 대상 상태를 확인하고, 문제가 캠페인에 영향을 미치기 전에 문제를 파악할 수 있습니다.
last-substantial-update: 2026-06-09T00:00:00Z
index: false
source-git-commit: ed47f1547e6949fc71417e7d99d83802ae3c2134
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 3%

---


# 대상자 및 대상자 활성화 위치 이해

<!-- last-modified: 2026-06-04 -->

![활성화 권장 사항을 통해 우선 순위가 지정된 대상 전략을 제공하는 AI 클라이언트](../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png)

활성화된 대상, 유입되는 대상 및 대상이 정상인지 여부를 이해하면 일반적으로 Real-Time CDP을 열고 여러 화면을 탐색할 수 있습니다. 이 연습에서는 RTCDP MCP 서버를 사용하여 AI 클라이언트를 통해 동일한 답변을 얻는 방법을 보여 줍니다. 일반 언어 질문을 통해 대상 구성, 활성화 상태 및 데이터 흐름 상태를 표시합니다.

| 시나리오 세부 정보 | |
| --- | --- |
| CX 엔터프라이즈 애플리케이션 | [Real-Time Customer Data Platform(Real-Time CDP)](https://experienceleague.adobe.com/ko/docs/experience-platform/rtcdp/home) |
| 무생식 도구 | [CX 엔터프라이즈 MCP](../tools/mcp-servers.md#cx-enterprise-mcp-servers) |
| 대상자 | 마케터, 분석가, 운영자 |
| 사전 요구 사항 | MCP 호환 AI 클라이언트, Real-Time CDP 액세스 |

각 단계에는 하나의 대표적인 프롬프트와 예제 AI 응답이 표시됩니다. 같은 세션에서 추가 탐색을 위해 **수행할 수 있는 추가** 섹션이 다음과 같습니다.

## 시작하기에 앞서

>[!BEGINTABS]

>[!TAB 클라우드.ai]

CX Enterprise MCP 를 사용자 정의 커넥터로 연결하여 Real-Time CDP 도구에 액세스합니다.

1. Cloud.ai의 **설정 > 통합**(으)로 이동합니다.
2. **사용자 지정 커넥터 추가**&#x200B;를 선택하고 서버 URL을 입력하십시오. `https://cx-enterprise.adobe.io/mcp`
3. **연결**&#x200B;을 선택하고 Adobe ID으로 로그인하세요.

전체 설정: [Claude.ai 사용자 지정 커넥터 설명서](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

ChatGPT 개발자 모드(Pro, Plus, 비즈니스, 엔터프라이즈 또는 교육 계획 필요)를 사용하여 CX 엔터프라이즈 MCP를 연결합니다.

1. **ChatGPT 설정**&#x200B;에서 **개발자 모드**&#x200B;를 사용하도록 설정합니다.
2. **설정 > 통합**(으)로 이동하여 **사용자 지정 커넥터 추가 > 원격 MCP 서버**&#x200B;를 선택합니다.
3. 서버 URL 입력: `https://cx-enterprise.adobe.io/mcp`
4. **연결**&#x200B;을 선택하고 Adobe ID으로 로그인하세요.

전체 설정: [ChatGPT MCP 설명서](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB 기타 AI 클라이언트]

Gemini, Microsoft Copilot, Cursor, Claude Code 또는 다른 MCP 호환 환경을 사용하시겠습니까? 다음 끝점을 사용하여 CX 엔터프라이즈 MCP에 연결:

```
https://cx-enterprise.adobe.io/mcp
```

지원되는 모든 클라이언트에 대한 전체 설치 지침: [AI 클라이언트에 연결](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>메시지가 표시되면 Adobe ID으로 로그인하고 Real-Time CDP 인스턴스에 연결된 IMS 조직을 선택합니다. 잘못된 조직을 선택하는 것이 인증 오류의 가장 일반적인 원인입니다.

## 1단계: 대상자와 대상자의 표현 알아보기

먼저 사용 가능한 대상의 인벤토리와 이들이 캡처하는 고객 행동을 물어봅니다. 이렇게 하면 특정 세그먼트로 드릴다운하기 전에 전체 풍경을 볼 수 있습니다.

```
What audiences are currently available and what customer behaviors do they represent?
```

+++예제 응답 보기

![AI 클라이언트가 사용 가능한 대상 및 해당 대상이 나타내는 고객 행동을 나열함](../assets/use-cases/query-audiences/query-audiences-step1-audience-list.png)

+++


## 2단계: 가장 중요한 세그먼트 식별

대상 지형을 보고 어떤 세그먼트가 가장 큰지, 그리고 무엇이 이 세그먼트들을 전략적으로 가치 있게 만드는지 질문하십시오.

```
Which audiences are the largest and what makes them valuable?
```

+++예제 응답 보기

![가장 큰 대상을 식별하고 무엇이 이러한 대상을 귀중하게 하는지 설명하는 AI 클라이언트](../assets/use-cases/query-audiences/query-audiences-step2.gif)

+++


## 3단계: 활성화 및 대상 검토

대상이 현재 어디에 흐르고 있는지, 그리고 어떤 대상으로 활성화되었는지 질문합니다.

```
Where are our audiences currently being activated and to which destinations?
```

+++예제 응답 보기

![대상 활성화 상태 및 대상 매핑을 표시하는 AI 클라이언트](../assets/use-cases/query-audiences/query-audiences-step3.gif)

+++


## 4단계: 전략적 추천 받기

CX 엔터프라이즈 MCP 의 RTCDP 툴은 읽기 전용이며 활성화 상태, 대상 상태 및 데이터 흐름 데이터를 표시하지만 구성을 수정하지는 않습니다. 문제를 식별하면 애플리케이션에서 수정 사항이 발생합니다.

```
If you were our audience strategist, what would you prioritize next and why?
```

+++예제 응답 보기

![우선 순위가 지정된 대상 전략 권장 사항을 제공하는 AI 클라이언트](../assets/use-cases/query-audiences/query-audiences-step4.gif)

+++


>[!NOTE]
>
>CX Enterprise MCP의 RTCDP 도구는 대상 및 활성화 데이터를 표시하지만 대상 구성, 세그먼트 정의 또는 데이터 흐름 설정을 수정할 수 없습니다. 수정 단계는 Real-Time CDP 애플리케이션에서 발생합니다.

## 수행한 작업

AI 클라이언트를 Real-Time CDP에 연결하고 4개의 프롬프트에서 대상 포트폴리오의 전략적 그림을 빌드했습니다. 사용 가능한 대상을 캡처한 고객 행동에 매핑하고, 가장 크고 중요한 세그먼트를 식별하고, 각 대상이 흐르는 위치와 대상을 확인하고, 다음 활성화 시 우선 순위가 지정된 권장 사항을 받았습니다. 이렇게 하면 여러 Real-Time CDP 화면 탐색을 직접적이고 전략적인 대화로 대체합니다.

## 수행할 수 있는 작업 더 보기

CX 엔터프라이즈 MCP의 Real-Time CDP 도구는 광범위한 대상 및 활성화 쿼리를 지원합니다. 동일한 세션에서 시도할 수 있는 프롬프트를 보려면 아래 시나리오를 확장하십시오.

+++캠페인이 전송되기 전에 어디로 이동하는지 정확히 파악

활성화 실패는 침묵입니다. 대상자가 경고 없이 흐르지 않고 캠페인이 오래된 목록으로 전송됩니다. 이러한 프롬프트는 어떤 세그먼트가 어떤 대상에 언제 도달하는지 명확하게 파악할 수 있도록 해 줍니다.

**프롬프트**

```
Which audiences are activated to Google Ads?
```

```
Show me the activation history for the [audience name] audience.
```

```
What is the last refresh time for the [audience name] audience?
```

+++

+++캠페인에 영향을 미치기 전에 활성화 문제 파악

실행이 누락된 대상 또는 활성 대상이 없는 세그먼트는 캠페인이 의도한 것보다 적은 사람에게 도달하고 있을 수 있음을 의미합니다. 이러한 프롬프트는 이러한 간격을 능동적으로 표시합니다.

**프롬프트**

```
Are there any audiences with no active destinations?
```

```
Are any destination dataflows showing errors right now?
```

```
Which audiences have not been updated in the last 30 days?
```

+++

+++대상자 환경 감사 및 이해

대상 크기가 이동되거나 새 세그먼트가 만들어지면 인벤토리가 명확해져 잘못된 목록을 계획하고 활성화할 수 없습니다. 이러한 프롬프트는 요청 시 해당 가시성을 제공합니다.

**프롬프트**

```
How many profiles are in the [segment name] segment?
```

```
Show me all audiences created in the last 30 days.
```

```
Which audience has grown the most in the last 60 days?
```

```
How many total profiles are in my Real-Time CDP instance?
```

+++

+++ID 및 데이터 품질 이해

ID 네임스페이스 및 병합 정책은 대상자에 포함된 프로필과 해결 방법에 직접 영향을 줍니다. 이러한 프롬프트는 예기치 않은 대상 크기 또는 프로필 중복을 설명할 수 있는 구성 세부 정보를 표시합니다.

**프롬프트**

```
What identity namespaces are configured and which are most commonly used?
```

```
What merge policies are defined and which audiences use each one?
```

```
Are there any audiences using a non-default merge policy that could cause profile overlap?
```

+++


## 추가 정보

| 리소스 | 찾을 내용 |
| --- | --- |
| [Real-Time CDP MCP 설명서](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) | MCP 서버 설정 및 도구 참조 |
| [Adobe AI 레지스트리](https://developer.adobe.com/ai-registry/?type=mcp) | MCP 서버 메타데이터 및 가용성 |
| [Real-Time CDP 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/rtcdp/home) | 전체 Real-Time CDP 애플리케이션 설명서 |
| [AEP 대상 설명서](https://experienceleague.adobe.com/ko/docs/experience-platform/destinations/home) | 전체 대상 참조 |
