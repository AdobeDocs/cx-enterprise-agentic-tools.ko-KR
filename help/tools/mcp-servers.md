---
title: MCP 서버
description: Model Context Protocol 서버를 사용하여 MCP 호환 AI 클라이언트를 Adobe CX Enterprise 워크플로우에 연결합니다.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 2%

---


# MCP 서버

<!-- last-modified: 2026-05-19 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

Adobe CX Enterprise MCP 서버는 호환되는 AI 클라이언트를 Adobe 데이터 및 워크플로에 직접 제어하고 액세스할 수 있도록 합니다. 한 번 연결하면 AI 환경을 종료하지 않고도 일반 언어로 캠페인 성과를 쿼리하고, 대상을 활성화하고, 여정을 검토하고, 콘텐츠를 관리하는 등의 작업을 수행할 수 있습니다. MCP 서버는 AI 클라이언트와 Adobe의 기본 시스템 사이에 위치하기 때문에 조직의 액세스 제어 및 데이터 거버넌스가 유효한 동안 자연어 유연성을 얻을 수 있습니다.

Adobe MCP 서버는 개방형 모델 컨텍스트 프로토콜 표준을 따릅니다. 모든 MCP 호환 AI 클라이언트는 모든 Adobe MCP 서버에 연결합니다.

## CX 엔터프라이즈 MCP 게이트웨이

![CX 엔터프라이즈 MCP 게이트웨이는 AI 클라이언트를 전체 Adobe CX 엔터프라이즈 제품군의 MCP 도구에 연결합니다](../assets/mcp-gateway-hero.gif)

**끝점 한 개. 모든 Adobe CX 엔터프라이즈 MCP 서버.**

CX 엔터프라이즈 게이트웨이는 AI 클라이언트를 각 애플리케이션에 대한 별도의 연결 없이 분석, 캠페인, 콘텐츠 및 데이터 전반에 걸쳐 도구로 라우팅합니다. 한 번 연결하면 게이트웨이가 Adobe 권한에 따라 조직에 라이선스가 부여된 도구만 표시합니다.

>[!BEGINTABS]

>[!TAB CX 엔터프라이즈 애플리케이션]

각 애플리케이션의 도구는 조직의 Adobe 라이센스를 기반으로 사용할 수 있습니다.

| 애플리케이션 | 수행 가능한 작업 |
| --- | --- |
| Adobe Journey Optimizer | [여정, 캠페인 및 채널 구성 검토](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) |
| Customer Journey Analytics | [보고서 쿼리, 데이터 보기 검색, 작성 작업 공간](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) |
| Real-Time CDP | [대상, 활성화 상태 및 데이터 흐름 상태 확인](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp)&#x200B;(비공개 베타) |

>[!TAB 연결]

애플리케이션별 MCP 엔드포인트를 사용할 때마다 CX 엔터프라이즈 게이트웨이 엔드포인트를 사용하십시오.

```
https://cx-enterprise.adobe.io/mcp
```

>[!NOTE]
>AEM의 경우 직접 AEM 엔드포인트 사용 - AEM은 CX 엔터프라이즈 MCP 게이트웨이를 통해 라우팅되지 않습니다.

메시지가 표시되면 Adobe ID에 로그인하고 Adobe 애플리케이션에 연결된 IMS 조직을 선택합니다. 잘못된 조직을 선택하는 것은 누락된 도구 또는 인증 오류의 가장 일반적인 원인입니다.

