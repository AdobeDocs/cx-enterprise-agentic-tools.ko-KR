---
title: 무생식 도구
description: 빌더를 위한 MCP 서버, 에이전트 기술 및 API를 비교하고 Adobe CX 엔터프라이즈 워크플로우에 적합한 에이전트 도구를 선택합니다.
index: false
source-git-commit: 3c29bfeeef3d2cb523724db02448aaa77cdf8900
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 1%

---


# 무생식 도구

<!-- last-modified: 2026-05-08 -->

모든 무의미한 도구 접근 방식이 동일한 필요를 제공하는 것은 아닙니다. MCP 서버는 호환되는 AI 클라이언트의 Adobe 데이터에 코딩 작업 없이 즉시 자연어로 액세스할 수 있도록 합니다. 에이전트 기술은 Adobe 도메인 전문 지식을 반복 가능한 에이전트 워크플로로 인코딩하므로 작업이 항상 실행됩니다. API는 개발자에게 사용자 지정 애플리케이션 및 통합을 구축하기 위한 완전한 프로그래밍 방식 제어를 제공합니다. 이 페이지에서는 상황에 적합한 시작점을 선택할 수 있도록 장단점에 대해 설명합니다.

<!--
CARDS

* mcp-servers.md
  {title = MCP Servers}
  {description = Connect any compatible AI client to Adobe CX Enterprise data and workflows. No coding required.}
  {cta = Explore MCP Servers}
  {image = ../assets/mcp-servers-card.png}

* agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflow instructions that guide agents through CX Enterprise tasks consistently.}
  {cta = Explore Agent Skills}
  {image = ../assets/agent-skills-card.png}

