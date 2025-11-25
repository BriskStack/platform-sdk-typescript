# AiGatewayChatApi

All URIs are relative to *https://api.briskstack.com/ai-gateway/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**aiGatewayV1ChatCompletionsPost**](AiGatewayChatApi.md#aigatewayv1chatcompletionspost) | **POST** /ai-gateway/v1/chat/completions | Create chat completion |



## aiGatewayV1ChatCompletionsPost

> AiGatewayChatCompletionResponse aiGatewayV1ChatCompletionsPost(aiGatewayChatCompletionRequest)

Create chat completion

Creates a chat completion using AI providers via Cloudflare AI Gateway. Supports BYOK (Bring Your Own Key) - pass your AI provider API key in the X-API-Key header.

### Example

```ts
import {
  Configuration,
  AiGatewayChatApi,
} from '@briskstack/platform-sdk';
import type { AiGatewayV1ChatCompletionsPostRequest } from '@briskstack/platform-sdk';

async function example() {
  console.log("🚀 Testing @briskstack/platform-sdk SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: apiKeyAuth
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new AiGatewayChatApi(config);

  const body = {
    // AiGatewayChatCompletionRequest (optional)
    aiGatewayChatCompletionRequest: ...,
  } satisfies AiGatewayV1ChatCompletionsPostRequest;

  try {
    const data = await api.aiGatewayV1ChatCompletionsPost(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **aiGatewayChatCompletionRequest** | [AiGatewayChatCompletionRequest](AiGatewayChatCompletionRequest.md) |  | [Optional] |

### Return type

[**AiGatewayChatCompletionResponse**](AiGatewayChatCompletionResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth), [bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Chat completion successful |  -  |
| **400** | Bad request - invalid parameters |  -  |
| **401** | Unauthorized - missing or invalid OpenAI API key |  -  |
| **422** | Validation error - request body validation failed |  -  |
| **500** | Internal server error |  -  |
| **502** | Bad gateway - upstream API error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

