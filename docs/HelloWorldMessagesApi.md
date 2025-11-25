# HelloWorldMessagesApi

All URIs are relative to *https://api.briskstack.com/ai-gateway/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**helloWorldV1MessagesPost**](HelloWorldMessagesApi.md#helloworldv1messagespost) | **POST** /hello-world/v1/messages | Create message |



## helloWorldV1MessagesPost

> HelloWorldCreateMessageResponse helloWorldV1MessagesPost(helloWorldCreateMessageRequest)

Create message

Creates a new message

### Example

```ts
import {
  Configuration,
  HelloWorldMessagesApi,
} from '@briskstack/platform';
import type { HelloWorldV1MessagesPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new HelloWorldMessagesApi();

  const body = {
    // HelloWorldCreateMessageRequest (optional)
    helloWorldCreateMessageRequest: ...,
  } satisfies HelloWorldV1MessagesPostRequest;

  try {
    const data = await api.helloWorldV1MessagesPost(body);
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
| **helloWorldCreateMessageRequest** | [HelloWorldCreateMessageRequest](HelloWorldCreateMessageRequest.md) |  | [Optional] |

### Return type

[**HelloWorldCreateMessageResponse**](HelloWorldCreateMessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Message created |  -  |
| **422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

