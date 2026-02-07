# DevicesApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**notificationsV1DevicesPost**](DevicesApi.md#notificationsv1devicespost) | **POST** /notifications/v1/devices | Register device token |
| [**notificationsV1DevicesTokenDelete**](DevicesApi.md#notificationsv1devicestokendelete) | **DELETE** /notifications/v1/devices/{token} | Unregister device token |



## notificationsV1DevicesPost

> RegisterDeviceResponse notificationsV1DevicesPost(registerDeviceRequest)

Register device token

Registers a device token for push notifications

### Example

```ts
import {
  Configuration,
  DevicesApi,
} from '@briskstack/platform';
import type { NotificationsV1DevicesPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DevicesApi(config);

  const body = {
    // RegisterDeviceRequest (optional)
    registerDeviceRequest: ...,
  } satisfies NotificationsV1DevicesPostRequest;

  try {
    const data = await api.notificationsV1DevicesPost(body);
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
| **registerDeviceRequest** | [RegisterDeviceRequest](RegisterDeviceRequest.md) |  | [Optional] |

### Return type

[**RegisterDeviceResponse**](RegisterDeviceResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Device registered |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## notificationsV1DevicesTokenDelete

> notificationsV1DevicesTokenDelete(token)

Unregister device token

Removes a device token (e.g., on logout)

### Example

```ts
import {
  Configuration,
  DevicesApi,
} from '@briskstack/platform';
import type { NotificationsV1DevicesTokenDeleteRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DevicesApi(config);

  const body = {
    // string
    token: ExponentPushToken[xxxxxxxxxxxxxxxxxxxxxx],
  } satisfies NotificationsV1DevicesTokenDeleteRequest;

  try {
    const data = await api.notificationsV1DevicesTokenDelete(body);
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
| **token** | `string` |  | [Defaults to `undefined`] |

### Return type

`void` (Empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Device unregistered |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

