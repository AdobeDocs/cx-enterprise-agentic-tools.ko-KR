---
title: Adobe CX 엔터프라이즈 에이전트 툴
description: MCP 서버, 에이전트 기술 및 API를 사용하여 AI 에이전트 및 개발 도구를 Adobe CX Enterprise 기능에 연결합니다.
last-substantial-update: 2026-06-08T00:00:00Z
index: false
source-git-commit: ec08b7ff646519ceb10bd3431e0c0d5db8f3367f
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 3%

---


# Adobe CX 엔터프라이즈 에이전트 툴

<!-- last-modified: 2026-06-08 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491251/?captions=kor&learn=on&enablevpops)

AI가 Adobe CX Enterprise의 동료가 되도록 합니다. AI 클라이언트를 캠페인, 대상자, 여정 및 컨텐츠에 연결하고 이미 사용하는 도구에서 일반 언어로 상호 작용합니다. 시작하는 데 필요한 새 인터페이스, 컨텍스트 전환, 코딩이 없습니다.

>[!TIP]
>**CX Enterprise MCP로 시작** 하나의 연결을 통해 AI 클라이언트는 조직의 라이선스를 기반으로 Adobe Journey Optimizer, Customer Journey Analytics 및 Real-Time CDP에 액세스할 수 있습니다. [지금 연결](tools/mcp-servers.md#cx-enterprise-mcp)

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
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/mcp-servers.md" title="MCP 서버" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/mcp-servers-card.png" alt="MCP 서버"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/mcp-servers.md" target="_blank" rel="referrer" title="MCP 서버">MCP 서버</a>
                    </p>
                    <p class="is-size-6">MCP 호환 AI 클라이언트를 Adobe CX Enterprise 워크플로우에 연결합니다. AI 도구를 종료하지 않고 데이터를 쿼리하고, 캠페인을 분석하고 대상에 액세스합니다.</p>
                </div>
                <a href="tools/mcp-servers.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">MCP 서버 탐색</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/agent-skills.md" title="에이전트 스킬" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/agent-skills-card.png" alt="에이전트 스킬"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/agent-skills.md" target="_blank" rel="referrer" title="에이전트 스킬">에이전트 기술</a>
                    </p>
                    <p class="is-size-6">Adobe에서 제공하는 워크플로우로 에이전트에게 CX 엔터프라이즈 작업을 안내합니다. 한 번 인코딩되고 일관되게 적용되는 도메인 전문 지식.</p>
                </div>
                <a href="tools/agent-skills.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">에이전트 기술 살펴보기</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/apis.md" title="빌더용 API" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/apis-card.png" alt="빌더용 API"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        빌더용 <a href="tools/apis.md" target="_blank" rel="referrer" title="빌더용 API">API</a>
                    </p>
                    <p class="is-size-6">클라우드 코드 및 커서와 같은 에이전틱 코딩 툴을 사용하여 맞춤형 Adobe CX 엔터프라이즈 애플리케이션을 구축할 수 있습니다.</p>
                </div>
                <a href="tools/apis.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">빌더를 위한 API 탐색</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## 모든 팀을 위한 에이전트 툴

>[!BEGINTABS]

>[!TAB MCP 서버]

호환되는 모든 AI 클라이언트를 사용하여 코딩이 필요 없는 일반 언어로 CX 엔터프라이즈 애플리케이션에 액세스합니다. AJO, CJA 및 Real-Time CDP에 대한 단일 연결을 위해 CX Enterprise MCP로 시작하거나 AEM 및 기타 애플리케이션에 직접 연결합니다.

- Claude, Cursor, ChatGPT 및 기타 MCP 호환 클라이언트에서 몇 분 안에 연결
- 자연어를 사용하여 캠페인, 대상자 및 여정 데이터 쿼리
- 새 인터페이스 또는 교육이 필요하지 않음

[MCP 서버 시작](tools/mcp-servers.md)

>[!TAB 에이전트 기술]

에이전트 스킬은 AI 클라이언트가 수행할 수 있는 지침으로 Adobe 도메인 전문 지식을 인코딩합니다. 에이전트는 즉흥적으로 수행하는 대신 Adobe 모범 사례에 따라 안정적이고 반복적으로 수행할 수 있는 작업을 정확하게 알고 있습니다.

- 반복 가능한 CX 엔터프라이즈 워크플로우에 대한 일관된 결과
- Adobe을 에이전트에게 설명할 필요가 없습니다. 스킬이 처리합니다.
- 에이전트 기술을 지원하는 AI 클라이언트에서 작동합니다

[에이전트 스킬 탐색](tools/agent-skills.md)

>[!TAB 빌더용  API]

Adobe 제품을 실행하는 동일한 API에 직접 프로그래밍 방식으로 액세스합니다. 사용자 정의 애플리케이션 및 통합을 구축하여 팀이 특정 CX 엔터프라이즈 워크플로우에 대한 액세스 권한을 집중하고 관리할 수 있도록 합니다.

- 한 번 빌드하고 조직 전체에 배포합니다.
- 팀에 필요한 보호, 승인 및 사용자 지정 논리 추가
- 클라우드 코드, 커서 및 기타 아젠틱 코딩 도구를 사용하여 보다 신속하게 빌드

[빌더를 위한 API 살펴보기](tools/apis.md)

>[!ENDTABS]

## 실행 중인 무생식 도구

Adobe CX 엔터프라이즈 에이전트 툴의 실제 모습에 대해 알아보십시오. 각 연습에서는 설정부터 결과까지 실제 비즈니스 시나리오를 다루며 AI 클라이언트를 연결하는 방법, 질문 사항 및 돌아온 사항을 정확하게 보여 줍니다.

<!--
CARDS

* use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Surface Customer Journey Analytics comparisons and conversion trends through plain-language questions. Uses CX Enterprise MCP.}
  {cta = Start walkthrough}

