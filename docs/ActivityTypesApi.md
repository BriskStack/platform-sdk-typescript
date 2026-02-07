# ActivityTypesApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**activityV1TypesGet**](ActivityTypesApi.md#activityv1typesget) | **GET** /activity/v1/types | List activity types |
| [**activityV1TypesPost**](ActivityTypesApi.md#activityv1typespost) | **POST** /activity/v1/types | Create activity type |



## activityV1TypesGet

> ActivityTypeListResponse activityV1TypesGet()

List activity types

Returns all activity types registered for this venture

### Example

```ts
import {
  Configuration,
  ActivityTypesApi,
} from '@briskstack/platform';
import type { ActivityV1TypesGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ActivityTypesApi(config);

  try {
    const data = await api.activityV1TypesGet();
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

[**ActivityTypeListResponse**](ActivityTypeListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Activity types list |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## activityV1TypesPost

> ActivityType activityV1TypesPost(createActivityTypeRequest)

Create activity type

Registers a new activity type for this venture

### Example

```ts
import {
  Configuration,
  ActivityTypesApi,
} from '@briskstack/platform';
import type { ActivityV1TypesPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ActivityTypesApi(config);

  const body = {
    // CreateActivityTypeRequest (optional)
    createActivityTypeRequest: ...,
  } satisfies ActivityV1TypesPostRequest;

  try {
    const data = await api.activityV1TypesPost(body);
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
| **createActivityTypeRequest** | [CreateActivityTypeRequest](CreateActivityTypeRequest.md) |  | [Optional] |

### Return type

[**ActivityType**](ActivityType.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Activity type created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **409** | Activity type code already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

