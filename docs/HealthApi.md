# HealthApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**platformV1HealthzGet**](HealthApi.md#platformv1healthzget) | **GET** /platform/v1/healthz | Health check endpoint |



## platformV1HealthzGet

> HealthzResponse platformV1HealthzGet()

Health check endpoint

Returns service health status

### Example

```ts
import {
  Configuration,
  HealthApi,
} from '@briskstack/platform';
import type { PlatformV1HealthzGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new HealthApi();

  try {
    const data = await api.platformV1HealthzGet();
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

[**HealthzResponse**](HealthzResponse.md)

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

