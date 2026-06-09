---
title: 빌더용 API
description: Adobe CX Enterprise API를 사용하여 맞춤형 애플리케이션 및 통합을 구축할 수 있습니다.
last-substantial-update: 2026-06-02T00:00:00Z
index: false
source-git-commit: a130fc470e97f2316e2ea72ebda47b9fc4ad9b33
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 11%

---


# 빌더용 API

<!-- last-modified: 2026-06-02 -->

![Adobe CX Enterprise API](../assets/hero-apis.png)

Adobe CX Enterprise API를 사용하면 개발자와 AI 지원 코딩 에이전트 툴이 Adobe 데이터 및 워크플로우에 직접 액세스할 수 있습니다. 이를 사용하여 사용자 정의 애플리케이션을 구축하고, 통합을 자동화하고, Adobe 기능을 자체 시스템에 임베드할 수 있습니다. API는 시스템 통합에 대한 완전한 프로그래밍 방식 제어가 필요하거나 Adobe 데이터 위에 애플리케이션을 구축하는 경우 올바른 선택입니다. Adobe 워크플로에 대한 에이전트 기반 대화 액세스는 [MCP 서버](mcp-servers.md)를 참조하십시오.

## Adobe CX 엔터프라이즈 API

>[!BEGINTABS]

>[!TAB Adobe Analytics]

보고, 데이터 피드, 계산된 지표 및 세그먼트 관리.

