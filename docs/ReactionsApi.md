# ReactionsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**feedV1ItemsItemIdReactionsPost**](ReactionsApi.md#feedv1itemsitemidreactionspost) | **POST** /feed/v1/items/{itemId}/reactions | Toggle reaction |



## feedV1ItemsItemIdReactionsPost

> ToggleReactionResponse feedV1ItemsItemIdReactionsPost(itemId, toggleReactionRequest)

Toggle reaction

Adds a reaction if not exists, removes if exists (toggle behavior)

### Example

```ts
import {
  Configuration,
  ReactionsApi,
} from '@briskstack/platform';
import type { FeedV1ItemsItemIdReactionsPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ReactionsApi(config);

  const body = {
    // string
    itemId: 123e4567-e89b-12d3-a456-426614174000,
    // ToggleReactionRequest (optional)
    toggleReactionRequest: ...,
  } satisfies FeedV1ItemsItemIdReactionsPostRequest;

  try {
    const data = await api.feedV1ItemsItemIdReactionsPost(body);
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
| **toggleReactionRequest** | [ToggleReactionRequest](ToggleReactionRequest.md) |  | [Optional] |

### Return type

[**ToggleReactionResponse**](ToggleReactionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Reaction toggled |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Feed item not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

