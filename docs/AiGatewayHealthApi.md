# AiGatewayHealthApi

All URIs are relative to *https://api.briskstack.com/ai-gateway/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**aiGatewayV1HealthzGet**](AiGatewayHealthApi.md#aigatewayv1healthzget) | **GET** /ai-gateway/v1/healthz | Health check endpoint |



## aiGatewayV1HealthzGet

> AiGatewayHealthzResponse aiGatewayV1HealthzGet()

Health check endpoint

Returns service health status

### Example

```ts
import {
  Configuration,
  AiGatewayHealthApi,
} from '@briskstack/platform';
import type { AiGatewayV1HealthzGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new AiGatewayHealthApi();

  try {
    const data = await api.aiGatewayV1HealthzGet();
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

[**AiGatewayHealthzResponse**](AiGatewayHealthzResponse.md)

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