[API 탐색](https://developer.adobe.com/analytics-apis/docs/2.0/)

>[!TAB Adobe Commerce]

카탈로그, 장바구니, 주문, 고객 및 프로모션을 위한 REST 및 GraphQL API입니다.

[API 탐색](https://developer.adobe.com/commerce/webapi/)

>[!TAB Adobe Experience Platform]

데이터 세트, 스키마, 프로필, ID, 쿼리 및 세그멘테이션에 대한 CRUD 작업입니다.

[API 탐색](https://developer.adobe.com/experience-platform-apis/)

>[!TAB Adobe Journey Optimizer]

여정 오케스트레이션, 캠페인 관리, 콘텐츠 템플릿 및 Offer Decisioning

[API 탐색](https://developer.adobe.com/journey-optimizer-apis/)

>[!TAB AEM as a Cloud Service]

Adobe Experience Manager용 컨텐츠, 자산 및 워크플로우 관리 API.

[API 탐색](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions)

>[!TAB Audience Manager]

대상자 관리 및 활성화 워크플로.

[API 탐색](https://developer.adobe.com/audience-manager/)

>[!TAB 클라이언트 SDK]

Mobile SDK, Edge SDK 및 인앱 메시지.

[API 탐색](https://developer.adobe.com/client-sdks/home/)

>[!TAB Customer Journey Analytics]

Analytics 데이터 액세스, 보고 및 CJA 통찰력 워크플로우입니다.

[API 탐색](https://developer.adobe.com/cja-apis/docs/)

>[!TAB 데이터 수집]

Edge Network 데이터 수집, 실시간 이벤트 수집 및 스트리밍 데이터 전달.

[API 탐색](https://developer.adobe.com/data-collection-apis/docs/)

>[!TAB Developer Console]

API 프로젝트 설정, 인증 및 자격 증명 관리.

[API 탐색](https://developer.adobe.com/developer-console/docs/guides/)

>[!TAB 이벤트]

이벤트 기반 통합, 웹후크 및 자동화 트리거.

[API 탐색](https://developer.adobe.com/events/docs/)

>[!TAB 개인정보 보호]

개인 정보 보호 워크플로, 데이터 거버넌스 및 데이터 주제 요청.

[API 탐색](https://experienceleague.adobe.com/ko/docs/experience-platform/privacy/home)

>[!TAB 사용자 관리]

사용자 관리, ID 관리 및 엔터프라이즈 계정 자동화

[API 탐색](https://developer.adobe.com/umapi/)

>[!ENDTABS]

## API를 사용하여 빌드

![Adobe CX Enterprise API에 연결하는 IDE](../assets/hero-connect-apis.gif)

클라우드 코드, 커서 및 OpenAI 코드와 같은 코딩 에이전트는 Adobe CX Enterprise API를 사용하여 빌드하는 데 적합합니다. 프로젝트에 OpenAPI 사양을 추가하면 에이전트는 끝점을 찾고 요청을 생성하며 수동 배선 없이 API 동작에 대한 이유를 파악할 수 있습니다. 시작하려면 Adobe Developer Console에서 인증된 자격 증명과 프로젝트에 추가된 API 설명서, 이렇게 두 가지가 필요합니다.

### Adobe Developer Console에서 API 자격 증명 설정

모든 Adobe CX Enterprise API 액세스는 [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)을(를) 통해 관리됩니다. 프로젝트를 만들고, 애플리케이션에 필요한 API를 추가하고, 자격 증명을 생성합니다.

1. Adobe Developer Console에서 로그인하고 [프로젝트를 만듭니다](https://developer.adobe.com/developer-console/docs/guides/projects/).
2. 필요한 Adobe CX 엔터프라이즈 응용 프로그램에 대해 [API를 추가](https://developer.adobe.com/developer-console/docs/guides/services/)합니다.
3. [인증 유형](https://developer.adobe.com/developer-console/docs/guides/authentication/)을 선택하세요. 자동화된 워크플로의 경우 **OAuth 서버 간**, 사용자 대면 애플리케이션의 경우 **OAuth 웹 앱**&#x200B;을 사용합니다.
4. 자격 증명을 생성합니다. 애플리케이션에서 사용할 클라이언트 ID, 클라이언트 암호 및 토큰 엔드포인트를 확인합니다.

대부분의 Adobe CX Enterprise API에는 애플리케이션 라이센스가 필요합니다. Developer Console 프로젝트에서 API를 사용할 수 없는 경우 Adobe 담당자에게 문의하십시오.

### 프로젝트에 Adobe API 컨텍스트 추가

AI 코딩 에이전트는 프로젝트에 올바른 참조 자료를 추가할 때 Adobe API를 안정적으로 검색하고 사용할 수 있습니다. OpenAPI 사양을 게시하는 모든 Adobe CX Enterprise API에 대해 작동합니다.

**1. API 사양 찾기**

위에 나열된 [Adobe CX Enterprise API](#adobe-cx-enterprise-apis)를 찾아보거나 [Adobe Developer API 카탈로그](https://developer.adobe.com/apis)&#x200B;(으)로 직접 이동합니다.

**2. OpenAPI 사양** 다운로드

프로젝트에 `/specs` 디렉터리를 만듭니다. [developer.adobe.com](https://developer.adobe.com/apis)의 API 참조 페이지에서 OpenAPI YAML을 다운로드하여 저장합니다. 원본 URL 및 다운로드 날짜를 기록하는 `README.md`을(를) 추가합니다.

```
/specs/README.md
/specs/aem-assets.openapi.yaml
```

>[!TIP]
>체크인 스냅샷을 사용하면 코딩 에이전트가 안정적이고 재현 가능한 동작을 제공하고 Git 기록에 API 변경 사항을 표시할 수 있습니다.

**3. API 인덱스** 생성

이 프롬프트를 코딩 에이전트에 붙여넣고 `<API-SPEC-FILE>`을(를) 파일 이름으로 바꿉니다.

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and generate /docs/<API-SPEC-FILE>.api.md.

Create a concise API index for AI coding agents. For each operation include: operationId, HTTP method, path, purpose, authentication requirements, required inputs, response shape, common error responses, pagination behavior, asynchronous behavior, and deprecation status.

Do not invent endpoints, parameters, request bodies, response fields, or behavior not present in the OpenAPI specification.
```

**4. 에이전트 지침 생성**

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and /docs/<API-SPEC-FILE>.api.md.

Generate AGENTS.md. Instructions should:
- Treat the OpenAPI specification as the source of truth.
- Use the API index as a navigation guide.
- Never invent endpoints, parameters, response fields, or status codes.
- Prefer documented operationIds.
- Avoid deprecated or experimental APIs unless explicitly requested.
- Follow authentication requirements defined in the specification.
- Use the local OpenAPI snapshot for implementation decisions.
```

**5. 확인**

생성된 파일만 사용하여 간단한 작업을 완료하도록 코딩 에이전트에 요청합니다.

```
Write a function that takes an AEM asset ID and returns the asset title and description. Use only /specs/aem-assets.openapi.yaml and /docs/aem-assets.api.md.
```

에이전트가 인벤터리 동작을 작성하지 않고 올바르게 완료하면 설정이 완료된 것입니다.

**권장 프로젝트 구조**

```
project/
├── specs/
│   ├── README.md
│   └── aem-assets.openapi.yaml
├── docs/
│   └── aem-assets.api.md
└── AGENTS.md
```

**현재 사양 유지**

Adobe에서 새 API 버전을 게시할 때 새 스냅숏을 `/specs`에 다운로드하고 날짜를 `README.md`로 업데이트한 다음 인덱스와 `AGENTS.md`을(를) 다시 생성합니다.
