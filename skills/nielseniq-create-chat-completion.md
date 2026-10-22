---
name: nielseniq-create-chat-completion
description: Creates a completion for a chat message using a specified deployment model.
api: openapi/nielseniq-crmcasetrackapi-openapi.yml
operations:
- postChatCompletionsCreateRespUsingPOST
- 688cd23dbe4114127cd8747d
- postEmbeddingsCreateRespUsingPOST
- postImageGenerationsCreateDalleRespUsingPOST
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (deepseek)
source: openapi/nielseniq-crmcasetrackapi-openapi.yml ; every operationId checked against the contract
---

# nielseniq-create-chat-completion

Creates a completion for a chat message using a specified deployment model.

## Steps

1. 1. Call `postChatCompletionsCreateRespUsingPOST` with the `deployment-id` path parameter and required request body fields for the chat completion
2. 2. Call `688cd23dbe4114127cd8747d` with the `deployment-id` path parameter and required request body fields for prompt completion
3. 3. Call `postEmbeddingsCreateRespUsingPOST` with the `deployment-id` path parameter and required request body fields to get vector representations
4. 4. Call `postImageGenerationsCreateDalleRespUsingPOST` with the `deployment-id` path parameter and required request body fields to generate images from text captions

## Rules

- Authentication requires either apiKey header or subscription-key header
- Use the base server URL https://api.developer.nielseniq.com/data-access/v1
- Operations use path parameters like deployment-id for model deployments
- Batch operations are available for processing multiple requests
