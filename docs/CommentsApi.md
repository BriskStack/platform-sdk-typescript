# CommentsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**feedV1ItemsItemIdCommentsCommentIdDelete**](CommentsApi.md#feedv1itemsitemidcommentscommentiddelete) | **DELETE** /feed/v1/items/{itemId}/comments/{commentId} | Delete comment |
| [**feedV1ItemsItemIdCommentsGet**](CommentsApi.md#feedv1itemsitemidcommentsget) | **GET** /feed/v1/items/{itemId}/comments | List comments |
| [**feedV1ItemsItemIdCommentsPost**](CommentsApi.md#feedv1itemsitemidcommentspost) | **POST** /feed/v1/items/{itemId}/comments | Add comment |



## feedV1ItemsItemIdCommentsCommentIdDelete

> feedV1ItemsItemIdCommentsCommentIdDelete(itemId, commentId)

Delete comment

Deletes a comment (only the comment owner can delete)

### Example

```ts
import {
  Configuration,
  CommentsApi,
} from '@briskstack/platform';
import type { FeedV1ItemsItemIdCommentsCommentIdDeleteRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CommentsApi(config);

  const body = {
    // string
    itemId: 123e4567-e89b-12d3-a456-426614174000,
    // string
    commentId: 123e4567-e89b-12d3-a456-426614174003,
  } satisfies FeedV1ItemsItemIdCommentsCommentIdDeleteRequest;

  try {
    const data = await api.feedV1ItemsItemIdCommentsCommentIdDelete(body);
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
| **itemId** | `string` |  | [Defaults to `undefined`] |
| **commentId** | `string` |  | [Defaults to `undefined`] |

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
| **204** | Comment deleted |  -  |
| **401** | Unauthorized |  -  |
| **403** | Not the comment owner |  -  |
| **404** | Comment not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## feedV1ItemsItemIdCommentsGet

> CommentListResponse feedV1ItemsItemIdCommentsGet(itemId, limit, cursor)

List comments

Returns comments for a feed item

### Example

```ts
import {
  Configuration,
  CommentsApi,
} from '@briskstack/platform';
import type { FeedV1ItemsItemIdCommentsGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CommentsApi(config);

  const body = {
    // string
    itemId: 123e4567-e89b-12d3-a456-426614174000,
    // string (optional)
    limit: 20,
    // string (optional)
    cursor: 2025-01-15T10:00:00Z_123e4567,
  } satisfies FeedV1ItemsItemIdCommentsGetRequest;

  try {
    const data = await api.feedV1ItemsItemIdCommentsGet(body);
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
| **itemId** | `string` |  | [Defaults to `undefined`] |
| **limit** | `string` |  | [Optional] [Defaults to `undefined`] |
| **cursor** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**CommentListResponse**](CommentListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Comments |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Feed item not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## feedV1ItemsItemIdCommentsPost

> Comment feedV1ItemsItemIdCommentsPost(itemId, createCommentRequest)

Add comment

Adds a comment to a feed item

### Example

```ts
import {
  Configuration,
  CommentsApi,
} from '@briskstack/platform';
import type { FeedV1ItemsItemIdCommentsPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new CommentsApi(config);

  const body = {
    // string
    itemId: 123e4567-e89b-12d3-a456-426614174000,
    // CreateCommentRequest (optional)
    createCommentRequest: ...,
  } satisfies FeedV1ItemsItemIdCommentsPostRequest;

  try {
    const data = await api.feedV1ItemsItemIdCommentsPost(body);
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
| **itemId** | `string` |  | [Defaults to `undefined`] |
| **createCommentRequest** | [CreateCommentRequest](CreateCommentRequest.md) |  | [Optional] |

### Return type

[**Comment**](Comment.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Comment created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Feed item not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

