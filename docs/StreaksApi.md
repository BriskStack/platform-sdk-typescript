# StreaksApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**gamificationV1StreaksGet**](StreaksApi.md#gamificationv1streaksget) | **GET** /gamification/v1/streaks | Get user streaks |
| [**gamificationV1StreaksPost**](StreaksApi.md#gamificationv1streakspost) | **POST** /gamification/v1/streaks | Update streak |



## gamificationV1StreaksGet

> StreakListResponse gamificationV1StreaksGet(userId)

Get user streaks

Returns all streaks for a user

### Example

```ts
import {
  Configuration,
  StreaksApi,
} from '@briskstack/platform';
import type { GamificationV1StreaksGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new StreaksApi(config);

  const body = {
    // string
    userId: 123e4567-e89b-12d3-a456-426614174001,
  } satisfies GamificationV1StreaksGetRequest;

  try {
    const data = await api.gamificationV1StreaksGet(body);
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

### Return type

[**StreakListResponse**](StreakListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User streaks |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1StreaksPost

> UpdateStreakResponse gamificationV1StreaksPost(updateStreakRequest)

Update streak

Updates a streak based on activity. Creates streak if not exists.

### Example

```ts
import {
  Configuration,
  StreaksApi,
} from '@briskstack/platform';
import type { GamificationV1StreaksPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new StreaksApi(config);

  const body = {
    // UpdateStreakRequest (optional)
    updateStreakRequest: ...,
  } satisfies GamificationV1StreaksPostRequest;

  try {
    const data = await api.gamificationV1StreaksPost(body);
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
| **updateStreakRequest** | [UpdateStreakRequest](UpdateStreakRequest.md) |  | [Optional] |

### Return type

[**UpdateStreakResponse**](UpdateStreakResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Streak updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

