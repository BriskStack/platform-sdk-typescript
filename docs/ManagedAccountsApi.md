# ManagedAccountsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**authV1ManagedUserClaimPost**](ManagedAccountsApi.md#authv1manageduserclaimpost) | **POST** /auth/v1/managed-user/claim | Claim managed user account |
| [**authV1ManagedUserConsentPost**](ManagedAccountsApi.md#authv1manageduserconsentpost) | **POST** /auth/v1/managed-user/consent | Grant parental consent for a managed child |
| [**authV1ManagedUserLoginPost**](ManagedAccountsApi.md#authv1manageduserloginpost) | **POST** /auth/v1/managed-user/login | Login as managed user (requires parent authorization) |
| [**authV1ManagedUserPost**](ManagedAccountsApi.md#authv1manageduserpost) | **POST** /auth/v1/managed-user | Create managed user account |



## authV1ManagedUserClaimPost

> ClaimManagedUserResponse authV1ManagedUserClaimPost(claimManagedUserRequest)

Claim managed user account

Add email and password to an existing managed user account, enabling independent login. All history (activities, data) is preserved. This is a public endpoint - no authentication required.

### Example

```ts
import {
  Configuration,
  ManagedAccountsApi,
} from '@briskstack/platform';
import type { AuthV1ManagedUserClaimPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new ManagedAccountsApi();

  const body = {
    // ClaimManagedUserRequest (optional)
    claimManagedUserRequest: ...,
  } satisfies AuthV1ManagedUserClaimPostRequest;

  try {
    const data = await api.authV1ManagedUserClaimPost(body);
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
| **claimManagedUserRequest** | [ClaimManagedUserRequest](ClaimManagedUserRequest.md) |  | [Optional] |

### Return type

[**ClaimManagedUserResponse**](ClaimManagedUserResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Account claimed successfully |  -  |
| **400** | Invalid request |  -  |
| **404** | User not found |  -  |
| **409** | Account already claimed or email in use |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## authV1ManagedUserConsentPost

> GrantConsentResponse authV1ManagedUserConsentPost(grantConsentRequest)

Grant parental consent for a managed child

Creates a parental consent record allowing the authenticated user (parent) to access the specified child account. Required for multi-child device sharing. Idempotent - safe to call if consent already exists.

### Example

```ts
import {
  Configuration,
  ManagedAccountsApi,
} from '@briskstack/platform';
import type { AuthV1ManagedUserConsentPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ManagedAccountsApi(config);

  const body = {
    // GrantConsentRequest (optional)
    grantConsentRequest: ...,
  } satisfies AuthV1ManagedUserConsentPostRequest;

  try {
    const data = await api.authV1ManagedUserConsentPost(body);
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
| **grantConsentRequest** | [GrantConsentRequest](GrantConsentRequest.md) |  | [Optional] |

### Return type

[**GrantConsentResponse**](GrantConsentResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Consent granted successfully |  -  |
| **401** | Authentication required |  -  |
| **404** | Child user not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## authV1ManagedUserLoginPost

> LoginManagedUserResponse authV1ManagedUserLoginPost(loginManagedUserRequest)

Login as managed user (requires parent authorization)

Creates a session for a managed user (child without email/password). Requires parent authorization via Bearer token. Parent must have parental consent relationship with the managed user. Returns child JWT for multi-account device sharing.

### Example

```ts
import {
  Configuration,
  ManagedAccountsApi,
} from '@briskstack/platform';
import type { AuthV1ManagedUserLoginPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ManagedAccountsApi(config);

  const body = {
    // LoginManagedUserRequest (optional)
    loginManagedUserRequest: ...,
  } satisfies AuthV1ManagedUserLoginPostRequest;

  try {
    const data = await api.authV1ManagedUserLoginPost(body);
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
| **loginManagedUserRequest** | [LoginManagedUserRequest](LoginManagedUserRequest.md) |  | [Optional] |

### Return type

[**LoginManagedUserResponse**](LoginManagedUserResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Login successful |  -  |
| **401** | Parent authentication required |  -  |
| **403** | Not authorized for this child |  -  |
| **404** | Managed user not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## authV1ManagedUserPost

> CreateManagedUserResponse authV1ManagedUserPost(createManagedUserRequest)

Create managed user account

Create a managed user account without email/password. The user can participate in platform features but cannot log in until they claim their account. Requires service authentication (internal JWT).

### Example

```ts
import {
  Configuration,
  ManagedAccountsApi,
} from '@briskstack/platform';
import type { AuthV1ManagedUserPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ManagedAccountsApi(config);

  const body = {
    // CreateManagedUserRequest (optional)
    createManagedUserRequest: ...,
  } satisfies AuthV1ManagedUserPostRequest;

  try {
    const data = await api.authV1ManagedUserPost(body);
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
| **createManagedUserRequest** | [CreateManagedUserRequest](CreateManagedUserRequest.md) |  | [Optional] |

### Return type

[**CreateManagedUserResponse**](CreateManagedUserResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Managed user account created |  -  |
| **400** | Invalid request |  -  |
| **401** | Service authentication required |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

