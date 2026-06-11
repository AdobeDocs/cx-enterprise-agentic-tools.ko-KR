---
title: 에이전트 스킬
description: AI 에이전트에게 CX 엔터프라이즈 작업을 일관되게 안내하는 Adobe에서 선별된 워크플로 및 지침입니다.
last-substantial-update: 2026-05-19T00:00:00Z
index: false
source-git-commit: 8630ab022f4565471b6f8e357d5d87b7e8507ff3
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---


# 에이전트 스킬

<!-- last-modified: 2026-06-11 -->

![Adobe CX Enterprise용 에이전트 기술](../assets/hero-agent-skills.png)

에이전트 기술은 Adobe에서 제공하는 워크플로우로, AI 에이전트에게 Adobe CX Enterprise 작업을 안정적으로 완료하기 위한 단계별 지침을 제공합니다. 각 에이전트 스킬은 도메인의 전문 지식 및 모범 사례를 인코딩하여 에이전트가 즉흥할 필요 없이 일관되고 검증된 결과를 생성하도록 합니다. 에이전트 기술은 특히 매번 세부 메시지를 확인해야 하는 작업에 대해 대화 간에 반복 가능하고 안내되는 동작을 원하는 경우 적합합니다. MCP 서버 및 API를 보완합니다. 에이전트 기술은 에이전트 작동 방식을 정의합니다. MCP 서버 및 API는 기본 액세스를 제공합니다.

## Adobe CX 엔터프라이즈 에이전트 기술

아래 기능 영역을 선택하여 해당 워크플로우에 대한 기술을 살펴보십시오.

>[!BEGINTABS]

>[!TAB Adobe Experience Manager]

AEM as a Cloud Service, Edge Delivery Services 및 AEM 6.5 LTS에서 Experience Manager 개발, 콘텐츠, 디자인 및 프로젝트 관리를 위한 에이전트 기술입니다.

[에이전트 스킬 보기](https://github.com/adobe/skills/tree/main/plugins/aem)

>[!TAB Adobe Analytics]

Adobe Analytics의 KPI 모니터링, funnel 분석 및 경영진 보고 워크플로우를 위한 에이전트 기술.

[에이전트 스킬 보기](https://github.com/adobe/skills/tree/main/plugins/adobe-analytics)

>[!TAB Customer Journey Analytics]

Customer Journey Analytics의 성능 비교, 차원 분석 및 작업 영역 작성을 위한 에이전트 기술입니다.

[에이전트 스킬 보기](https://github.com/adobe/skills/tree/main/plugins/adobe-cja)

>[!TAB Adobe App Builder]

Adobe App Builder을 사용하여 맞춤형 애플리케이션을 스캐폴딩, 테스트 및 배포하는 에이전트 기술입니다.

[에이전트 스킬 보기](https://github.com/adobe/skills/tree/main/plugins/app-builder)

>[!TAB Creative Cloud]

Creative Cloud을 사용한 일괄 사진 편집, 템플릿에서의 디자인, 비디오 편집 및 소셜 미디어 변형을 위한 에이전트 기술.

[에이전트 스킬 보기](https://github.com/adobe/skills/tree/main/plugins/creative-cloud)

>[!ENDTABS]

## 에이전트 스킬 추가

![에이전트 기술 작동 방식](../assets/hero-connect-agent-skills.gif)

에이전트 스킬은 Adobe 에이전트 도구를 사용하여 작업을 완료하는 방법을 AI 에이전트에게 알려 주는 지침 세트입니다. 에이전트가 스킬을 로드할 때, 즉흥적으로 처리하지 않고 해당 워크플로우를 따릅니다.

### 에이전트 스킬 설치

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

## 에이전트 작업 기술

에이전트 스킬은 Adobe 도메인 전문 지식을 AI 클라이언트 내에서 작동하도록 만들어 에이전트가 즉흥적이지 않고 입증된 워크플로우를 따릅니다. 아래 각 연습에서는 시작부터 출력까지 Adobe 모범 사례에 따라 안정적으로 완료된 특정 비즈니스 작업을 보여 줍니다.

<!--
CARDS

* https://experienceleague.adobe.com/ko/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development
  {title = Develop AEM components with AI}
  {description = Use Claude Code or Cursor with Agent Skills to scaffold, code, and refine AEM components guided by Adobe best practices.}
  {cta = Try with Agent Skills}
  {image = ../assets/agent-skills-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Develop AEM components with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/ko/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" title="AI를 사용하여 AEM 구성 요소 개발" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="AI를 사용하여 AEM 구성 요소 개발"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/ko/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" title="AI를 사용하여 AEM 구성 요소 개발">AI를 사용하여 AEM 구성 요소 개발</a>
                    </p>
                    <p class="is-size-6">에이전트 기술과 함께 클라우드 코드 또는 커서를 사용하여 Adobe 모범 사례에 따라 AEM 구성 요소를 스캐폴드, 코드 및 세분화합니다.</p>
                </div>
                <a href="https://experienceleague.adobe.com/ko/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">에이전트 기술을 사용해 보세요</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