전체 설치 지침은 아래의 [AI 클라이언트에 연결](#connect-to-your-ai-client)을 참조하십시오.

>[!ENDTABS]

## Adobe CX 엔터프라이즈 MCP 서버

아래 나열된 서버는 직접 접속되며 CX 엔터프라이즈 MCP 게이트웨이를 통해 라우팅되지 않습니다. AJO, Customer Journey Analytics 및 Real-Time CDP 액세스의 경우 위의 [CX 엔터프라이즈 MCP 게이트웨이](#cx-enterprise-mcp-gateway)를 사용하십시오.

<!--
CARDS

* #cx-enterprise-mcp-gateway
  {title = CX Enterprise MCP Gateway}
  {description = One connection to AJO, CJA, and Real-Time CDP tools. The gateway surfaces only the tools your organization is licensed for.}
  {cta = Connect}
  {image = ../assets/mcp-cxenterprise-card.png}

* https://developer.adobe.com/analytics-mcp/docs/aa/
  {title = Adobe Analytics}
  {description = Tools for report suite discovery, dimension and metric analysis, segment authoring, and workspace creation in Adobe Analytics.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-analytics-card.png}

* https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service
  {title = AEM Content}
  {description = Tools for managing pages, content fragments, assets, and launches in Adobe Experience Manager as a Cloud Service using natural language.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service
  {title = AEM Content (Read-Only)}
  {description = Tools for discovering and querying pages, content fragments, and launches in AEM as a Cloud Service. No write access.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://experienceleague.adobe.com/ko/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager
  {title = AEM Cloud Manager}
  {description = Tools for managing Cloud Manager programs, environments, pipelines, and repositories from your IDE using natural language.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

-->

### MCP 서버 엔드포인트

| 서버 | 엔드포인트 | 도구 |
| --- | --- | --- |
| [CX 엔터프라이즈 MCP 게이트웨이](#cx-enterprise-mcp-gateway) | `https://cx-enterprise.adobe.io/mcp` | · [Adobe Journey Optimizer 도구](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server)<br>· [Customer Journey Analytics 도구](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp)<br>· [Real-Time CDP 도구](https://experienceleague.adobe.com/ko/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) |
| [Adobe Analytics](https://developer.adobe.com/analytics-mcp/docs/aa/) | `https://aa-mcp.adobe.io/mcp` | [도구 보기](https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp) |
| [AEM Cloud Manager](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | [도구 보기](https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp) |
| [AEM 컨텐츠](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | [도구 보기](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) |
| [AEM 컨텐츠(읽기 전용)](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | [도구 보기](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly) |

## AI 클라이언트에 연결

모든 Adobe MCP 서버는 IMS(Adobe Identity Management Service)와 함께 OAuth를 사용합니다. 메시지가 표시되면 올바른 IMS 조직을 선택합니다. 잘못된 것을 선택하는 것이 인증 오류의 가장 일반적인 원인입니다.

수동으로 구성하기 전에 [Adobe AI 레지스트리](https://developer.adobe.com/ai-registry/?type=connector)에서 AI 클라이언트 및 Adobe 응용 프로그램에 대한 관리되는 커넥터를 확인하십시오. 관리되는 커넥터는 인증을 자동으로 처리합니다. 클라이언트와 애플리케이션에 커넥터를 사용할 수 있는 경우 아래 수동 단계 대신 커넥터를 사용하십시오.

![Adobe MCP 서버에 연결하는 AI 에이전트](../assets/hero-connect-mcp-servers.gif)

>[!BEGINTABS]

>[!TAB 클라우드.ai]

### ![권장](../assets/badge-recommended.svg) 관리되는 커넥터 사용

[Adobe AI 레지스트리](https://developer.adobe.com/ai-registry/?type=connector)&#x200B;(으)로 이동하여 Adobe 응용 프로그램을 검색합니다. 클라우드 커넥터(예: [Adobe Experience Manager 커넥터](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector))가 나열되면 아래 단계 대신 해당 설정 지침을 따르십시오.

### 사용자 지정 커넥터를 사용하여 연결

Claude.ai는 계정 설정에서 사용자 지정 커넥터를 통해 원격 MCP 서버를 지원합니다.

1. **설정 > 통합**(으)로 이동합니다.
2. **사용자 지정 커넥터 추가**&#x200B;를 클릭합니다.
3. `https://cx-enterprise.adobe.io/mcp`을(를) URL로 입력하고 표시 이름을 `Adobe CX Enterprise`과(와) 같이 입력합니다.
4. **연결**&#x200B;을 클릭하고 Adobe ID으로 로그인합니다. 올바른 IMS 조직을 선택합니다.

전체 설정: [Claude.ai 사용자 지정 커넥터 설명서](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB 클라우드 코드]

### CLI 사용

`claude mcp add`을(를) 실행하여 CX 엔터프라이즈 MCP 게이트웨이를 등록합니다. 하나의 연결을 통해 조직의 라이선스를 기반으로 AJO, CJA 및 Real-Time CDP 도구에 액세스할 수 있습니다.

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### 설정 파일 편집

프로젝트 루트(프로젝트 수준)의 `~/.claude.json`(전역) 또는 `.mcp.json`에 서버 추가:

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

CX 엔터프라이즈 MCP 게이트웨이를 커서 `mcp.json` 구성 파일에 추가한 다음 **설정 > MCP**&#x200B;를 통해 연결합니다.

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

게이트웨이 항목 하나를 사용하면 조직의 라이선스에 따라 AJO, CJA 및 Real-Time CDP에 액세스할 수 있습니다.

추가되면 MCP 서버가 커서 설정의 **설치된 MCP 서버** 아래에 나타납니다. **인증 필요**&#x200B;를 표시하는 서버 옆의 **연결**&#x200B;을 선택하고 Adobe ID으로 로그인합니다. 애플리케이션에 대한 액세스 권한이 있는 IMS 조직을 선택합니다.

![설치된 Adobe MCP 서버 및 mcp.json을 표시하는 커서 MCP 서버 구성](../assets/screenshots/cursor-mcp-server-configuration.jpg)

전체 설정: [커서 MCP 설명서](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### ![권장](../assets/badge-recommended.svg) 관리되는 커넥터 사용

[Adobe AI 레지스트리](https://developer.adobe.com/ai-registry/?type=connector)&#x200B;(으)로 이동하여 Adobe 응용 프로그램을 검색합니다. ChatGPT 커넥터가 나열되면 아래 단계 대신 설정 지침을 따르십시오.

### 원격 MCP 서버를 사용하여 연결

ChatGPT는 Pro, Plus, Business, Enterprise 및 Education 플랜에서 사용할 수 있는 [개발자 모드](https://developers.openai.com/api/docs/guides/developer-mode)를 통해 원격 MCP 서버를 지원합니다.

1. **ChatGPT 설정**&#x200B;에서 개발자 모드를 사용하도록 설정합니다.
2. **설정 > 통합**(으)로 이동합니다.
3. **사용자 지정 커넥터 추가**&#x200B;를 클릭하고 **원격 MCP 서버**&#x200B;를 선택합니다.
4. URL로 `https://cx-enterprise.adobe.io/mcp`을(를) 입력하고 이름으로 `Adobe CX Enterprise`을(를) 입력합니다.
5. 인증을 **OAuth**(으)로 설정합니다.
6. **연결**&#x200B;을 클릭하고 Adobe ID으로 로그인합니다. 올바른 IMS 조직을 선택합니다.

전체 설정: [ChatGPT MCP 설명서](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB OpenAI 코드 CLI]

OpenAI Codex CLI는 TOML 구성을 통해 원격 MCP 서버를 지원합니다.

**구성 파일 위치:**

- **사용자 수준(모든 프로젝트):** `~/.codex/config.toml`
- 프로젝트 루트의 **프로젝트 범위:** `.codex/config.toml`

CX 엔터프라이즈 MCP 게이트웨이 추가:

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
4. MCP 온보딩 마법사에서 다음을 입력합니다.
   - **서버 이름:** `Adobe CX Enterprise`
   - **서버 URL:** `https://cx-enterprise.adobe.io/mcp`
5. 인증을 **OAuth 2.0**(으)로 설정하고 Adobe IMS 인증 및 토큰 URL로 구성합니다.
6. **만들기**&#x200B;를 선택한 다음 **에이전트에 추가**&#x200B;를 선택합니다.

>[!NOTE]
>
>Copilot Studio의 MCP 서버 연결은 Power Platform을 통과합니다. 조직의 DLP(데이터 손실 방지) 정책이 적용됩니다.

전체 설정: [Copilot Studio MCP 설명서](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## 문제 해결

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

## 실행 중인 무생식 도구

실제 비즈니스 워크플로우에 적용되는 Adobe CX Enterprise MCP 서버를 참조하십시오.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use the CX Enterprise MCP Gateway to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use the CX Enterprise MCP Gateway to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use the CX Enterprise MCP Gateway to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine the CX Enterprise MCP Gateway and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* ../use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Use the CX Enterprise MCP Gateway for a unified view of AJO, CJA, and Real-Time CDP campaign health in one AI session.}
  {cta = Start walkthrough}
-->
