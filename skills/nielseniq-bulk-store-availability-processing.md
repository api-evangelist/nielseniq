---
name: nielseniq-bulk-store-availability-processing
description: Submit bulk store availability data for processing and monitor job status.
api: openapi/nielseniq-store-availability-bulk-openapi.yml
operations:
- getBatchStoreAvailabilityRespUsingPOST
- getAddCheckDigitRespUsingPOST
- getJobStatusRespUsingGET
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (deepseek)
source: openapi/nielseniq-store-availability-bulk-openapi.yml ; every operationId checked against the contract
---

# nielseniq-bulk-store-availability-processing

Submit bulk store availability data for processing and monitor job status.

## Steps

1. 1. Submit batch store availability data using `getBatchStoreAvailabilityRespUsingPOST` with the required request body fields
2. 2. Add check digits for validation using `getAddCheckDigitRespUsingPOST` with the required request body fields
3. 3. Monitor processing status using `getJobStatusRespUsingGET` with the job identifier

## Rules

- Authentication requires either apiKeyHeader (apiKey) or apiKeyHeader (subscription-key) header, or apiKeyQuery parameter
- Use the base server URL https://api.developer.nielseniq.com/data-access/v1 for all operations
- Job status checking is idempotent and can be polled multiple times without side effects
- Batch processing operations are asynchronous requiring separate status checks
