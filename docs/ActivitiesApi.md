# ActivitiesApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**activityV1ActivitiesGet**](ActivitiesApi.md#activityv1activitiesget) | **GET** /activity/v1/activities | List activities |
| [**activityV1ActivitiesPost**](ActivitiesApi.md#activityv1activitiespost) | **POST** /activity/v1/activities | Record activity |



## activityV1ActivitiesGet

> ActivityListResponse activityV1ActivitiesGet(userId, activityType, from, to, limit, offset)

List activities

Returns a paginated list of activities for a user

### Example

```ts
import {
  Configuration,
  ActivitiesApi,
} from '@briskstack/platform';
import type { ActivityV1ActivitiesGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ActivitiesApi(config);

  const body = {
    // string
    userId: 123e4567-e89b-12d3-a456-426614174001,
    // string (optional)
    activityType: reading,
    // string (optional)
    from: 2025-01-01,
    // string (optional)
    to: 2025-01-31,
    // string (optional)
    limit: 50,
    // string (optional)
    offset: 0,
  } satisfies ActivityV1ActivitiesGetRequest;

  try {
    const data = await api.activityV1ActivitiesGet(body);
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
| **activityType** | `string` |  | [Optional] [Defaults to `undefined`] |
| **from** | `string` |  | [Optional] [Defaults to `undefined`] |
| **to** | `string` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `string` |  | [Optional] [Defaults to `undefined`] |
| **offset** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**ActivityListResponse**](ActivityListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Activities list |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## activityV1ActivitiesPost

> RecordActivityResponse activityV1ActivitiesPost(recordActivityRequest)

Record activity

Records a new activity event and updates daily stats

### Example

```ts
import {
  Configuration,
  ActivitiesApi,
} from '@briskstack/platform';
import type { ActivityV1ActivitiesPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ActivitiesApi(config);

  const body = {
    // RecordActivityRequest (optional)
    recordActivityRequest: ...,
  } satisfies ActivityV1ActivitiesPostRequest;

  try {
    const data = await api.activityV1ActivitiesPost(body);
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
| **recordActivityRequest** | [RecordActivityRequest](RecordActivityRequest.md) |  | [Optional] |

### Return type

[**RecordActivityResponse**](RecordActivityResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Activity recorded |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Activity type not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

