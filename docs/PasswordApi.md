# PasswordApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**authV1PasswordResetConfirmPost**](PasswordApi.md#authv1passwordresetconfirmpost) | **POST** /auth/v1/password/reset/confirm | Confirm password reset |
| [**authV1PasswordResetPost**](PasswordApi.md#authv1passwordresetpost) | **POST** /auth/v1/password/reset | Request password reset |



## authV1PasswordResetConfirmPost

> PasswordResetConfirmResponse authV1PasswordResetConfirmPost(passwordResetConfirmRequest)

Confirm password reset

Reset password using token from email

### Example

```ts
import {
  Configuration,
  PasswordApi,
} from '@briskstack/platform';
import type { AuthV1PasswordResetConfirmPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new PasswordApi();

  const body = {
    // PasswordResetConfirmRequest (optional)
    passwordResetConfirmRequest: ...,
  } satisfies AuthV1PasswordResetConfirmPostRequest;

  try {
    const data = await api.authV1PasswordResetConfirmPost(body);
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
| **passwordResetConfirmRequest** | [PasswordResetConfirmRequest](PasswordResetConfirmRequest.md) |  | [Optional] |

### Return type

[**PasswordResetConfirmResponse**](PasswordResetConfirmResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Password reset successful |  -  |
| **400** | Invalid or expired token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## authV1PasswordResetPost

> PasswordResetResponse authV1PasswordResetPost(passwordResetRequest)

Request password reset

Send password reset email to user

### Example

```ts
import {
  Configuration,
  PasswordApi,
} from '@briskstack/platform';
import type { AuthV1PasswordResetPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new PasswordApi();

  const body = {
    // PasswordResetRequest (optional)
    passwordResetRequest: ...,
  } satisfies AuthV1PasswordResetPostRequest;

  try {
    const data = await api.authV1PasswordResetPost(body);
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
| **passwordResetRequest** | [PasswordResetRequest](PasswordResetRequest.md) |  | [Optional] |

### Return type

[**PasswordResetResponse**](PasswordResetResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reset email sent (if account exists) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

