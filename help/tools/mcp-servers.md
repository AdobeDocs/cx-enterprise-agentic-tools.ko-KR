---
title: MCP 서버
description: Model Context Protocol 서버를 사용하여 MCP 호환 AI 클라이언트를 Adobe CX Enterprise 워크플로우에 연결합니다.
last-substantial-update: 2026-06-17T00:00:00Z
source-git-commit: 49e3c0cdb77cca3ff39f3aea591cc0fe8d4be4c9
workflow-type: tm+mt
source-wordcount: '2404'
ht-degree: 6%

---


# MCP 서버

<!-- last-modified: 2026-06-11 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

Adobe CX Enterprise MCP 서버는 호환되는 AI 클라이언트를 Adobe 데이터 및 워크플로에 직접 제어하고 액세스할 수 있도록 합니다. 한 번 연결하면 AI 환경을 종료하지 않고도 일반 언어로 캠페인 성과를 쿼리하고, 대상을 활성화하고, 여정을 검토하고, 콘텐츠를 관리하는 등의 작업을 수행할 수 있습니다. MCP 서버는 AI 클라이언트와 Adobe의 기본 시스템 사이에 위치하기 때문에 조직의 액세스 제어 및 데이터 거버넌스가 유효한 동안 자연어 유연성을 얻을 수 있습니다.

