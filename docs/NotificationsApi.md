# NotificationsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**notificationsV1InboxGet**](NotificationsApi.md#notificationsv1inboxget) | **GET** /notifications/v1/inbox | Get notification inbox |
| [**notificationsV1NotificationIdReadPatch**](NotificationsApi.md#notificationsv1notificationidreadpatch) | **PATCH** /notifications/v1/{notificationId}/read | Mark notification as read |
| [**notificationsV1ReadAllPatch**](NotificationsApi.md#notificationsv1readallpatch) | **PATCH** /notifications/v1/read-all | Mark all notifications as read |
| [**notificationsV1SendPost**](NotificationsApi.md#notificationsv1sendpost) | **POST** /notifications/v1/send | Send notification |



## notificationsV1InboxGet

> InboxResponse notificationsV1InboxGet(limit, cursor, unreadOnly)

Get notification inbox

Returns the authenticated user\&#39;s notifications

### Example

```ts
import {
  Configuration,
  NotificationsApi,
} from '@briskstack/platform';
import type { NotificationsV1InboxGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new NotificationsApi(config);

  const body = {
    // string (optional)
    limit: 20,
    // string (optional)
    cursor: 2025-01-15T10:00:00Z_123e4567,
    // 'true' | 'false' (optional)
    unreadOnly: true,
  } satisfies NotificationsV1InboxGetRequest;

  try {
    const data = await api.notificationsV1InboxGet(body);
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
| **limit** | `string` |  | [Optional] [Defaults to `undefined`] |
| **cursor** | `string` |  | [Optional] [Defaults to `undefined`] |
| **unreadOnly** | `true`, `false` |  | [Optional] [Defaults to `undefined`] [Enum: true, false] |

### Return type

[**InboxResponse**](InboxResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Notification inbox |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## notificationsV1NotificationIdReadPatch

> notificationsV1NotificationIdReadPatch(notificationId)

Mark notification as read

Marks a specific notification as read

### Example

```ts
import {
  Configuration,
  NotificationsApi,
} from '@briskstack/platform';
import type { NotificationsV1NotificationIdReadPatchRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new NotificationsApi(config);

  const body = {
    // string
    notificationId: 123e4567-e89b-12d3-a456-426614174000,
  } satisfies NotificationsV1NotificationIdReadPatchRequest;

  try {
    const data = await api.notificationsV1NotificationIdReadPatch(body);
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
| **notificationId** | `string` |  | [Defaults to `undefined`] |

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
| **204** | Notification marked as read |  -  |
| **401** | Unauthorized |  -  |
| **404** | Notification not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## notificationsV1ReadAllPatch

> notificationsV1ReadAllPatch()

Mark all notifications as read

Marks all of the user\&#39;s notifications as read

### Example

```ts
import {
  Configuration,
  NotificationsApi,
} from '@briskstack/platform';
import type { NotificationsV1ReadAllPatchRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new NotificationsApi(config);

  try {
    const data = await api.notificationsV1ReadAllPatch();
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

`void` (Empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | All notifications marked as read |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## notificationsV1SendPost

> SendNotificationResponse notificationsV1SendPost(sendNotificationRequest)

Send notification

Creates a new notification for a user (typically called by other services)

### Example

```ts
import {
  Configuration,
  NotificationsApi,
} from '@briskstack/platform';
import type { NotificationsV1SendPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new NotificationsApi(config);

  const body = {
    // SendNotificationRequest (optional)
    sendNotificationRequest: ...,
  } satisfies NotificationsV1SendPostRequest;

  try {
    const data = await api.notificationsV1SendPost(body);
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
| **sendNotificationRequest** | [SendNotificationRequest](SendNotificationRequest.md) |  | [Optional] |

### Return type

[**SendNotificationResponse**](SendNotificationResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Notification sent |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

