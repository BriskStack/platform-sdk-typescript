# BadgesApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**gamificationV1BadgesAwardPost**](BadgesApi.md#gamificationv1badgesawardpost) | **POST** /gamification/v1/badges/award | Award badge |
| [**gamificationV1BadgesGet**](BadgesApi.md#gamificationv1badgesget) | **GET** /gamification/v1/badges | List badges |
| [**gamificationV1BadgesPost**](BadgesApi.md#gamificationv1badgespost) | **POST** /gamification/v1/badges | Create badge |
| [**gamificationV1BadgesUserGet**](BadgesApi.md#gamificationv1badgesuserget) | **GET** /gamification/v1/badges/user | Get user badges |



## gamificationV1BadgesAwardPost

> UserBadge gamificationV1BadgesAwardPost(awardBadgeRequest)

Award badge

Manually awards a badge to a user

### Example

```ts
import {
  Configuration,
  BadgesApi,
} from '@briskstack/platform';
import type { GamificationV1BadgesAwardPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new BadgesApi(config);

  const body = {
    // AwardBadgeRequest (optional)
    awardBadgeRequest: ...,
  } satisfies GamificationV1BadgesAwardPostRequest;

  try {
    const data = await api.gamificationV1BadgesAwardPost(body);
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
| **awardBadgeRequest** | [AwardBadgeRequest](AwardBadgeRequest.md) |  | [Optional] |

### Return type

[**UserBadge**](UserBadge.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Badge awarded |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Badge not found |  -  |
| **409** | User already has badge |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1BadgesGet

> BadgeListResponse gamificationV1BadgesGet(category)

List badges

Returns all badge definitions for this venture

### Example

```ts
import {
  Configuration,
  BadgesApi,
} from '@briskstack/platform';
import type { GamificationV1BadgesGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new BadgesApi(config);

  const body = {
    // string (optional)
    category: achievement,
  } satisfies GamificationV1BadgesGetRequest;

  try {
    const data = await api.gamificationV1BadgesGet(body);
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
| **category** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**BadgeListResponse**](BadgeListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Badge definitions |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1BadgesPost

> Badge gamificationV1BadgesPost(createBadgeRequest)

Create badge

Creates a new badge definition for this venture

### Example

```ts
import {
  Configuration,
  BadgesApi,
} from '@briskstack/platform';
import type { GamificationV1BadgesPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new BadgesApi(config);

  const body = {
    // CreateBadgeRequest (optional)
    createBadgeRequest: ...,
  } satisfies GamificationV1BadgesPostRequest;

  try {
    const data = await api.gamificationV1BadgesPost(body);
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
| **createBadgeRequest** | [CreateBadgeRequest](CreateBadgeRequest.md) |  | [Optional] |

### Return type

[**Badge**](Badge.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Badge created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **409** | Badge code already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1BadgesUserGet

> UserBadgeListResponse gamificationV1BadgesUserGet(userId)

Get user badges

Returns all badges earned by a user

### Example

```ts
import {
  Configuration,
  BadgesApi,
} from '@briskstack/platform';
import type { GamificationV1BadgesUserGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new BadgesApi(config);

  const body = {
    // string
    userId: 123e4567-e89b-12d3-a456-426614174001,
  } satisfies GamificationV1BadgesUserGetRequest;

  try {
    const data = await api.gamificationV1BadgesUserGet(body);
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

[**UserBadgeListResponse**](UserBadgeListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User badges |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

