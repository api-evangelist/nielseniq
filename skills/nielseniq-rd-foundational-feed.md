---
name: nielseniq-rd-foundational-feed
description: Read the NielsenIQ RD foundational product feed page by page and record or reset processing status.
api: openapi/nielseniq-rdecosystembb-openapi.yml
operations:
- getRdFoundationalFeedRespUsingGET
- updateBbProcessingStatusRespUsingPOST
- resetBbProcessingStatusRespUsingPOST
- getRdimageDispatchRespUsingGET
generated: '2026-10-18'
method: generated
source: openapi/nielseniq-rdecosystembb-openapi.yml
---

# Read the NielsenIQ RD foundational product feed page by page and record or reset processing status.

## Authentication

Send the `subscription-key` header (Azure API Management key from portal.developer.nielseniq.com) plus the required `Authorization` header. The image dispatch call needs only `subscription-key`. Base URL: https://api.developer.nielseniq.com/rdecosystem-bb.

## Steps

1. Call `getRdFoundationalFeedRespUsingGET` (GET /rdfoundationalfeed). Filter with `fromDate`, `endDate`, `country`, `provider` and `productType`, and page with `page`, `size` and `limit`.
2. Get product images with `getRdimageDispatchRespUsingGET` (GET /rdimagedispatch?imgId=...).
3. Report what you processed with `updateBbProcessingStatusRespUsingPOST` (POST /updateBbProcessingStatus). Use `resetBbProcessingStatusRespUsingPOST` (POST /resetBbProcessingStatus) only to reprocess items on purpose.

## Errors

Every operation documents 200, 401 (bad or missing credentials), 403 (key not subscribed to this product), 404 and 500 responses. The contract defines no error body schema.

## Idempotency

Both status calls are POST requests that change state. Do not retry them without checking the current status first.
