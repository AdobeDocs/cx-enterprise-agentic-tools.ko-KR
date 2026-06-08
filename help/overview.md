---
title: Adobe CX 엔터프라이즈 에이전트 툴
description: MCP 서버, 에이전트 기술 및 API를 사용하여 AI 에이전트 및 개발 도구를 Adobe CX Enterprise 기능에 연결합니다.
index: false
source-git-commit: d6c236f5405fac4b9813280d9fac2d4a60968924
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 2%

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
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/analyze-campaign-performance.md" title="캠페인 성과 분석" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Analyze+Campaign+Performance" alt="캠페인 성과 분석"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" title="캠페인 성과 분석">캠페인 성과 분석</a>
                    </p>
                    <p class="is-size-6">CX 엔터프라이즈 MCP 게이트웨이를 사용하여 모든 AI 클라이언트의 Customer Journey Analytics 지표 및 통찰력을 확인할 수 있습니다.</p>
                </div>
                <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">연습 시작</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/query-audiences.md" title="쿼리 대상자" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Query+Audiences" alt="쿼리 대상자"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/query-audiences.md" target="_blank" rel="referrer" title="쿼리 대상자">대상자 쿼리</a>
                    </p>
                    <p class="is-size-6">CX 엔터프라이즈 MCP 게이트웨이를 사용하여 일반 언어 프롬프트를 사용하여 Real-Time CDP 대상 및 대상 데이터를 쿼리할 수 있습니다.</p>
                </div>
                <a href="use-cases/query-audiences.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">연습 시작</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Review AJO journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-ajo-journeys.md" title="AJO 여정 검토" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Review+AJO+Journeys" alt="AJO 여정 검토"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" title="AJO 여정 검토">AJO 여정 검토</a>
                    </p>
                    <p class="is-size-6">CX 엔터프라이즈 MCP 게이트웨이를 사용하여 AJO 여정, 캠페인 상태 및 AI 클라이언트로부터의 여정 조건에 액세스할 수 있습니다.</p>
                </div>
                <a href="use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
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
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Manage+AEM+Content+with+AI" alt="AI를 사용하여 AEM 콘텐츠 관리"
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
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Optimize content based on performance data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/optimize-content-with-performance-data.md" title="성능 데이터를 기반으로 콘텐츠 최적화" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data" alt="성능 데이터를 기반으로 콘텐츠 최적화"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" title="성능 데이터를 기반으로 콘텐츠 최적화">성능 데이터를 기반으로 콘텐츠 최적화</a>
                    </p>
                    <p class="is-size-6">CJA 및 AEM MCP 서버를 결합하여 성과가 낮은 콘텐츠를 찾고 한 세션에서 업데이트합니다.</p>
                </div>
                <a href="use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">연습 시작</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Run a cross-channel campaign review">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/cross-channel-campaign-review.md" title="크로스 채널 캠페인 검토 실행" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review" alt="크로스 채널 캠페인 검토 실행"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" title="크로스 채널 캠페인 검토 실행">크로스 채널 캠페인 검토 실행</a>
                    </p>
                    <p class="is-size-6">AJO, CJA 및 Real-Time CDP을 하나의 AI 세션에 연결하여 캠페인 상태를 통합적으로 볼 수 있습니다.</p>
                </div>
                <a href="use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">연습 시작</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Adobe 리소스

| 리소스 | 찾을 내용 |
| --- | --- |
| [Adobe AI 레지스트리](https://developer.adobe.com/ai-registry/?type=mcp) | 사용 가능한 MCP 서버 및 에이전트 기술의 전체 카탈로그 |
| [Adobe API 카탈로그](https://developer.adobe.com/apis) | 전체 Adobe CX Enterprise API 참조 |
| [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) | API 프로젝트 설정 및 인증 |
| [Experience League](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/home) | 전체 Adobe 애플리케이션 설명서 및 자습서 |