* apis.md
  {title = APIs for Builders}
  {description = Build custom applications and integrations using the same APIs that power Adobe products.}
  {cta = Explore APIs for Builders}
  {image = ../assets/apis-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="mcp-servers.md" title="MCP 서버" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-servers-card.png" alt="MCP 서버"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="mcp-servers.md" target="_blank" rel="referrer" title="MCP 서버">MCP 서버</a>
                    </p>
                    <p class="is-size-6">호환되는 모든 AI 클라이언트를 Adobe CX 엔터프라이즈 데이터 및 워크플로우에 연결합니다. 코딩이 필요하지 않습니다.</p>
                </div>
                <a href="mcp-servers.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">MCP 서버 탐색</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="agent-skills.md" title="에이전트 스킬" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="에이전트 스킬"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="agent-skills.md" target="_blank" rel="referrer" title="에이전트 스킬">에이전트 기술</a>
                    </p>
                    <p class="is-size-6">Adobe에서 제공하는 워크플로 지침은 에이전트에게 CX 엔터프라이즈 작업을 일관되게 안내합니다.</p>
                </div>
                <a href="agent-skills.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">에이전트 기술 살펴보기</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="apis.md" title="빌더용 API" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/apis-card.png" alt="빌더용 API"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        빌더용 <a href="apis.md" target="_blank" rel="referrer" title="빌더용 API">API</a>
                    </p>
                    <p class="is-size-6">Adobe 제품을 구동하는 동일한 API를 사용하여 사용자 정의 애플리케이션 및 통합을 구축할 수 있습니다.</p>
                </div>
                <a href="apis.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">빌더를 위한 API 탐색</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


## 무생식 도구 비교

| | MCP 서버 | 에이전트 스킬 | 빌더용 API |
| --- | --- | --- | --- |
| 다음에 최적 | AI 클라이언트 사용자 | 모든 사용자 | 개발자 |
| 코딩 필요 | 아니요 | 아니오 | 예 |
| 설정 시간 | 분 | 분 | 시간 ~ 일 |
| 받은 항목 | AI 도구에서 Adobe 액세스 | 가이드 및 반복 가능한 워크플로 | 전체 프로그램 제어 |
| AI 클라이언트 필요 | 예 | 예 | 선택 사항입니다 |

## 어디서부터 시작할지 모르겠습니까?

- AI를 사용하여 Adobe CX 엔터프라이즈 애플리케이션과 상호 작용하려면(작업을 수행하고, 데이터를 쿼리하고, AI가 자연스러운 대화를 통해 다음 작업을 찾도록 허용) [MCP 서버](mcp-servers.md)가 가장 유연한 시작점입니다.
- 에이전트가 즉흥적으로 실행하지 않고 Adobe 기반의 워크플로를 일관되게 따르도록 하려면 [에이전트 기술](agent-skills.md)이(가) 재사용 가능한 지침에 해당 도메인 전문 지식을 인코딩합니다.
- 사용자의 특정 Adobe 워크플로를 간소화하거나 자동화하는 집중 응용 프로그램을 빌드하기 위해 [빌더용 API](apis.md)를 사용하면 발생하는 작업을 직접 프로그래밍 방식으로 제어할 수 있습니다.

>[!BEGINTABS]

>[!TAB MCP 서버]

MCP 서버를 AI 도구와 Adobe 사이의 라이브 와이어로 생각해 보십시오. 한 번 연결하면 AI가 캠페인을 쿼리하고 대상을 가져오고 여정 상태를 확인하는 등의 작업을 수행할 수 있습니다. 모든 것이 일반 언어로 되어 있으므로 코드가 필요하지 않습니다.

**다음 경우에 MCP 서버 사용:**

- 이미 사용하고 있는 AI 도구 내에 Adobe 데이터를 원하는 경우
- 탐색적 분석 또는 임시 데이터 검색을 수행하는 경우
- 프로젝트를 회전하지 않고 결과를 빠르게 원하는 경우

**사용해 보기:** 클라우드에게 활성 여정을 요약하도록 요청하세요. ChatGPT에서 Real-Time CDP 대상 크기를 가져옵니다. 대시보드를 열지 않고 CJA 캠페인 지표를 검토합니다.

[MCP 서버 탐색](mcp-servers.md)

>[!TAB 에이전트 기술]

에이전트 기술은 에이전트가 따를 수 있는 지침으로 인코딩된 Adobe의 도메인 전문 기술입니다. 스킬은 에이전트가 올바른 단계를 이해하기를 바라는 대신 무엇을 해야 하는지 정확하게 알려줍니다. 안정적이고 반복 가능하며 이미 조정된 Adobe 워크플로우입니다.

**다음의 경우 에이전트 기술을 사용합니다.**

- 매번 같은 방법으로 같은 작업을 수행해야 합니다.
- 반복 가능한 콘텐츠 또는 미디어 프로덕션 워크플로우를 실행 중입니다.
- 설명하지 않아도 Adobe을 아는 에이전트가 필요합니다.

**시도해 보세요.** 사진 집합을 일괄 편집하여 통합적으로 표시합니다. 하나의 소스 에셋에서 플랫폼용 소셜 변형을 생성합니다. 몇 가지 프롬프트에서 Adobe Express 템플릿에서 디자인합니다.

[에이전트 스킬 탐색](agent-skills.md)

>빌더용 [!TAB API]

API는 기본 구성단위입니다. 개발자는 Adobe의 자체 제품을 구동하는 동일한 API를 사용하여 Adobe 데이터 및 작업에 직접 프로그래밍 방식으로 액세스할 수 있습니다. 이를 사용하여 일정, 조건 및 스택에 따라 실행되는 항목을 빌드합니다.

**API 사용 시기:**

- 사용자 정의 응용 프로그램 또는 대시보드를 만드는 중입니다.
- Adobe 데이터를 다른 시스템에 통합해야 합니다
- 클라우드 코드 또는 커서를 사용하여 전체 응용 프로그램을 생성하고 있습니다.
- 전체 만들기, 업데이트 또는 삭제 제어가 필요합니다.

**시도:** 사용자 지정 캠페인 대시보드를 빌드합니다. 데이터 파이프라인을 자동화합니다. Adobe Experience Platform에 읽고 쓰는 클라우드 코드로 애플리케이션을 생성합니다.

[빌더를 위한 API 살펴보기](apis.md)

>[!ENDTABS]

## 함께 사용

MCP 서버, 에이전트 기술 및 API는 상호 보완적입니다. 많은 워크플로가 다음 세 가지 모두를 결합합니다.

- 에이전트 스킬은 워크플로를 정의하고 에이전트를 안내합니다
- MCP 서버는 워크플로 중간에 Adobe 데이터에 대한 읽기 액세스 권한을 에이전트에게 부여합니다
- API는 직접 시스템 쓰기 또는 사용자 지정 애플리케이션 논리가 필요한 작업을 처리합니다
