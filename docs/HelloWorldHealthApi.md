# HelloWorldHealthApi

All URIs are relative to *https://api.briskstack.com/ai-gateway/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**helloWorldV1HealthzGet**](HelloWorldHealthApi.md#helloworldv1healthzget) | **GET** /hello-world/v1/healthz | Health check endpoint |



## helloWorldV1HealthzGet

> HelloWorldHealthzResponse helloWorldV1HealthzGet()

Health check endpoint

Returns service health status

### Example

```ts
import {
  Configuration,
  HelloWorldHealthApi,
} from '@briskstack/platform-sdk';
import type { HelloWorldV1HealthzGetRequest } from '@briskstack/platform-sdk';

async function example() {
  console.log("🚀 Testing @briskstack/platform-sdk SDK...");
  const api = new HelloWorldHealthApi();

  try {
    const data = await api.helloWorldV1HealthzGet();
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

[**HelloWorldHealthzResponse**](HelloWorldHealthzResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Service is healthy |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

