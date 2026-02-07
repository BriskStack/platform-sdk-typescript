# StatsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**activityV1StatsGet**](StatsApi.md#activityv1statsget) | **GET** /activity/v1/stats | Get activity stats |



## activityV1StatsGet

> StatsResponse activityV1StatsGet(userId, period, from, to, activityTypes, includeDaily, includeComparison)

Get activity stats

Returns aggregated activity statistics for a user over a time period

### Example

```ts
import {
  Configuration,
  StatsApi,
} from '@briskstack/platform';
import type { ActivityV1StatsGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new StatsApi(config);

  const body = {
    // string
    userId: 123e4567-e89b-12d3-a456-426614174001,
    // 'today' | 'week' | 'month' | 'custom' (optional)
    period: week,
    // string (optional)
    from: 2025-01-01,
    // string (optional)
    to: 2025-01-31,
    // string (optional)
    activityTypes: reading,study,
    // 'true' | 'false' (optional)
    includeDaily: true,
    // 'true' | 'false' (optional)
    includeComparison: true,
  } satisfies ActivityV1StatsGetRequest;

  try {
    const data = await api.activityV1StatsGet(body);
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
| **period** | `today`, `week`, `month`, `custom` |  | [Optional] [Defaults to `undefined`] [Enum: today, week, month, custom] |
| **from** | `string` |  | [Optional] [Defaults to `undefined`] |
| **to** | `string` |  | [Optional] [Defaults to `undefined`] |
| **activityTypes** | `string` |  | [Optional] [Defaults to `undefined`] |
| **includeDaily** | `true`, `false` |  | [Optional] [Defaults to `undefined`] [Enum: true, false] |
| **includeComparison** | `true`, `false` |  | [Optional] [Defaults to `undefined`] [Enum: true, false] |

### Return type

[**StatsResponse**](StatsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Activity stats |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

