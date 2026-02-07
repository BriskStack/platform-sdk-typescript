# LeaderboardsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**gamificationV1LeaderboardGet**](LeaderboardsApi.md#gamificationv1leaderboardget) | **GET** /gamification/v1/leaderboard | Get leaderboard |
| [**gamificationV1LeaderboardsGet**](LeaderboardsApi.md#gamificationv1leaderboardsget) | **GET** /gamification/v1/leaderboards | Get user leaderboards |



## gamificationV1LeaderboardGet

> LeaderboardResponse gamificationV1LeaderboardGet(groupId, period, limit)

Get leaderboard

Returns rankings for users within a group

### Example

```ts
import {
  Configuration,
  LeaderboardsApi,
} from '@briskstack/platform';
import type { GamificationV1LeaderboardGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LeaderboardsApi(config);

  const body = {
    // string
    groupId: 123e4567-e89b-12d3-a456-426614174000,
    // 'today' | 'week' | 'month' | 'all' (optional)
    period: week,
    // number (optional)
    limit: 10,
  } satisfies GamificationV1LeaderboardGetRequest;

  try {
    const data = await api.gamificationV1LeaderboardGet(body);
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
| **groupId** | `string` |  | [Defaults to `undefined`] |
| **period** | `today`, `week`, `month`, `all` |  | [Optional] [Defaults to `undefined`] [Enum: today, week, month, all] |
| **limit** | `number` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**LeaderboardResponse**](LeaderboardResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Leaderboard rankings |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1LeaderboardsGet

> UserLeaderboardsResponse gamificationV1LeaderboardsGet(userId)

Get user leaderboards

Returns user\&#39;s rank across all their groups

### Example

```ts
import {
  Configuration,
  LeaderboardsApi,
} from '@briskstack/platform';
import type { GamificationV1LeaderboardsGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new LeaderboardsApi(config);

  const body = {
    // string
    userId: 123e4567-e89b-12d3-a456-426614174001,
  } satisfies GamificationV1LeaderboardsGetRequest;

  try {
    const data = await api.gamificationV1LeaderboardsGet(body);
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

[**UserLeaderboardsResponse**](UserLeaderboardsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User leaderboard positions |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

