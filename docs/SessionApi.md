# SessionApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**authV1LogoutPost**](SessionApi.md#authv1logoutpost) | **POST** /auth/v1/logout | Logout user |
| [**authV1SessionsGet**](SessionApi.md#authv1sessionsget) | **GET** /auth/v1/sessions | List active sessions |
| [**authV1SessionsSessionIdDelete**](SessionApi.md#authv1sessionssessioniddelete) | **DELETE** /auth/v1/sessions/{sessionId} | Revoke a session |



## authV1LogoutPost

> LogoutResponse authV1LogoutPost(logoutRequest)

Logout user

Revoke refresh token and end session

### Example

```ts
import {
  Configuration,
  SessionApi,
} from '@briskstack/platform';
import type { AuthV1LogoutPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new SessionApi(config);

  const body = {
    // LogoutRequest (optional)
    logoutRequest: ...,
  } satisfies AuthV1LogoutPostRequest;

  try {
    const data = await api.authV1LogoutPost(body);
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
| **logoutRequest** | [LogoutRequest](LogoutRequest.md) |  | [Optional] |

### Return type

[**LogoutResponse**](LogoutResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Logout successful |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## authV1SessionsGet

> SessionsResponse authV1SessionsGet()

List active sessions

Get all active sessions for the current user

### Example

```ts
import {
  Configuration,
  SessionApi,
} from '@briskstack/platform';
import type { AuthV1SessionsGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new SessionApi(config);

  try {
    const data = await api.authV1SessionsGet();
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

[**SessionsResponse**](SessionsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Sessions list |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## authV1SessionsSessionIdDelete

> SuccessResponse authV1SessionsSessionIdDelete(sessionId)

Revoke a session

Revoke a specific session by ID

### Example

```ts
import {
  Configuration,
  SessionApi,
} from '@briskstack/platform';
import type { AuthV1SessionsSessionIdDeleteRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new SessionApi(config);

  const body = {
    // string
    sessionId: 123e4567-e89b-12d3-a456-426614174000,
  } satisfies AuthV1SessionsSessionIdDeleteRequest;

  try {
    const data = await api.authV1SessionsSessionIdDelete(body);
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
| **sessionId** | `string` |  | [Defaults to `undefined`] |

### Return type

[**SuccessResponse**](SuccessResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Session revoked |  -  |
| **401** | Unauthorized |  -  |
| **404** | Session not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

