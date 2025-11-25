# HelloWorldAuthApi

All URIs are relative to *https://api.briskstack.com/ai-gateway/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**helloWorldV1ProtectedGet**](HelloWorldAuthApi.md#helloworldv1protectedget) | **GET** /hello-world/v1/protected | Protected endpoint (requires authentication) |



## helloWorldV1ProtectedGet

> HelloWorldProtectedResponse helloWorldV1ProtectedGet()

Protected endpoint (requires authentication)

Demonstrates authentication - requires valid user JWT from Supabase

### Example

```ts
import {
  Configuration,
  HelloWorldAuthApi,
} from '@briskstack/platform-sdk';
import type { HelloWorldV1ProtectedGetRequest } from '@briskstack/platform-sdk';

async function example() {
  console.log("🚀 Testing @briskstack/platform-sdk SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new HelloWorldAuthApi(config);

  try {
    const data = await api.helloWorldV1ProtectedGet();
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

[**HelloWorldProtectedResponse**](HelloWorldProtectedResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Success - authenticated user |  -  |
| **401** | Unauthorized - no/invalid token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