* use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/analyze-campaign-performance.md" title="캠페인 성과 분석" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="캠페인 성과 분석"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" title="캠페인 성과 분석">캠페인 성과 분석</a>
                    </p>
                    <p class="is-size-6">일반 언어 질문을 통해 Customer Journey Analytics 비교 및 전환 트렌드를 표시합니다. CX 엔터프라이즈 MCP 사용</p>
                </div>
                <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">연습 시작</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Manage AEM content with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-aem-content.md" title="AI를 사용하여 AEM 콘텐츠 관리" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="AI를 사용하여 AEM 콘텐츠 관리"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-aem-content.md" target="_blank" rel="referrer" title="AI를 사용하여 AEM 콘텐츠 관리">AI로 AEM 콘텐츠 관리</a>
                    </p>
                    <p class="is-size-6">자연어를 사용하여 AEM에서 페이지 및 콘텐츠 조각을 검색, 업데이트 및 게시할 수 있습니다.</p>
                </div>
                <a href="use-cases/manage-aem-content.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">연습 시작</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

**[모든 연습 보기](use-cases/overview.md)**

## Adobe 리소스

| 리소스 | 찾을 내용 |
| --- | --- |
| [Adobe AI 레지스트리](https://developer.adobe.com/ai-registry/?type=mcp) | MCP 서버의 전체 카탈로그 |
| [Adobe 에이전트 기술](https://github.com/adobe/skills) | CX 엔터프라이즈 워크플로우를 위한 Adobe에서 제공하는 에이전트 기술 |
| [Adobe API 카탈로그](https://developer.adobe.com/apis) | 전체 Adobe CX Enterprise API 참조 |
| [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) | API 프로젝트 설정 및 인증 |
| [Adobe Admin Console](https://adminconsole.adobe.com) | 사용자 및 제품 액세스 관리 |
| [Experience League](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/home) | 전체 Adobe 애플리케이션 설명서 및 자습서 |
