# OAuthApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**authV1OauthCallbackPost**](OAuthApi.md#authv1oauthcallbackpost) | **POST** /auth/v1/oauth/callback | OAuth callback |
| [**authV1OauthStartPost**](OAuthApi.md#authv1oauthstartpost) | **POST** /auth/v1/oauth/start | Start OAuth flow |



## authV1OauthCallbackPost

> OAuthCallbackResponse authV1OauthCallbackPost(oAuthCallbackRequest)

OAuth callback

Handle OAuth callback from provider

### Example

```ts
import {
  Configuration,
  OAuthApi,
} from '@briskstack/platform';
import type { AuthV1OauthCallbackPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new OAuthApi();

  const body = {
    // OAuthCallbackRequest (optional)
    oAuthCallbackRequest: ...,
  } satisfies AuthV1OauthCallbackPostRequest;

  try {
    const data = await api.authV1OauthCallbackPost(body);
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
| **oAuthCallbackRequest** | [OAuthCallbackRequest](OAuthCallbackRequest.md) |  | [Optional] |

### Return type

[**OAuthCallbackResponse**](OAuthCallbackResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OAuth authentication successful |  -  |
| **400** | OAuth error |  -  |
| **401** | OAuth authentication failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## authV1OauthStartPost

> OAuthStartResponse authV1OauthStartPost(oAuthStartRequest)

Start OAuth flow

Initiate OAuth authentication with external provider

### Example

```ts
import {
  Configuration,
  OAuthApi,
} from '@briskstack/platform';
import type { AuthV1OauthStartPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new OAuthApi();

  const body = {
    // OAuthStartRequest (optional)
    oAuthStartRequest: ...,
  } satisfies AuthV1OauthStartPostRequest;

  try {
    const data = await api.authV1OauthStartPost(body);
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
| **oAuthStartRequest** | [OAuthStartRequest](OAuthStartRequest.md) |  | [Optional] |

### Return type

[**OAuthStartResponse**](OAuthStartResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OAuth authorization URL |  -  |
| **400** | Invalid provider |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

