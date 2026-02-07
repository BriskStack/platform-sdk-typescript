# UserApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**authV1MeGet**](UserApi.md#authv1meget) | **GET** /auth/v1/me | Get current user |
| [**authV1MePatch**](UserApi.md#authv1mepatch) | **PATCH** /auth/v1/me | Update current user profile |
| [**authV1UsersUserIdPatch**](UserApi.md#authv1usersuseridpatch) | **PATCH** /auth/v1/users/{userId} | Update user profile by ID (service-only) |



## authV1MeGet

> UserProfile authV1MeGet()

Get current user

Get the profile of the currently authenticated user

### Example

```ts
import {
  Configuration,
  UserApi,
} from '@briskstack/platform';
import type { AuthV1MeGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UserApi(config);

  try {
    const data = await api.authV1MeGet();
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

[**UserProfile**](UserProfile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User profile |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## authV1MePatch

> UserProfile authV1MePatch(updateProfileRequest)

Update current user profile

Update profile information for the currently authenticated user

### Example

```ts
import {
  Configuration,
  UserApi,
} from '@briskstack/platform';
import type { AuthV1MePatchRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UserApi(config);

  const body = {
    // UpdateProfileRequest (optional)
    updateProfileRequest: ...,
  } satisfies AuthV1MePatchRequest;

  try {
    const data = await api.authV1MePatch(body);
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
| **updateProfileRequest** | [UpdateProfileRequest](UpdateProfileRequest.md) |  | [Optional] |

### Return type

[**UserProfile**](UserProfile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Profile updated successfully |  -  |
| **400** | Invalid request body |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## authV1UsersUserIdPatch

> UserProfile authV1UsersUserIdPatch(userId, updateUserByIdRequest)

Update user profile by ID (service-only)

Update profile for a specific user by ID. Requires service authentication (internal JWT).

### Example

```ts
import {
  Configuration,
  UserApi,
} from '@briskstack/platform';
import type { AuthV1UsersUserIdPatchRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UserApi(config);

  const body = {
    // string
    userId: 123e4567-e89b-12d3-a456-426614174000,
    // UpdateUserByIdRequest (optional)
    updateUserByIdRequest: ...,
  } satisfies AuthV1UsersUserIdPatchRequest;

  try {
    const data = await api.authV1UsersUserIdPatch(body);
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
| **userId** | `string` |  | [Defaults to `undefined`] |
| **updateUserByIdRequest** | [UpdateUserByIdRequest](UpdateUserByIdRequest.md) |  | [Optional] |

### Return type

[**UserProfile**](UserProfile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Profile updated successfully |  -  |
| **400** | Invalid request body |  -  |
| **401** | Service authentication required |  -  |
| **404** | User not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

