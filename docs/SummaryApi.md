# SummaryApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**gamificationV1SummaryGet**](SummaryApi.md#gamificationv1summaryget) | **GET** /gamification/v1/summary | Get gamification summary |



## gamificationV1SummaryGet

> GamificationSummary gamificationV1SummaryGet(userId)

Get gamification summary

Returns complete gamification status for a user (XP, streaks, badges)

### Example

```ts
import {
  Configuration,
  SummaryApi,
} from '@briskstack/platform';
import type { GamificationV1SummaryGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new SummaryApi(config);

  const body = {
    // string
    userId: 123e4567-e89b-12d3-a456-426614174001,
  } satisfies GamificationV1SummaryGetRequest;

  try {
    const data = await api.gamificationV1SummaryGet(body);
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

[**GamificationSummary**](GamificationSummary.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Gamification summary |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

