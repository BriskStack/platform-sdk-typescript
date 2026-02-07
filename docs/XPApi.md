# XPApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**gamificationV1XpGet**](XPApi.md#gamificationv1xpget) | **GET** /gamification/v1/xp | Get user XP |
| [**gamificationV1XpPost**](XPApi.md#gamificationv1xppost) | **POST** /gamification/v1/xp | Award XP |



## gamificationV1XpGet

> UserXpResponse gamificationV1XpGet(userId)

Get user XP

Returns user\&#39;s XP total, level, and progress

### Example

```ts
import {
  Configuration,
  XPApi,
} from '@briskstack/platform';
import type { GamificationV1XpGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new XPApi(config);

  const body = {
    // string
    userId: 123e4567-e89b-12d3-a456-426614174001,
  } satisfies GamificationV1XpGetRequest;

  try {
    const data = await api.gamificationV1XpGet(body);
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

[**UserXpResponse**](UserXpResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User XP info |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1XpPost

> AwardXpResponse gamificationV1XpPost(awardXpRequest)

Award XP

Awards XP to a user, updates totals, checks for badge unlocks

### Example

```ts
import {
  Configuration,
  XPApi,
} from '@briskstack/platform';
import type { GamificationV1XpPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new XPApi(config);

  const body = {
    // AwardXpRequest (optional)
    awardXpRequest: ...,
  } satisfies GamificationV1XpPostRequest;

  try {
    const data = await api.gamificationV1XpPost(body);
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
| **awardXpRequest** | [AwardXpRequest](AwardXpRequest.md) |  | [Optional] |

### Return type

[**AwardXpResponse**](AwardXpResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | XP awarded |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

