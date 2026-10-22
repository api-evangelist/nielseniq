---
name: nielseniq-data-access-catalogues
description: Query NielsenIQ Buy Data Access metadata catalogues.
api: openapi/nielseniq-buy-data-access-catalogues-api-openapi.yml
operations:
- getCataloguesRespUsingPOST
generated: '2026-10-18'
method: generated
source: openapi/nielseniq-buy-data-access-catalogues-api-openapi.yml
---

# Query NielsenIQ Buy Data Access metadata catalogues.

## Authentication

Send the required `Authorization`, `Accept`, `Content-Type` and `subscription-key` headers. The security schemes in the spec name an `apiKey` header or query parameter. Base URL: https://api.developer.nielseniq.com/data-access/v1.

## Steps

1. Call `getCataloguesRespUsingPOST` (POST /Catalogues) with the catalogue query in the JSON request body.

## Errors

Every operation documents 200, 401 (bad or missing credentials), 403 (key not subscribed to this product), 404 and 500 responses. The contract defines no error body schema.

## Idempotency

This is a POST used as a read. The contract does not state whether it is idempotent.
