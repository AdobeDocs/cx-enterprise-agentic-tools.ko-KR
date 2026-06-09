---
title: 에이전트 스킬
description: AI 에이전트에게 CX 엔터프라이즈 작업을 일관되게 안내하는 Adobe에서 선별된 워크플로 및 지침입니다.
last-substantial-update: 2026-05-19T00:00:00Z
index: false
source-git-commit: 1d568bb9c3d948a0470c0f5d110ebb8fa696a53c
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 7%

---


# 에이전트 스킬

<!-- last-modified: 2026-05-19 -->

![Adobe CX Enterprise용 에이전트 기술](../assets/hero-agent-skills.png)

에이전트 기술은 Adobe에서 제공하는 워크플로우로, AI 에이전트에게 Adobe CX Enterprise 작업을 안정적으로 완료하기 위한 단계별 지침을 제공합니다. 각 에이전트 스킬은 도메인의 전문 지식 및 모범 사례를 인코딩하여 에이전트가 즉흥할 필요 없이 일관되고 검증된 결과를 생성하도록 합니다. 에이전트 기술은 특히 매번 세부 메시지를 확인해야 하는 작업에 대해 대화 간에 반복 가능하고 안내되는 동작을 원하는 경우 적합합니다. MCP 서버 및 API를 보완합니다. 에이전트 기술은 에이전트 작동 방식을 정의합니다. MCP 서버 및 API는 기본 액세스를 제공합니다.

## Adobe CX 엔터프라이즈 에이전트 기술

아래 기능 영역을 선택하여 해당 워크플로우에 대한 기술을 살펴보십시오.

<!--
CARDS

* https://github.com/adobe/skills/tree/main/plugins/aem
  {title = Adobe Experience Manager}
  {description = Agent Skills for Experience Manager development, content, design, and project management across AEM as a Cloud Service, Edge Delivery Services, and AEM 6.5 LTS.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-aem-card.png}

* https://github.com/adobe/skills/tree/main/plugins/adobe-analytics
  {title = Adobe Analytics}
  {description = Agent Skills for KPI monitoring, funnel analysis, and executive reporting workflows in Adobe Analytics.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-analytics-card.png}

* https://github.com/adobe/skills/tree/main/plugins/adobe-cja
  {title = Customer Journey Analytics}
  {description = Agent Skills for performance comparison, dimension analysis, and workspace authoring in Customer Journey Analytics.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-cja-card.png}

* https://github.com/adobe/skills/tree/main/plugins/app-builder
  {title = Adobe App Builder}
  {description = Agent Skills for scaffolding, testing, and deploying custom applications with Adobe App Builder.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-cxenterprise-card.png}

