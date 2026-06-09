---
title: 고객에게 영향을 미치기 전에 여정 문제 파악
description: CX Enterprise MCP Gateway를 사용하여 활성 AJO 여정을 모니터링하고, 캠페인 구성을 검토하고, 고객에게 도달하기 전에 운영 문제를 파악할 수 있습니다.
last-substantial-update: 2026-06-08T00:00:00Z
index: false
source-git-commit: 093448ea6a9840d1d2027b76e177b145400a9202
workflow-type: tm+mt
source-wordcount: '1008'
ht-degree: 3%

---


# 고객에게 영향을 미치기 전에 여정 문제 파악
<!-- last-modified: 2026-06-08 -->

![AJO 여정 검토](https://placehold.co/1600x900?text=Review+AJO+Journeys)

활성화된 여정, 해당 변수를 유도하는 조건 및 캠페인이 정상적으로 구성되는 방식에 대한 명확한 그림을 얻는다는 것은 Adobe Journey Optimizer을 열고 해당 인터페이스를 탐색한다는 의미입니다. 이 연습에서는 CX Enterprise MCP Gateway를 사용하여 일반 언어 질문을 통해 AJO 여정 및 캠페인 데이터를 쿼리하여 AI 클라이언트를 통해 동일한 가시성을 얻는 방법을 보여 줍니다.

| | |
| --- | --- |
| CX 엔터프라이즈 애플리케이션 | Adobe Journey Optimizer (AJO) |
| 무생식 도구 | CX 엔터프라이즈 MCP 게이트웨이 |
| 대상자 | 캠페인 관리자, 마케터 |
| 사전 요구 사항 | MCP 호환 AI 클라이언트, AJO 액세스 |

각 단계에는 하나의 대표적인 프롬프트와 예제 AI 응답이 표시됩니다. 같은 세션에서 추가 탐색을 위해 **수행할 수 있는 추가** 섹션이 다음과 같습니다.


## 시작하기에 앞서

>[!BEGINTABS]

>[!TAB 클라우드.ai]

CX 엔터프라이즈 MCP 게이트웨이를 맞춤형 커넥터로 연결하여 Adobe Journey Optimizer 도구에 액세스합니다.

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
>메시지가 표시되면 Adobe ID으로 로그인하고 AJO 환경에 연결된 IMS 조직을 선택합니다. 잘못된 조직을 선택하는 것이 인증 오류의 가장 일반적인 원인입니다.
>
>첫 번째 연결 시 AI 클라이언트가 IMS 조직을 선택하거나 샌드박스를 지정하도록 요청할 수 있습니다. 컨텍스트가 설정되면 MCP 서버는 세션의 나머지 부분에 컨텍스트를 사용합니다.
>
>일부 도구는 실행 전에 승인을 묻는 메시지를 표시합니다. 요청을 검토하고 승인 또는 거절합니다. 확인 없이는 아무 작업도 수행되지 않습니다.


## 1단계: 활성 여정 및 그 목적 살펴보기

먼저 활성 여정 인벤토리와 그 뒤에 있는 비즈니스 목표를 요청합니다. 특정 여정으로 이동하기 전에 전체 사진을 볼 수 있습니다.

```
What customer journeys are currently available and what business objectives do they support?
```

+++예제 응답 보기

![사용 가능한 고객 여정 및 비즈니스 목표를 나열하는 AI 클라이언트](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step1.gif)

+++



## 2단계: 여정의 단계 및 고객 경험 검토

여정 목록을 볼 때 AI 클라이언트에게 특정 여정의 단계를 안내하고 각 단계에서 고객이 경험하는 것을 설명하도록 요청합니다.

```
Walk me through the [journey name] journey and explain the customer experience.
```

+++예제 응답 보기

![새로운 고객 환영 여정 단계 및 고객 경험을 안내하는 AI 클라이언트](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step2-welcome-journey.png)

+++


>[!NOTE]
>
>`[journey name]`을(를) 1단계 결과의 여정 이름으로 바꾸십시오.


## 3단계: 캠페인, 대상자 및 목표 검토

여정에서 캠페인으로 이동합니다. 어떤 캠페인이 활성화되었는지, 어떤 캠페인을 대상으로 하는지, 어떤 결과를 도출하도록 설계되었는지를 요약해 주십시오.

```
Show me our campaigns, the audiences they target, and the outcomes they're designed to drive.
```

+++예제 응답 보기

![AI 클라이언트가 대상 타기팅 및 의도한 결과와 함께 활성 캠페인을 나열](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step3.gif)

+++



## 4단계: 캠페인과 여정이 연결되는 방식 이해

AI 고객에게 캠페인과 여정 간의 점을 연결하고 공유 참여 목표를 위해 함께 작동하는 방식을 설명합니다.

```
How do our campaigns and journeys work together to improve customer engagement?
```

+++예제 응답 보기

![캠페인과 여정 간의 관계를 설명하는 AI 클라이언트](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step4-connection.png)

+++



## 5단계: 우선 순위가 지정된 권장 사항 가져오기

라이프사이클 마케팅 관리자의 관점에서 다음에 집중해야 할 사항에 대한 우선 순위 추천을 요청합니다. 이는 세션에서 검토된 모든 것에서 가장 영향력 있는 격차와 기회를 표면화합니다.

```
If you were our lifecycle marketing manager, what would you prioritize next and why?
```

+++예제 응답 보기

![우선 순위가 지정된 라이프사이클 마케팅 권장 사항을 제공하는 AI 클라이언트](../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5.gif)

+++


>[!NOTE]
>
>AJO MCP 서버는 여정 및 캠페인 정보를 노출하지만 여정, 캠페인 또는 콘텐츠를 수정할 수 없습니다. 권장 사항을 구현하려면 AJO 애플리케이션으로 직접 이동하거나, 동일한 세션에서 콘텐츠를 변경하기 위해 AEM Content MCP 서버를 연결합니다.


## 수행한 작업

AI 클라이언트를 Adobe Journey Optimizer에 연결하고 5개의 프롬프트를 통해 여정 및 캠페인 포트폴리오의 전체 그림을 빌드했습니다. 활성 여정 및 해당 비즈니스 목표를 인벤토리하고, 특정 여정에 대한 단계별 고객 경험을 검토하고, 활성 캠페인을 대상과 의도한 결과에 매핑하고, 캠페인과 여정이 함께 작동하는 방식을 이해하고, 다음에 집중할 위치에 대한 우선 순위 추천을 받았습니다. 이를 통해 라이프사이클 마케팅 및 캠페인 관리자는 AJO 인터페이스를 열지 않고도 전략적으로 볼 수 있습니다.


## 수행할 수 있는 작업 더 보기

CX 엔터프라이즈 MCP 게이트웨이는 광범위한 AJO 여정 및 캠페인 세부 정보를 제공할 수 있습니다. 동일한 세션에서 시도할 수 있는 프롬프트를 보려면 아래 시나리오를 확장하십시오.

+++변경하기 전에 라이브 정보 확인

실행 중인 다른 항목을 알지 못한 채 여정을 변경하는 것은 위험합니다. 이러한 프롬프트는 활성 항목, 최근에 수정된 항목 및 캠페인이 구성되는 방식에 대한 현재 인벤토리를 제공합니다.

**프롬프트**

```
Show me all journeys modified in the last 7 days.
```

```
Show me all journeys that use SMS as a channel.
```

```
Which campaigns are scheduled to end this week?
```

```
What loyalty challenges are currently active?
```

+++

+++특정 여정의 세부 정보 살펴보기

여정을 검토, 승인 또는 전달해야 할 때 AJO을 열지 않고 전체 논리를 앞에 두면 시간이 절약됩니다. 이렇게 하면 요청 시 표면 조건, 스케줄 및 세그먼트 규칙이 표시됩니다.

**프롬프트**

```
What is the entry condition for the [journey name] journey?
```

```
What are the exit conditions and timeout rules for the [journey name] journey?
```

```
What messages and wait conditions are in the [journey name] journey?
```

```
Which segment does the [journey name] journey target?
```

+++

+++특정 캠페인의 세부 정보 살펴보기

승인, 전달 또는 변경하기 전에 캠페인의 전체 구성을 검토해야 하는 경우 이러한 프롬프트는 AJO을 열지 않고 대상 규칙, 채널 설정 및 일정 세부 사항을 표시합니다.

**프롬프트**

```
Walk me through the full configuration of the [campaign name] campaign.
```

```
What audience does the [campaign name] campaign target and how large is that segment?
```

```
What frequency cap and send schedule apply to the [campaign name] campaign?
```

```
Are any campaigns targeting overlapping audiences?
```

```
What channel configurations are set up in our AJO environment?
```

+++



## 추가 정보

| 리소스 | 찾을 내용 |
| --- | --- |
| [AI 레지스트리의 AJO MCP 서버](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) | AJO MCP 서버 도구 및 가용성 |
| [AJO 설명서](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/ajo-home) | 전체 AJO 애플리케이션 설명서 |
| [AJO API](https://developer.adobe.com/journey-optimizer-apis/) | 사용자 정의 통합을 위한 AJO API 참조 |
| [AJO 자습서](https://experienceleague.adobe.com/ko/docs/journey-optimizer-learn/tutorials/overview) | 비디오 튜토리얼 및 학습 경로 |
