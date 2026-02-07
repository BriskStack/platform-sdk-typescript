# TokenApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**authV1RefreshPost**](TokenApi.md#authv1refreshpost) | **POST** /auth/v1/refresh | Refresh access token |



## authV1RefreshPost

> RefreshResponse authV1RefreshPost(refreshRequest)

Refresh access token

Exchange refresh token for new access/refresh token pair

### Example

```ts
import {
  Configuration,
  TokenApi,
} from '@briskstack/platform';
import type { AuthV1RefreshPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new TokenApi();

  const body = {
    // RefreshRequest (optional)
    refreshRequest: ...,
  } satisfies AuthV1RefreshPostRequest;

  try {
    const data = await api.authV1RefreshPost(body);
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
| **refreshRequest** | [RefreshRequest](RefreshRequest.md) |  | [Optional] |

### Return type

[**RefreshResponse**](RefreshResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Token refreshed |  -  |
| **401** | Invalid or expired refresh token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

