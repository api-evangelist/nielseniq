---
name: nielseniq-rd-icv-dispatch
description: Pull Retail Data ecosystem ICV dispatch records from NielsenIQ, look them up by NAN key or external code, and
  acknowledge them.
api: openapi/nielseniq-rdecosystem-openapi.yml
operations:
- getRdICVDispatchRespUsingGET
- getRdICVDispatchforNanKeyRespUsingGET
- getRdICVDispatchforExtrncodeRespUsingGET
- postackRdICVDispatchforIDRespUsingPOST
- postackRdICVDispatchRespUsingPOST
generated: '2026-10-18'
method: generated
source: openapi/nielseniq-rdecosystem-openapi.yml
---

# Pull Retail Data ecosystem ICV dispatch records from NielsenIQ, look them up by NAN key or external code, and acknowledge them.

## Authentication

Send the `subscription-key` header (Azure API Management key from portal.developer.nielseniq.com) plus the required `Authorization` header on every call. Base URL: https://api.developer.nielseniq.com/rdecosystem.

## Steps

1. Call `getRdICVDispatchRespUsingGET` (GET /rddispatch/icv) with optional `size` and `provider` to fetch pending ICV dispatch records.
2. To look up a single record, call `getRdICVDispatchforNanKeyRespUsingGET` (GET /rddispatch/icv/nankey/{id}) or `getRdICVDispatchforExtrncodeRespUsingGET` (GET /rddispatch/icv/extrncd/{id}).
3. After you have processed a record, acknowledge it with `postackRdICVDispatchforIDRespUsingPOST` (POST /rddispatch/icv/ack/id/{id}), or acknowledge a batch with `postackRdICVDispatchRespUsingPOST` (POST /rddispatch/icv/ack).

## Errors

Every operation documents 200, 401 (bad or missing credentials), 403 (key not subscribed to this product), 404 and 500 responses. The contract defines no error body schema.

## Idempotency

The contract does not say whether an acknowledgement can be repeated safely. Acknowledge each record once and do not retry a POST blindly after a timeout.
