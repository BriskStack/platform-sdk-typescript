# EmailApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**authV1EmailResendPost**](EmailApi.md#authv1emailresendpost) | **POST** /auth/v1/email/resend | Resend verification email |
| [**authV1EmailVerifyPost**](EmailApi.md#authv1emailverifypost) | **POST** /auth/v1/email/verify | Verify email address |



## authV1EmailResendPost

> ResendVerificationResponse authV1EmailResendPost(resendVerificationRequest)

Resend verification email

Resend email verification link

### Example

```ts
import {
  Configuration,
  EmailApi,
} from '@briskstack/platform';
import type { AuthV1EmailResendPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new EmailApi();

  const body = {
    // ResendVerificationRequest (optional)
    resendVerificationRequest: ...,
  } satisfies AuthV1EmailResendPostRequest;

  try {
    const data = await api.authV1EmailResendPost(body);
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
| **resendVerificationRequest** | [ResendVerificationRequest](ResendVerificationRequest.md) |  | [Optional] |

### Return type

[**ResendVerificationResponse**](ResendVerificationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Verification email sent (if applicable) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## authV1EmailVerifyPost

> EmailVerifyResponse authV1EmailVerifyPost(emailVerifyRequest)

Verify email address

Verify email using token from verification email

### Example

```ts
import {
  Configuration,
  EmailApi,
} from '@briskstack/platform';
import type { AuthV1EmailVerifyPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new EmailApi();

  const body = {
    // EmailVerifyRequest (optional)
    emailVerifyRequest: ...,
  } satisfies AuthV1EmailVerifyPostRequest;

  try {
    const data = await api.authV1EmailVerifyPost(body);
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
| **emailVerifyRequest** | [EmailVerifyRequest](EmailVerifyRequest.md) |  | [Optional] |

### Return type

[**EmailVerifyResponse**](EmailVerifyResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Email verified |  -  |
| **400** | Invalid or expired token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

