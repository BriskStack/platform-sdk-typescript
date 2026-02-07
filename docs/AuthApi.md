# AuthApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**authV1LoginPost**](AuthApi.md#authv1loginpost) | **POST** /auth/v1/login | Login with email and password |
| [**authV1RegisterPost**](AuthApi.md#authv1registerpost) | **POST** /auth/v1/register | Register new user |



## authV1LoginPost

> LoginResponse authV1LoginPost(loginRequest)

Login with email and password

Authenticate user and return access/refresh tokens

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@briskstack/platform';
import type { AuthV1LoginPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new AuthApi();

  const body = {
    // LoginRequest (optional)
    loginRequest: ...,
  } satisfies AuthV1LoginPostRequest;

  try {
    const data = await api.authV1LoginPost(body);
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
| **loginRequest** | [LoginRequest](LoginRequest.md) |  | [Optional] |

### Return type

[**LoginResponse**](LoginResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Login successful |  -  |
| **401** | Invalid credentials |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## authV1RegisterPost

> RegisterResponse authV1RegisterPost(registerRequest)

Register new user

Create a new user account with email and password

### Example

```ts
import {
  Configuration,
  AuthApi,
} from '@briskstack/platform';
import type { AuthV1RegisterPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const api = new AuthApi();

  const body = {
    // RegisterRequest (optional)
    registerRequest: ...,
  } satisfies AuthV1RegisterPostRequest;

  try {
    const data = await api.authV1RegisterPost(body);
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
| **registerRequest** | [RegisterRequest](RegisterRequest.md) |  | [Optional] |

### Return type

[**RegisterResponse**](RegisterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | User created successfully |  -  |
| **400** | Invalid request |  -  |
| **409** | Email already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

