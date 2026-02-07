# PreferencesApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**notificationsV1PreferencesGet**](PreferencesApi.md#notificationsv1preferencesget) | **GET** /notifications/v1/preferences | Get notification preferences |
| [**notificationsV1PreferencesPatch**](PreferencesApi.md#notificationsv1preferencespatch) | **PATCH** /notifications/v1/preferences | Update notification preferences |



## notificationsV1PreferencesGet

> GetPreferencesResponse notificationsV1PreferencesGet()

Get notification preferences

Returns the authenticated user\&#39;s notification preferences

### Example

```ts
import {
  Configuration,
  PreferencesApi,
} from '@briskstack/platform';
import type { NotificationsV1PreferencesGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new PreferencesApi(config);

  try {
    const data = await api.notificationsV1PreferencesGet();
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

[**GetPreferencesResponse**](GetPreferencesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Notification preferences |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## notificationsV1PreferencesPatch

> GetPreferencesResponse notificationsV1PreferencesPatch(updatePreferencesRequest)

Update notification preferences

Updates the authenticated user\&#39;s notification preferences

### Example

```ts
import {
  Configuration,
  PreferencesApi,
} from '@briskstack/platform';
import type { NotificationsV1PreferencesPatchRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new PreferencesApi(config);

  const body = {
    // UpdatePreferencesRequest (optional)
    updatePreferencesRequest: ...,
  } satisfies NotificationsV1PreferencesPatchRequest;

  try {
    const data = await api.notificationsV1PreferencesPatch(body);
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
| **updatePreferencesRequest** | [UpdatePreferencesRequest](UpdatePreferencesRequest.md) |  | [Optional] |

### Return type

[**GetPreferencesResponse**](GetPreferencesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Updated preferences |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

