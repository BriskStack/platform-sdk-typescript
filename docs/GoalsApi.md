# GoalsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**gamificationV1GoalsGet**](GoalsApi.md#gamificationv1goalsget) | **GET** /gamification/v1/goals | List goals |
| [**gamificationV1GoalsGoalIdGet**](GoalsApi.md#gamificationv1goalsgoalidget) | **GET** /gamification/v1/goals/{goalId} | Get goal with pledges |
| [**gamificationV1GoalsGoalIdPatch**](GoalsApi.md#gamificationv1goalsgoalidpatch) | **PATCH** /gamification/v1/goals/{goalId} | Update goal |
| [**gamificationV1GoalsPost**](GoalsApi.md#gamificationv1goalspost) | **POST** /gamification/v1/goals | Create goal |



## gamificationV1GoalsGet

> GoalListResponse gamificationV1GoalsGet(userId, status)

List goals

Returns goals for a user (optionally filtered by status)

### Example

```ts
import {
  Configuration,
  GoalsApi,
} from '@briskstack/platform';
import type { GamificationV1GoalsGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new GoalsApi(config);

  const body = {
    // string
    userId: 123e4567-e89b-12d3-a456-426614174001,
    // 'active' | 'completed' | 'expired' | 'cancelled' (optional)
    status: active,
  } satisfies GamificationV1GoalsGetRequest;

  try {
    const data = await api.gamificationV1GoalsGet(body);
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
| **status** | `active`, `completed`, `expired`, `cancelled` |  | [Optional] [Defaults to `undefined`] [Enum: active, completed, expired, cancelled] |

### Return type

[**GoalListResponse**](GoalListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Goals list |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1GoalsGoalIdGet

> GoalWithPledges gamificationV1GoalsGoalIdGet(goalId)

Get goal with pledges

Returns a specific goal with all its pledges

### Example

```ts
import {
  Configuration,
  GoalsApi,
} from '@briskstack/platform';
import type { GamificationV1GoalsGoalIdGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new GoalsApi(config);

  const body = {
    // string
    goalId: 123e4567-e89b-12d3-a456-426614174000,
  } satisfies GamificationV1GoalsGoalIdGetRequest;

  try {
    const data = await api.gamificationV1GoalsGoalIdGet(body);
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
| **goalId** | `string` |  | [Defaults to `undefined`] |

### Return type

[**GoalWithPledges**](GoalWithPledges.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Goal with pledges |  -  |
| **401** | Unauthorized |  -  |
| **404** | Goal not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1GoalsGoalIdPatch

> Goal gamificationV1GoalsGoalIdPatch(goalId, updateGoalRequest)

Update goal

Updates goal progress or status

### Example

```ts
import {
  Configuration,
  GoalsApi,
} from '@briskstack/platform';
import type { GamificationV1GoalsGoalIdPatchRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new GoalsApi(config);

  const body = {
    // string
    goalId: 123e4567-e89b-12d3-a456-426614174000,
    // UpdateGoalRequest (optional)
    updateGoalRequest: ...,
  } satisfies GamificationV1GoalsGoalIdPatchRequest;

  try {
    const data = await api.gamificationV1GoalsGoalIdPatch(body);
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
| **goalId** | `string` |  | [Defaults to `undefined`] |
| **updateGoalRequest** | [UpdateGoalRequest](UpdateGoalRequest.md) |  | [Optional] |

### Return type

[**Goal**](Goal.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Goal updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Goal not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1GoalsPost

> Goal gamificationV1GoalsPost(createGoalRequest)

Create goal

Creates a new goal for a user with optional reward

### Example

```ts
import {
  Configuration,
  GoalsApi,
} from '@briskstack/platform';
import type { GamificationV1GoalsPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new GoalsApi(config);

  const body = {
    // CreateGoalRequest (optional)
    createGoalRequest: ...,
  } satisfies GamificationV1GoalsPostRequest;

  try {
    const data = await api.gamificationV1GoalsPost(body);
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
| **createGoalRequest** | [CreateGoalRequest](CreateGoalRequest.md) |  | [Optional] |

### Return type

[**Goal**](Goal.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Goal created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

