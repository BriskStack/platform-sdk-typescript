# RewardsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**gamificationV1RewardsGet**](RewardsApi.md#gamificationv1rewardsget) | **GET** /gamification/v1/rewards | List rewards |
| [**gamificationV1RewardsPost**](RewardsApi.md#gamificationv1rewardspost) | **POST** /gamification/v1/rewards | Create reward |
| [**gamificationV1RewardsRewardIdFulfillPost**](RewardsApi.md#gamificationv1rewardsrewardidfulfillpost) | **POST** /gamification/v1/rewards/{rewardId}/fulfill | Fulfill reward |
| [**gamificationV1RewardsRewardIdGet**](RewardsApi.md#gamificationv1rewardsrewardidget) | **GET** /gamification/v1/rewards/{rewardId} | Get reward |
| [**gamificationV1RewardsRewardIdPatch**](RewardsApi.md#gamificationv1rewardsrewardidpatch) | **PATCH** /gamification/v1/rewards/{rewardId} | Update reward |



## gamificationV1RewardsGet

> RewardListResponse gamificationV1RewardsGet(providedBy, recipientId, groupId, status)

List rewards

Returns rewards for this venture with optional filters

### Example

```ts
import {
  Configuration,
  RewardsApi,
} from '@briskstack/platform';
import type { GamificationV1RewardsGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RewardsApi(config);

  const body = {
    // string (optional)
    providedBy: 123e4567-e89b-12d3-a456-426614174001,
    // string (optional)
    recipientId: 123e4567-e89b-12d3-a456-426614174010,
    // string (optional)
    groupId: 123e4567-e89b-12d3-a456-426614174020,
    // 'active' | 'fulfilled' | 'cancelled' (optional)
    status: active,
  } satisfies GamificationV1RewardsGetRequest;

  try {
    const data = await api.gamificationV1RewardsGet(body);
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
| **providedBy** | `string` |  | [Optional] [Defaults to `undefined`] |
| **recipientId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **groupId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **status** | `active`, `fulfilled`, `cancelled` |  | [Optional] [Defaults to `undefined`] [Enum: active, fulfilled, cancelled] |

### Return type

[**RewardListResponse**](RewardListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Rewards list |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1RewardsPost

> Reward gamificationV1RewardsPost(createRewardRequest)

Create reward

Creates a new reward definition

### Example

```ts
import {
  Configuration,
  RewardsApi,
} from '@briskstack/platform';
import type { GamificationV1RewardsPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RewardsApi(config);

  const body = {
    // CreateRewardRequest (optional)
    createRewardRequest: ...,
  } satisfies GamificationV1RewardsPostRequest;

  try {
    const data = await api.gamificationV1RewardsPost(body);
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
| **createRewardRequest** | [CreateRewardRequest](CreateRewardRequest.md) |  | [Optional] |

### Return type

[**Reward**](Reward.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Reward created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1RewardsRewardIdFulfillPost

> Reward gamificationV1RewardsRewardIdFulfillPost(rewardId)

Fulfill reward

Marks a reward as fulfilled (delivered to recipient)

### Example

```ts
import {
  Configuration,
  RewardsApi,
} from '@briskstack/platform';
import type { GamificationV1RewardsRewardIdFulfillPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RewardsApi(config);

  const body = {
    // string
    rewardId: 123e4567-e89b-12d3-a456-426614174000,
  } satisfies GamificationV1RewardsRewardIdFulfillPostRequest;

  try {
    const data = await api.gamificationV1RewardsRewardIdFulfillPost(body);
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
| **rewardId** | `string` |  | [Defaults to `undefined`] |

### Return type

[**Reward**](Reward.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reward fulfilled |  -  |
| **400** | Reward not active |  -  |
| **401** | Unauthorized |  -  |
| **404** | Reward not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1RewardsRewardIdGet

> Reward gamificationV1RewardsRewardIdGet(rewardId)

Get reward

Returns a specific reward by ID

### Example

```ts
import {
  Configuration,
  RewardsApi,
} from '@briskstack/platform';
import type { GamificationV1RewardsRewardIdGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RewardsApi(config);

  const body = {
    // string
    rewardId: 123e4567-e89b-12d3-a456-426614174000,
  } satisfies GamificationV1RewardsRewardIdGetRequest;

  try {
    const data = await api.gamificationV1RewardsRewardIdGet(body);
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
| **rewardId** | `string` |  | [Defaults to `undefined`] |

### Return type

[**Reward**](Reward.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reward details |  -  |
| **401** | Unauthorized |  -  |
| **404** | Reward not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1RewardsRewardIdPatch

> Reward gamificationV1RewardsRewardIdPatch(rewardId, updateRewardRequest)

Update reward

Updates a reward (name, description, value, or status)

### Example

```ts
import {
  Configuration,
  RewardsApi,
} from '@briskstack/platform';
import type { GamificationV1RewardsRewardIdPatchRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new RewardsApi(config);

  const body = {
    // string
    rewardId: 123e4567-e89b-12d3-a456-426614174000,
    // UpdateRewardRequest (optional)
    updateRewardRequest: ...,
  } satisfies GamificationV1RewardsRewardIdPatchRequest;

  try {
    const data = await api.gamificationV1RewardsRewardIdPatch(body);
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
| **rewardId** | `string` |  | [Defaults to `undefined`] |
| **updateRewardRequest** | [UpdateRewardRequest](UpdateRewardRequest.md) |  | [Optional] |

### Return type

[**Reward**](Reward.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reward updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Reward not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

