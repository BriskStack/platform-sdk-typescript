# FeedItemsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**feedV1FeedGet**](FeedItemsApi.md#feedv1feedget) | **GET** /feed/v1/feed | Get aggregated feed |
| [**feedV1GroupsGroupIdFeedGet**](FeedItemsApi.md#feedv1groupsgroupidfeedget) | **GET** /feed/v1/groups/{groupId}/feed | Get group feed |
| [**feedV1ItemsPost**](FeedItemsApi.md#feedv1itemspost) | **POST** /feed/v1/items | Create feed item |
| [**feedV1UsersUserIdFeedGet**](FeedItemsApi.md#feedv1usersuseridfeedget) | **GET** /feed/v1/users/{userId}/feed | Get user\&#39;s own feed |



## feedV1FeedGet

> FeedListResponse feedV1FeedGet(limit, cursor, groupIds, types)

Get aggregated feed

Returns feed items from all groups the user belongs to, or filtered groups

### Example

```ts
import {
  Configuration,
  FeedItemsApi,
} from '@briskstack/platform';
import type { FeedV1FeedGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new FeedItemsApi(config);

  const body = {
    // string (optional)
    limit: 20,
    // string (optional)
    cursor: 2025-01-15T10:00:00Z_123e4567,
    // string (optional)
    groupIds: 123e4567-e89b-12d3-a456-426614174002,223e4567-e89b-12d3-a456-426614174003,
    // string (optional)
    types: book_finished,goal_completed,
  } satisfies FeedV1FeedGetRequest;

  try {
    const data = await api.feedV1FeedGet(body);
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
| **groupIds** | `string` |  | [Optional] [Defaults to `undefined`] |
| **types** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**FeedListResponse**](FeedListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Feed items |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## feedV1GroupsGroupIdFeedGet

> FeedListResponse feedV1GroupsGroupIdFeedGet(groupId, limit, cursor, types)

Get group feed

Returns feed items for a specific group (family, team, etc.)

### Example

```ts
import {
  Configuration,
  FeedItemsApi,
} from '@briskstack/platform';
import type { FeedV1GroupsGroupIdFeedGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new FeedItemsApi(config);

  const body = {
    // string
    groupId: 123e4567-e89b-12d3-a456-426614174002,
    // string (optional)
    limit: 20,
    // string (optional)
    cursor: 2025-01-15T10:00:00Z_123e4567,
    // string (optional)
    types: book_finished,goal_completed,
  } satisfies FeedV1GroupsGroupIdFeedGetRequest;

  try {
    const data = await api.feedV1GroupsGroupIdFeedGet(body);
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
| **limit** | `string` |  | [Optional] [Defaults to `undefined`] |
| **cursor** | `string` |  | [Optional] [Defaults to `undefined`] |
| **types** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**FeedListResponse**](FeedListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Feed items |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Not a member of this group |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## feedV1ItemsPost

> CreateFeedItemResponse feedV1ItemsPost(createFeedItemRequest)

Create feed item

Creates a new feed item for social display

### Example

```ts
import {
  Configuration,
  FeedItemsApi,
} from '@briskstack/platform';
import type { FeedV1ItemsPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new FeedItemsApi(config);

  const body = {
    // CreateFeedItemRequest (optional)
    createFeedItemRequest: ...,
  } satisfies FeedV1ItemsPostRequest;

  try {
    const data = await api.feedV1ItemsPost(body);
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
| **createFeedItemRequest** | [CreateFeedItemRequest](CreateFeedItemRequest.md) |  | [Optional] |

### Return type

[**CreateFeedItemResponse**](CreateFeedItemResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Feed item created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## feedV1UsersUserIdFeedGet

> FeedListResponse feedV1UsersUserIdFeedGet(userId, limit, cursor, types)

Get user\&#39;s own feed

Returns feed items for a specific user\&#39;s own activities

### Example

```ts
import {
  Configuration,
  FeedItemsApi,
} from '@briskstack/platform';
import type { FeedV1UsersUserIdFeedGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new FeedItemsApi(config);

  const body = {
    // string
    userId: 123e4567-e89b-12d3-a456-426614174001,
    // string (optional)
    limit: 20,
    // string (optional)
    cursor: 2025-01-15T10:00:00Z_123e4567,
    // string (optional)
    types: book_finished,goal_completed,
  } satisfies FeedV1UsersUserIdFeedGetRequest;

  try {
    const data = await api.feedV1UsersUserIdFeedGet(body);
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
| **limit** | `string` |  | [Optional] [Defaults to `undefined`] |
| **cursor** | `string` |  | [Optional] [Defaults to `undefined`] |
| **types** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**FeedListResponse**](FeedListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Feed items |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

