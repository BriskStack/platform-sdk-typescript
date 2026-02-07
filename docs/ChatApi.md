# ChatApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**aiV1ChatCompletionsPost**](ChatApi.md#aiv1chatcompletionspost) | **POST** /ai/v1/chat/completions | Create chat completion |



## aiV1ChatCompletionsPost

> ChatCompletionResponse aiV1ChatCompletionsPost(chatCompletionRequest)

Create chat completion

Creates a chat completion using AI providers via Cloudflare AI Gateway. Supports BYOK (Bring Your Own Key) - pass your AI provider API key in the X-API-Key header.

### Example

```ts
import {
  Configuration,
  ChatApi,
} from '@briskstack/platform';
import type { AiV1ChatCompletionsPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: apiKeyAuth
    apiKey: "YOUR API KEY",
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ChatApi(config);

  const body = {
    // ChatCompletionRequest (optional)
    chatCompletionRequest: ...,
  } satisfies AiV1ChatCompletionsPostRequest;

  try {
    const data = await api.aiV1ChatCompletionsPost(body);
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
| **chatCompletionRequest** | [ChatCompletionRequest](ChatCompletionRequest.md) |  | [Optional] |

### Return type

[**ChatCompletionResponse**](ChatCompletionResponse.md)

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