Adobe MCP 서버는 개방형 [모델 컨텍스트 프로토콜](https://modelcontextprotocol.io/docs/getting-started/intro) 표준을 따릅니다. 모든 MCP 호환 AI 클라이언트는 모든 Adobe MCP 서버에 연결합니다.

## CX Enterprise MCP 서버 {#cx-enterprise-mcp-servers}

>[!CONTEXTUALHELP]
>id="cx-enterprise-agentic-tools_mcp_servers_cx-enterprise"
>title="CX Enterprise MCP"
>abstract="단일 MCP 엔드포인트를 통해 액세스할 수 있는 CX Enterprise 애플리케이션입니다. AI 클라이언트에서 일반 언어로 질문하고, 분석하고, 조치를 취할 수 있습니다."
>additional-url="https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/mcp/overview" text="CX Enterprise MCP 설명서"

![CX 엔터프라이즈 MCP는 AI 클라이언트를 전체 Adobe CX 엔터프라이즈 제품군 내의 도구에 연결합니다](../assets/mcp-gateway-hero.gif)

끝점과 기능을 볼 응용 프로그램을 선택하십시오.

>[!BEGINTABS]

>[!TAB CX 엔터프라이즈 MCP]

**끝점 한 개. 여러 CX 엔터프라이즈 응용 프로그램입니다.**

한 번 연결하면 AI 클라이언트가 조직의 라이센스를 기반으로 CX 엔터프라이즈 애플리케이션에 액세스할 수 있습니다. 조직을 활성화하려면 [adobecxmcp@adobe.com](mailto:adobecxmcp@adobe.com)에 전자 메일을 보내 액세스를 요청하세요.

```
https://cx-enterprise.adobe.io/mcp
```

| CX 엔터프라이즈 애플리케이션 | 수행 가능한 작업 | 추가 권한 필요 |
| --- | --- | --- |
| [Adobe Analytics](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/analytics-mcp) | 보고서 세트 검색, 세그먼트 작성 및 작업 영역 만들기 | 아니오 |
| Campaign Classic | Campaign 인스턴스 검색, 스키마 찾아보기, 쿼리 실행, 워크플로우 제어 및 SOAP/JS 실행 | 예 |
| [Adobe Experience Platform](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/aep-mcp) | 데이터 세트 검색, 스키마 검색 및 샌드박스 관리 | 아니오 |
| 실험 | A/B, MVT 및 MAB 실험 보고, 지표, 통찰력, 기회 및 샘플 크기 계획 | 아니오 |
| GenStudio for Performance Marketing | 광고 성능 데이터 및 크리에이티브 인사이트 액세스 | 예 |
| [Adobe Journey Optimizer](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/ajo-mcp) | 여정, 캠페인 및 채널 구성 검토 | 아니오 |
| Adobe Journey Optimizer B2B edition | B2B 여정, 계정 프로그램, 구매 그룹 및 개인화 관리 | 아니오 |
| [Adobe Target](https://experienceleague.adobe.com/ko/docs/target/using/mcp/target-mcp) | 활동, 오퍼, 대상, mbox, 성능 보고서 및 미리보기 URL 검토 | [예](https://experienceleague.adobe.com/ko/docs/target/using/mcp/target-mcp-get-started#mcp-security) |
| [Customer Journey Analytics](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/cja-mcp) | 보고서 쿼리, 데이터 보기 검색 및 작업 공간 작성 | 아니오 |
| [Marketo Engage](https://experienceleague.adobe.com/ko/docs/marketo-developer/marketo/mcp-server) | 프로그램, 캠페인, 리드, 스마트 목록, 이메일 및 양식 관리 | [예](https://experienceleague.adobe.com/ko/docs/marketo-developer/marketo/mcp-server#get-marketo-credentials) |
| [Real-Time CDP](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/rtcdp-mcp) | 대상자 활성화 상태, 대상 상태 및 데이터 흐름 상태 확인 | 아니오 |

전체 설명서는 [CX 엔터프라이즈 MCP](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/mcp/overview)를 참조하십시오.

>[!NOTE]
>
>각 CX 엔터프라이즈 애플리케이션에 대한 액세스는 조직의 권한 및 Adobe Admin Console에서의 사용자 권한을 기반으로 합니다. 조직에 CX Enterprise MCP를 사용하려면 [adobecxmcp@adobe.com](mailto:adobecxmcp@adobe.com)에 전자 메일을 보내십시오.

>[!TAB Experience Manager]

Adobe Experience Manager에는 다양한 워크플로우에 대한 여러 MCP 서버가 있습니다.

| MCP 서버 | 엔드포인트 | 수행 가능한 작업 |
| --- | --- | --- |
| [AEM Cloud Manager](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | 프로그램, 환경, 파이프라인 및 저장소 관리 |
| [AEM 컨텐츠](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | 페이지, 콘텐츠 조각, 에셋 및 론치 관리 |
| [AEM 컨텐츠(읽기 전용)](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | 쓰기 액세스 권한 없이 페이지, 콘텐츠 조각 및 시작 검색 및 쿼리 |
| [AEM Experience Governance](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/cloud-service/ai/mcp-servers/experience-governance-mcp-server) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-governance` | 브랜드 가이드라인 및 규정 준수 규칙에 따라 컨텐츠 및 이미지 평가 |

>[!NOTE]
>
>각 AEM 환경에 대한 액세스는 조직의 AEM Cloud Service 권한 및 해당 환경에서의 사용자 권한에 따라 다릅니다.

>[!TAB Experience Platform]

| MCP 서버 | 엔드포인트 | 수행 가능한 작업 |
| --- | --- | --- |
| Adobe Marketing Agent | `https://aep-ai-ama.adobe.io/mcp` | AEP 애플리케이션 전반에 걸쳐 대상 분석, AEP 진단 및 AJO B2B 여정 구축 통합 |

>[!NOTE]
>
>액세스는 조직의 Adobe Experience Platform 권한 및 사용자의 권한에 따라 다릅니다.

>[!TAB Target]

Adobe Target MCP는 공개 베타 버전입니다. 현재 사용 가능한 모든 도구는 읽기 전용입니다. 쓰기 툴은 일반 공급 예정

| MCP 서버 | 엔드포인트 | 수행 가능한 작업 |
| --- | --- | --- |
| [Adobe Target](https://experienceleague.adobe.com/ko/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | 활동, 오퍼, 대상, mbox, 성능 보고서 및 미리보기 URL 검토 |

>[!NOTE]
>
>액세스는 Adobe Target 권한 및 사용자의 권한에 따라 다릅니다.

>[!TAB Workfront]

| MCP 서버 | 엔드포인트 | 수행 가능한 작업 |
| --- | --- | --- |
| [Adobe Workfront](https://experienceleague.adobe.com/ko/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview) | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | 작업, 프로젝트, 계획 기록, 통찰력 및 콘텐츠 승인 관리 |

>[!NOTE]
>
>액세스는 Adobe Workfront 라이선스와 사용자의 권한에 따라 다릅니다.

>[!ENDTABS]

## AI 클라이언트에 연결

대부분의 Adobe MCP 서버는 IMS(Adobe Identity Management Service)와 함께 OAuth를 사용합니다. 메시지가 표시되면 올바른 IMS 조직을 선택합니다. 잘못된 것을 선택하는 것이 인증 오류의 가장 일반적인 원인입니다.

![Adobe MCP 서버에 연결하는 AI 에이전트](../assets/hero-connect-mcp-servers.gif)

아래 단계에서는 CX 엔터프라이즈 MCP 엔드포인트를 예로 사용합니다. 동일한 프로세스가 모든 Adobe MCP 서버에 적용됩니다. 연결하려는 서버의 끝점 URL에서 교체합니다.

>[!BEGINTABS]

>[!TAB 클라우드.ai]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="권장"> 관리되는 커넥터 사용

[Adobe AI 레지스트리](https://developer.adobe.com/ai-registry/?type=connector)&#x200B;(으)로 이동하여 Adobe 응용 프로그램을 검색합니다. 클라우드 커넥터(예: [Adobe Experience Manager 커넥터](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector))가 나열되면 아래 단계 대신 해당 설정 지침을 따르십시오.

### 사용자 지정 커넥터를 사용하여 연결

Claude.ai는 계정 설정에서 사용자 지정 커넥터를 통해 원격 MCP 서버를 지원합니다.

1. **설정 > 통합**(으)로 이동합니다.
2. **사용자 지정 커넥터 추가**&#x200B;를 클릭합니다.
3. 서버 엔드포인트를 URL(예: CX Enterprise MCP의 경우 `https://cx-enterprise.adobe.io/mcp`)로 입력하고 선택한 표시 이름을 입력합니다.
4. **연결**&#x200B;을 클릭하고 Adobe ID으로 로그인합니다. 올바른 IMS 조직을 선택합니다.

전체 설정: [Claude.ai 사용자 지정 커넥터 설명서](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB 클라우드 코드]

### CLI 사용

`claude mcp add`을(를) 실행하여 Adobe MCP 서버를 등록합니다. 서버 이름과 URL을 연결할 서버의 값으로 바꿉니다. 이 예에서는 CX 엔터프라이즈 MCP 를 사용합니다.

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### 설정 파일 편집

프로젝트 루트(프로젝트 수준)의 `~/.claude.json`(전역) 또는 `.mcp.json`에 서버를 추가합니다. 키와 URL을 연결할 서버의 값으로 바꿉니다.

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

Adobe MCP 서버는 OAuth를 사용합니다. 도구를 처음 호출할 때 Adobe ID으로 인증하라는 메시지가 클라우드 코드에 표시됩니다. 메시지가 표시되면 올바른 IMS 조직을 선택합니다.

전체 설정: [코드 MCP 설명서 빌드](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB 커서]

Adobe MCP 서버를 커서 `mcp.json` 구성 파일에 추가한 다음 **설정 > MCP**&#x200B;를 통해 연결합니다. 키와 URL을 연결할 서버의 값으로 바꿉니다. 이 예에서는 CX 엔터프라이즈 MCP 를 사용합니다.

- **전역(모든 프로젝트):** `~/.cursor/mcp.json`
- 프로젝트 루트의 **프로젝트 수준:** `.cursor/mcp.json`

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

추가되면 MCP 서버가 커서 설정의 **설치된 MCP 서버** 아래에 나타납니다. **인증 필요**&#x200B;를 표시하는 서버 옆의 **연결**&#x200B;을 선택하고 Adobe ID으로 로그인합니다. 애플리케이션에 대한 액세스 권한이 있는 IMS 조직을 선택합니다.

![설치된 Adobe MCP 서버 및 mcp.json을 표시하는 커서 MCP 서버 구성](../assets/screenshots/cursor-mcp-server-configuration.jpg)

전체 설정: [커서 MCP 설명서](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="권장"> 관리되는 커넥터 사용

[Adobe AI 레지스트리](https://developer.adobe.com/ai-registry/?type=connector)&#x200B;(으)로 이동하여 Adobe 응용 프로그램을 검색합니다. ChatGPT 커넥터가 나열되면 아래 단계 대신 설정 지침을 따르십시오.

### 원격 MCP 서버를 사용하여 연결

ChatGPT는 Pro, Plus, Business, Enterprise 및 Education 플랜에서 사용할 수 있는 [개발자 모드](https://developers.openai.com/api/docs/guides/developer-mode)를 통해 원격 MCP 서버를 지원합니다.

1. **ChatGPT 설정**&#x200B;에서 개발자 모드를 사용하도록 설정합니다.
2. **설정 > 통합**(으)로 이동합니다.
3. **사용자 지정 커넥터 추가**&#x200B;를 클릭하고 **원격 MCP 서버**&#x200B;를 선택합니다.
4. 서버 엔드포인트를 URL(예: CX Enterprise MCP의 경우 `https://cx-enterprise.adobe.io/mcp`)로 입력하고 선택한 표시 이름을 입력합니다.
5. 인증을 **OAuth**(으)로 설정합니다.
6. **연결**&#x200B;을 클릭하고 Adobe ID으로 로그인합니다. 올바른 IMS 조직을 선택합니다.

전체 설정: [ChatGPT MCP 설명서](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB OpenAI 코드 CLI]

OpenAI Codex CLI는 TOML 구성을 통해 원격 MCP 서버를 지원합니다.

**구성 파일 위치:**

- **사용자 수준(모든 프로젝트):** `~/.codex/config.toml`
- 프로젝트 루트의 **프로젝트 범위:** `.codex/config.toml`

섹션 이름과 URL을 연결할 서버의 값으로 바꿉니다. 이 예에서는 CX 엔터프라이즈 MCP 를 사용합니다.

```toml
[mcp_servers.adobe-cx-enterprise]
url = "https://cx-enterprise.adobe.io/mcp"
enabled = true
```

Adobe MCP 서버는 OAuth를 사용합니다. Codex CLI는 처음 사용할 때 OAuth 플로우를 자동으로 처리합니다. 메시지가 표시되면 올바른 IMS 조직을 선택합니다.

전체 설정: [OpenAI Codex CLI MCP 설명서](https://developers.openai.com/codex/mcp)

>[!TAB Copilot Studio]

Microsoft Copilot Studio는 자동으로 Power Platform 사용자 지정 커넥터를 만드는 MCP 온보딩 마법사를 사용하여 원격 MCP 서버에 연결합니다.

1. Copilot Studio에서 에이전트를 엽니다.
2. **도구** 페이지로 이동합니다.
3. **도구 추가 > 새 도구 > 모델 컨텍스트 프로토콜**&#x200B;을 선택합니다.
4. MCP 온보딩 마법사에서 서버 세부 사항을 입력합니다. 예를 들어 CX 엔터프라이즈 MCP 의 경우:
   - **서버 이름:** `Adobe CX Enterprise`
   - **서버 URL:** `https://cx-enterprise.adobe.io/mcp`
5. 인증을 **OAuth 2.0**(으)로 설정하고 Adobe IMS 인증 및 토큰 URL로 구성합니다.
6. **만들기**&#x200B;를 선택한 다음 **에이전트에 추가**&#x200B;를 선택합니다.

>[!NOTE]
>
>Copilot Studio의 MCP 서버 연결은 Power Platform을 통과합니다. 조직의 DLP(데이터 손실 방지) 정책이 적용됩니다.

전체 설정: [Copilot Studio MCP 설명서](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## MCP 서버 작동 중

Adobe CX Enterprise MCP 서버가 실제 비즈니스 문제를 해결하는지 확인하십시오. 각 연습에서는 진정한 운영 과제에서 시작하여 AI 클라이언트가 도구를 전환하거나 코드를 작성하지 않고 일반 언어로 해결하는 방법을 보여 줍니다.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Campaign insights without reports}
  {description = Ask performance questions in plain language and get answers from Customer Journey Analytics, without building a single report.}
  {cta = Surface campaign insights}

* ../use-cases/query-audiences.md
  {title = Audience activation at a glance}
  {description = See which audiences are live, where they are flowing, and whether destinations are healthy, without navigating Real-Time CDP.}
  {cta = Check audience activation}

* ../use-cases/manage-ajo-journeys.md
  {title = Catch journey issues early}
  {description = Monitor active journeys and surface operational issues before they reach your audience.}
  {cta = Monitor your journeys}

* ../use-cases/manage-aem-content.md
  {title = Ship content updates faster}
  {description = Find, update, and publish AEM pages and content fragments faster, without switching to the AEM interface.}
  {cta = Ship content faster}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Close content performance gaps}
  {description = Surface conversion gaps in CJA, trace them to underperforming content in AEM, and apply the fix in a single AI session.}
  {cta = Close performance gaps}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Campaign insights without reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="보고서가 없는 Campaign 인사이트">
                        <img class="is-bordered-r-small" src="../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="보고서가 없는 Campaign 인사이트"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" title="보고서가 없는 Campaign 인사이트">보고서가 없는 캠페인 인사이트</a>
                    </p>
                    <p class="is-size-6">단일 보고서를 작성하지 않고도 일반 언어로 성능 질문에 답변하고 Customer Journey Analytics에서 답변을 얻을 수 있습니다.</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Surface Campaign 인사이트</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Audience activation at a glance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="대상 활성화 개요">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="대상 활성화 개요"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" title="대상 활성화 개요">대상자 활성화 개요</a>
                    </p>
                    <p class="is-size-6">Real-Time CDP을 탐색하지 않고도 라이브 대상, 전달 위치 및 대상의 상태 여부를 확인할 수 있습니다.</p>
                </div>
                <a href="../use-cases/query-audiences.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">대상 활성화 확인</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Catch journey issues early">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="여정 문제를 조기에 파악">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png" alt="여정 문제를 조기에 파악"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" title="여정 문제를 조기에 파악">여정 문제를 조기에 발견</a>
                    </p>
                    <p class="is-size-6">대상자에게 도달하기 전에 활성 여정 및 표면 운영 문제를 모니터링합니다.</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">여정 모니터링</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Ship content updates faster">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="더 빠른 콘텐츠 업데이트 배송">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="더 빠른 콘텐츠 업데이트 배송"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" title="더 빠른 콘텐츠 업데이트 배송">콘텐츠 업데이트 더 빨리 보내기</a>
                    </p>
                    <p class="is-size-6">AEM 인터페이스로 전환하지 않고도 AEM 페이지 및 컨텐츠 조각을 보다 빠르게 찾고, 업데이트하고, 게시할 수 있습니다.</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">더 빠르게 콘텐츠 배송</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Close content performance gaps">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="컨텐츠 성능 차이 해결">
                        <img class="is-bordered-r-small" src="../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png" alt="컨텐츠 성능 차이 해결"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" title="컨텐츠 성능 차이 해결">컨텐츠 성능 차이 닫기</a>
                    </p>
                    <p class="is-size-6">CJA에서 전환 격차를 노출하고, 이를 AEM에서 성과가 낮은 콘텐츠로 추적한 다음 단일 AI 세션에서 이 수정 사항을 적용합니다.</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">성능 차이 닫기</span>
                
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## 도움이 더 필요하십니까?

MCP 연결에는 인증, 조직 선택 및 애플리케이션 수준 권한이 포함됩니다. 어떤 것이 예상대로 작동하지 않는 경우 이러한 단계는 가장 일반적인 원인을 다룹니다.

+++Adobe 조직 전환

Adobe 사용자가 여러 IMS 조직에 속해 있고 잘못된 도구 또는 데이터가 표시되는 경우 MCP 서버를 연결 해제하고 브라우저에서 Adobe 세션에서 로그아웃한 다음 다시 연결합니다. 로그인하는 동안 조직을 선택하라는 메시지가 표시됩니다.

Adobe CX Enterprise MCP 서버는 사용자 계정이 둘 이상에 액세스할 수 있는 경우에도 한 번에 하나의 IMS 조직에만 인증할 수 있습니다.

+++

+++샌드박스, 보고서 세트, 환경 또는 기타 세션 리소스 지정

일부 Adobe CX Enterprise MCP 서버에서는 결과를 반환하기 전에 리소스를 지정해야 합니다. 애플리케이션에 따라 샌드박스, 프로그램, 환경, 보고서 세트 또는 데이터 보기일 수 있습니다.

액세스 권한이 있는 리소스를 잘 모를 경우 AI 클라이언트에 문의하십시오. 예: &quot;사용 가능한 샌드박스를 나열합니다.&quot; 또는 &quot;액세스 권한이 있는 보고서 세트는 무엇입니까?&quot; Adobe CX Enterprise MCP 서버는 종종 사용자가 사용할 수 있는 전체 리소스 목록을 반환할 수 있습니다.

세션 리소스가 설정되면 언제든지 AI 클라이언트에게 어떤 리소스를 사용할지 알려 전환할 수 있습니다.

+++

+++권한 및 액세스 오류

AI 클라이언트는 OAuth를 사용하여 Adobe 사용자 계정을 대행합니다. Adobe 애플리케이션에 로그인할 때 적용되는 동일한 권한 및 액세스 제어 기능은 MCP 서버를 사용할 때에도 적용됩니다.

작업이 실패하거나 결과를 반환하지 않는 경우 사용자에게 Adobe Admin Console 및 관련 CX 엔터프라이즈 애플리케이션에서 필요한 권한이 있는지 확인하십시오. 액세스 조정이 필요한 경우 Adobe 시스템 관리자에게 문의하십시오.

+++

+++세션이 손실된 후 다시 인증

Adobe CX Enterprise MCP 서버는 OAuth를 사용하여 Adobe 사용자 계정을 인증합니다. 인증 상태가 손실되면 다시 인증할 때까지 추가 도구 호출이 성공하지 못합니다.

재인증: AI 클라이언트의 MCP 서버 구성을 열고 Adobe CX 엔터프라이즈 MCP 서버 항목을 선택한 다음 다시 연결합니다. Adobe ID으로 다시 로그인하라는 메시지가 표시됩니다.

+++
