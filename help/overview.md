---
title: Adobe CX 엔터프라이즈 에이전트 툴
description: MCP 서버, 에이전트 기술 및 API를 사용하여 AI 에이전트 및 개발 도구를 Adobe CX Enterprise 기능에 연결합니다.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 4%

---


# Adobe CX 엔터프라이즈 에이전트 툴

<!-- last-modified: 2026-05-08 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491235/?learn=on&enablevpops)

AI에게 **Adobe CX Enterprise** 데이터, 워크플로 및 자동화에 대한 직통 회선을 제공합니다. 호환되는 AI 클라이언트 또는 개발 도구에서 **일반 언어**&#x200B;로 캠페인을 쿼리하고, 대상을 활성화하고, 여정을 관리합니다.

<!--
CARDS

* tools/mcp-servers.md
  {title = MCP Servers}
  {description = Connect any MCP-compatible AI client to Adobe CX Enterprise workflows. Query data, analyze campaigns, and access audiences without leaving your AI tool.}
  {cta = Explore MCP Servers}
  {image = assets/mcp-servers-card.png}

* tools/agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflows that guide agents through CX Enterprise tasks. Domain expertise encoded once, applied consistently.}
  {cta = Explore Agent Skills}
  {image = assets/agent-skills-card.png}

* tools/apis.md
  {title = APIs for Builders}
  {description = Build custom Adobe CX Enterprise applications using agentic coding tools like Claude Code and Cursor.}
  {cta = Explore APIs for Builders}
  {image = assets/apis-card.png}
-->

## 모든 팀을 위한 에이전트 툴

>[!BEGINTABS]

>[!TAB 비즈니스 리더]

Adobe 에이전트 툴의 비즈니스 가치와 Adobe 투자를 확장하는 방법을 이해합니다.

- 에이전트를 사용하면 팀을 교체하지 않고도 마케팅 및 작업 워크플로를 가속화할 수 있습니다
- 액세스 제어, 감사 추적 및 루프 내 인간 워크플로우는 처음부터 기본으로 제공됩니다
- 아젠틱 툴은 Adobe 표면뿐만 아니라 모든 호환 가능한 AI 클라이언트에서 작동합니다
- 데이터는 사용자의 권한에 의해 관리되고 사용자의 환경에 유지됩니다

팀이 현재 이러한 무의미한 도구를 사용하여 어떤 작업을 수행하는지 이해하려면 [실제 연습](agentic-tools-in-action.md)을 참조하세요.

>[!TAB 비즈니스 사용자]

에이전트 도구가 일상적인 Adobe 워크플로를 가속화하는 방법을 알아봅니다.

- [MCP 서버](tools/mcp-servers.md)를 사용하여 몇 분 안에 AI 클라이언트를 Adobe 데이터에 연결
- 일반적인 [캠페인](use-cases/analyze-campaign-performance.md), [대상자](use-cases/query-audiences.md) 및 [여정](use-cases/manage-ajo-journeys.md) 작업에 대한 단계별 연습 준수
- 이미 사용 중인 AI 환경에서 작업

>[!TAB 빌더 및 개발자]

Adobe CX 엔터프라이즈 기능을 맞춤형 애플리케이션 및 에이전트에 통합합니다.

- 기능 영역별로 [빌더용 API](tools/apis.md)를 검색하고 개발 환경의 [MCP 서버](tools/mcp-servers.md)에 연결합니다.
- Adobe API와 함께 [클라우드 코드](https://docs.anthropic.com/en/docs/claude-code/mcp) 및 [커서](https://cursor.com/docs/mcp)와 같은 AI 지원 코딩 도구 사용
- [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)에서 인증 및 자격 증명 설정
- 지원되는 AI 클라이언트 및 설치 지침에 대한 전체 목록은 [MCP 서버](tools/mcp-servers.md)를 참조하십시오

>[!TAB 관리자]

액세스 관리, 승인된 에이전트 도구 관리 및 조직 전반에 대한 감독 유지

- [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)을(를) 통해 MCP 서버 및 API에 대한 인증 구성
- 에이전트 도구에 액세스할 수 있는 사용자 및 팀을 제어하기 위해 IMS(Identity Management 시스템) 조직 수준 권한을 설정합니다
- 조직에서 사용할 수 있도록 승인된 AI 클라이언트 및 MCP 서버를 정의하고 적용합니다
- 사용 모니터링, 감사 추적 검토 및 에이전트 작업이 규정 준수 요구 사항을 충족하는지 확인

인증 설정에 대해서는 [MCP 서버](tools/mcp-servers.md)를, 자격 증명 및 프로젝트 관리에 대해서는 [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)을 참조하십시오.

>[!ENDTABS]

## 실행 중인 무생식 도구

Adobe CX 엔터프라이즈 에이전트 툴의 실제 모습에 대해 알아보십시오. 각 연습에서는 설정부터 결과까지 실제 비즈니스 시나리오를 다루며 AI 클라이언트를 연결하는 방법, 질문 사항 및 돌아온 사항을 정확하게 보여 줍니다.

<!--
CARDS

* use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use the CX Enterprise MCP Gateway to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use the CX Enterprise MCP Gateway to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use the CX Enterprise MCP Gateway to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine CJA and AEM MCP Servers to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Connect AJO, CJA, and Real-Time CDP in one AI session for a unified view of campaign health.}
  {cta = Start walkthrough}
-->

## Adobe 리소스

| 리소스 | 찾을 내용 |
| --- | --- |
| [Adobe AI 레지스트리](https://developer.adobe.com/ai-registry/?type=mcp) | 사용 가능한 MCP 서버 및 에이전트 기술의 전체 카탈로그 |
| [Adobe API 카탈로그](https://developer.adobe.com/apis) | 전체 Adobe CX Enterprise API 참조 |
| [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) | API 프로젝트 설정 및 인증 |
| [Experience League](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/home) | 전체 Adobe 애플리케이션 설명서 및 자습서 |