* https://github.com/adobe/skills/tree/main/plugins/creative-cloud
  {title = Creative Cloud}
  {description = Agent Skills for batch photo editing, design from templates, video editing, and social media variants with Creative Cloud.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-creative-cloud.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Experience Manager">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/aem" title="Adobe Experience Manager" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-aem-card.png" alt="Adobe Experience Manager"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/aem" target="_blank" rel="referrer" title="Adobe Experience Manager">Adobe Experience Manager</a>
                    </p>
                    <p class="is-size-6">AEM as a Cloud Service, Edge Delivery Services 및 AEM 6.5 LTS에서 Experience Manager 개발, 콘텐츠, 디자인 및 프로젝트 관리를 위한 에이전트 기술입니다.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/aem" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">에이전트 기술 보기</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-analytics" title="Adobe Analytics" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-analytics-card.png" alt="Adobe Analytics"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-analytics" target="_blank" rel="referrer" title="Adobe Analytics">Adobe Analytics</a>
                    </p>
                    <p class="is-size-6">Adobe Analytics의 KPI 모니터링, funnel 분석 및 경영진 보고 워크플로우를 위한 에이전트 기술.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-analytics" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">에이전트 기술 보기</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Customer Journey Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-cja" title="Customer Journey Analytics" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-cja-card.png" alt="Customer Journey Analytics"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-cja" target="_blank" rel="referrer" title="Customer Journey Analytics">Customer Journey Analytics</a>
                    </p>
                    <p class="is-size-6">Customer Journey Analytics의 성능 비교, 차원 분석 및 작업 영역 작성을 위한 에이전트 기술입니다.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-cja" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">에이전트 기술 보기</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe App Builder">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/app-builder" title="Adobe App Builder" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-cxenterprise-card.png" alt="Adobe App Builder"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/app-builder" target="_blank" rel="referrer" title="Adobe App Builder">Adobe App Builder</a>
                    </p>
                    <p class="is-size-6">Adobe App Builder을 사용하여 맞춤형 애플리케이션을 스캐폴딩, 테스트 및 배포하는 에이전트 기술입니다.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/app-builder" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">에이전트 기술 보기</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Creative Cloud">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/creative-cloud" title="Creative Cloud" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-creative-cloud.png" alt="Creative Cloud"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/creative-cloud" target="_blank" rel="referrer" title="Creative Cloud">Creative Cloud</a>
                    </p>
                    <p class="is-size-6">Creative Cloud을 사용한 일괄 사진 편집, 템플릿에서의 디자인, 비디오 편집 및 소셜 미디어 변형을 위한 에이전트 기술.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/creative-cloud" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">에이전트 기술 보기</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## 에이전트 스킬 작동 방식

![에이전트 기술 작동 방식](../assets/hero-connect-agent-skills.gif)

에이전트 스킬은 Adobe 에이전트 도구를 사용하여 작업을 완료하는 방법을 AI 에이전트에게 알려 주는 지침 세트입니다. 에이전트가 스킬을 로드할 때, 즉흥적으로 처리하지 않고 해당 워크플로우를 따릅니다.

- 에이전트는 매번 동일한 방식으로 작업을 완료합니다
- 도메인 전문 지식은 한 번 인코딩되어 대화에서 재사용됩니다.
- 스킬은 여러 에이전트 툴과 작업을 하나의 워크플로우로 연결할 수 있습니다

## 시작하기

사용하는 AI 클라이언트를 기반으로 에이전트 스킬이 설치됩니다. 일부 클라이언트는 명령줄에서 직접 설치를 지원합니다.

- **클라우드 코드**: `/plugin install adobe/skills`
- **노드 환경**: `npx skills add adobe/skills`
- **GitHub CLI**: `gh upskill adobe/skills`

다른 클라이언트는 기술 파일을 다운로드하여 AI 클라이언트에 직접 추가해야 합니다. 클라이언트의 전체 설치 지침은 [GitHub의 Adobe 기술 추가 정보](https://github.com/adobe/skills#installation)를 참조하십시오.

### 에이전트 스킬 찾기

[Adobe 기술 GitHub 저장소](https://github.com/adobe/skills)에서 사용 가능한 기술의 전체 목록을 찾아봅니다. 각 에이전트 스킬에는 자세한 지침, 참조 및 예가 포함된 `SKILL.md` 파일이 포함되어 있습니다.

`adobe/skills` 패키지를 설치하거나 추가한 후 일부 AI 클라이언트에서 사용 가능한 모든 기술을 직접 나열할 수 있습니다.

- **클라우드 코드**: `claude /plugin list`
- **노드 환경**: `npx skills list`
- **GitHub CLI**: `gh upskill list`

## 에이전트 기술과 MCP 서버 및 Builders용 API 비교

| | 에이전트 스킬 | MCP 서버 | 빌더용 API |
| --- | --- | --- | --- |
| 용도 | 안내식 워크플로우 및 모범 사례 | Adobe 데이터 및 워크플로우 액세스 | 직접 시스템 통합 |
| 도메인 전문 지식 인코딩 | 예 | 아니오 | 아니오 |
| 코딩 필요 | 아니요 | 아니오 | 예 |
| 다음에 최적 | 반복 가능한 안내 작업 | 데이터 쿼리 및 워크플로우 작업 | 사용자 정의 애플리케이션 개발 |
