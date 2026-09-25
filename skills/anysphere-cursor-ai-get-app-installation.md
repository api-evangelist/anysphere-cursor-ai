---
name: anysphere-cursor-ai-get-app-installation
description: Retrieve details of a specific app installation for the authenticated app.
api: openapi/anysphere-cursor-ai-openapi.yaml
operations:
- OriginService_ListAppInstallations
- OriginService_GetAppInstallation
generated: '2026-09-25'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/anysphere-cursor-ai-openapi.yaml ; every operationId checked against the contract
---

# anysphere-cursor-ai-get-app-installation

Retrieve details of a specific app installation for the authenticated app.

## Steps

1. 1. Call `OriginService_ListAppInstallations` – include the `Authorization: Bearer <token>` header; use query parameters `page` and `per_page` if pagination is needed.
2. 2. Call `OriginService_GetAppInstallation` – include the `Authorization: Bearer <token>` header and provide the `installationId` path parameter obtained from the list response.

## Rules

- Auth: All requests require an `Authorization: Bearer <token>` header (bearerAuth).
- Pagination: `OriginService_ListAppInstallations` supports `page` and `per_page` query parameters for paginated results.
- Idempotency: Not applicable for these GET operations.
