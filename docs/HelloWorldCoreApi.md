# HelloWorldCoreApi

All URIs are relative to *https://api.briskstack.com/ai-gateway/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**helloWorldV1Get**](HelloWorldCoreApi.md#helloworldv1get) | **GET** /hello-world/v1/ | Hello endpoint |



## helloWorldV1Get

> HelloWorldHelloResponse helloWorldV1Get()

Hello endpoint

Returns a friendly hello message with service information

### Example

```ts
import {
  Configuration,
  HelloWorldCoreApi,
} from '@briskstack/platform-sdk';
import type { HelloWorldV1GetRequest } from '@briskstack/platform-sdk';

async function example() {
  console.log("🚀 Testing @briskstack/platform-sdk SDK...");
  const api = new HelloWorldCoreApi();

  try {
    const data = await api.helloWorldV1Get();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**HelloWorldHelloResponse**](HelloWorldHelloResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

