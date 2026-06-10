---
title: Adobe CX 엔터프라이즈 에이전트 툴
description: MCP 서버, 에이전트 기술 및 API를 사용하여 AI 에이전트 및 개발 도구를 Adobe CX Enterprise 기능에 연결합니다.
last-substantial-update: 2026-06-08T00:00:00Z
index: false
source-git-commit: da8d1eb1dcfef13af5d24ef1fe22ee9977c4e783
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 3%

---


# Adobe CX 엔터프라이즈 에이전트 툴

<!-- last-modified: 2026-06-08 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491251/?captions=kor&learn=on&enablevpops)

AI가 Adobe CX Enterprise의 공동 작업자가 되도록 합니다. AI 클라이언트를 캠페인, 대상자, 여정 및 컨텐츠에 연결합니다. 이미 사용하는 도구에서 일반 언어로 사용자와 상호 작용합니다. 시작하는 데 필요한 새 인터페이스, 컨텍스트 전환, 코딩이 없습니다.

>[!TIP]
>**CX Enterprise MCP로 시작** 하나의 연결을 통해 AI 클라이언트는 조직의 라이선스를 기반으로 Adobe Journey Optimizer, Customer Journey Analytics 및 Real-Time CDP에 액세스할 수 있습니다. [지금 연결](tools/mcp-servers.md#cx-enterprise-mcp-servers)

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
                    <a href="tools/mcp-servers.md" title="MCP 서버">
                        <img class="is-bordered-r-small" src="assets/mcp-servers-card.png" alt="MCP 서버"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/mcp-servers.md" title="MCP 서버">MCP 서버</a>
                    </p>
                    <p class="is-size-6">MCP 호환 AI 클라이언트를 Adobe CX Enterprise 워크플로우에 연결합니다. AI 도구를 종료하지 않고 데이터를 쿼리하고, 캠페인을 분석하고 대상에 액세스합니다.</p>
                </div>
                <a href="tools/mcp-servers.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">MCP 서버 탐색</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/agent-skills.md" title="에이전트 스킬">
                        <img class="is-bordered-r-small" src="assets/agent-skills-card.png" alt="에이전트 스킬"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/agent-skills.md" title="에이전트 스킬">에이전트 기술</a>
                    </p>
                    <p class="is-size-6">Adobe에서 제공하는 워크플로우로 에이전트에게 CX 엔터프라이즈 작업을 안내합니다. 한 번 인코딩되고 일관되게 적용되는 도메인 전문 지식.</p>
                </div>
                <a href="tools/agent-skills.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">에이전트 기술 살펴보기</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/apis.md" title="빌더용 API">
                        <img class="is-bordered-r-small" src="assets/apis-card.png" alt="빌더용 API"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        빌더용 <a href="tools/apis.md" title="빌더용 API">API</a>
                    </p>
                    <p class="is-size-6">클라우드 코드 및 커서와 같은 에이전틱 코딩 툴을 사용하여 맞춤형 Adobe CX 엔터프라이즈 애플리케이션을 구축할 수 있습니다.</p>
                </div>
                <a href="tools/apis.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
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

호환되는 AI 클라이언트를 사용하여 CX 엔터프라이즈 애플리케이션에 일반 언어로 액세스합니다. 코딩이 필요하지 않습니다. AJO, CJA 및 Real-Time CDP에 대한 단일 연결을 위해 CX Enterprise MCP로 시작하거나 AEM 및 기타 애플리케이션에 직접 연결합니다.

- Claude, Cursor, ChatGPT 및 기타 MCP 호환 클라이언트에서 몇 분 안에 연결
- 자연어를 사용하여 캠페인, 대상자 및 여정 데이터 쿼리
- 새 인터페이스 또는 교육이 필요하지 않음

[MCP 서버 시작](tools/mcp-servers.md)

>[!TAB 에이전트 기술]

에이전트 스킬은 AI 클라이언트가 수행할 수 있는 지침으로 Adobe 도메인 전문 지식을 인코딩합니다. 에이전트는 즉흥적으로 수행하는 대신 Adobe 모범 사례에 따라 안정적이고 반복적으로 수행할 수 있는 작업을 정확하게 알고 있습니다.

- 반복 가능한 CX 엔터프라이즈 워크플로우에 대한 일관된 결과
- Adobe을 에이전트에게 설명할 필요가 없습니다. 스킬이 처리합니다
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
  {title = Campaign insights without reports}
  {description = Ask performance questions in plain language and get answers from Customer Journey Analytics, without building a single report.}
  {cta = Surface campaign insights}

* use-cases/manage-aem-content.md
  {title = Ship content updates faster}
  {description = Find, update, and publish AEM pages and content fragments faster, without switching to the AEM interface.}
  {cta = Ship content faster}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Campaign insights without reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/analyze-campaign-performance.md" title="보고서가 없는 Campaign 인사이트">
                        <img class="is-bordered-r-small" src="assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="보고서가 없는 Campaign 인사이트"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/analyze-campaign-performance.md" title="보고서가 없는 Campaign 인사이트">보고서가 없는 캠페인 인사이트</a>
                    </p>
                    <p class="is-size-6">단일 보고서를 작성하지 않고도 일반 언어로 성능 질문에 답변하고 Customer Journey Analytics에서 답변을 얻을 수 있습니다.</p>
                </div>
                <a href="use-cases/analyze-campaign-performance.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Surface Campaign 인사이트</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Ship content updates faster">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-aem-content.md" title="더 빠른 콘텐츠 업데이트 배송">
                        <img class="is-bordered-r-small" src="assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="더 빠른 콘텐츠 업데이트 배송"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-aem-content.md" title="더 빠른 콘텐츠 업데이트 배송">콘텐츠 업데이트 더 빨리 보내기</a>
                    </p>
                    <p class="is-size-6">AEM 인터페이스로 전환하지 않고도 AEM 페이지 및 컨텐츠 조각을 보다 빠르게 찾고, 업데이트하고, 게시할 수 있습니다.</p>
                </div>
                <a href="use-cases/manage-aem-content.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">더 빠르게 콘텐츠 배송</span>
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
| [Adobe AI 레지스트리](https://developer.adobe.com/ai-registry/?type=mcp) | 일부 Adobe MCP 서버에 대한 관리되는 커넥터 및 서버 세부 정보 |
| [Adobe 에이전트 기술](https://github.com/adobe/skills) | CX 엔터프라이즈 워크플로우를 위한 Adobe에서 제공하는 에이전트 기술 |
| [Adobe API 카탈로그](https://developer.adobe.com/apis) | 전체 Adobe CX Enterprise API 참조 |
| [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) | API 프로젝트 설정 및 인증 |
| [Adobe Admin Console](https://adminconsole.adobe.com) | 사용자 및 제품 액세스 관리 |
| [Experience League](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/home) | 전체 Adobe 애플리케이션 설명서 및 자습서 |
