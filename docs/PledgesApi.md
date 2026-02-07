# PledgesApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**gamificationV1PledgesGet**](PledgesApi.md#gamificationv1pledgesget) | **GET** /gamification/v1/pledges | List pledges |
| [**gamificationV1PledgesPledgeIdGet**](PledgesApi.md#gamificationv1pledgespledgeidget) | **GET** /gamification/v1/pledges/{pledgeId} | Get pledge |
| [**gamificationV1PledgesPledgeIdPatch**](PledgesApi.md#gamificationv1pledgespledgeidpatch) | **PATCH** /gamification/v1/pledges/{pledgeId} | Update pledge |
| [**gamificationV1PledgesPost**](PledgesApi.md#gamificationv1pledgespost) | **POST** /gamification/v1/pledges | Create pledge |



## gamificationV1PledgesGet

> PledgeListResponse gamificationV1PledgesGet(goalId, sponsorId)

List pledges

Returns pledges (filtered by goal or sponsor)

### Example

```ts
import {
  Configuration,
  PledgesApi,
} from '@briskstack/platform';
import type { GamificationV1PledgesGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new PledgesApi(config);

  const body = {
    // string (optional)
    goalId: 123e4567-e89b-12d3-a456-426614174000,
    // string (optional)
    sponsorId: 123e4567-e89b-12d3-a456-426614174001,
  } satisfies GamificationV1PledgesGetRequest;

  try {
    const data = await api.gamificationV1PledgesGet(body);
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
| **goalId** | `string` |  | [Optional] [Defaults to `undefined`] |
| **sponsorId** | `string` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**PledgeListResponse**](PledgeListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pledges list |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1PledgesPledgeIdGet

> SponsorPledge gamificationV1PledgesPledgeIdGet(pledgeId)

Get pledge

Returns a specific pledge by ID

### Example

```ts
import {
  Configuration,
  PledgesApi,
} from '@briskstack/platform';
import type { GamificationV1PledgesPledgeIdGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new PledgesApi(config);

  const body = {
    // string
    pledgeId: 123e4567-e89b-12d3-a456-426614174000,
  } satisfies GamificationV1PledgesPledgeIdGetRequest;

  try {
    const data = await api.gamificationV1PledgesPledgeIdGet(body);
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
| **pledgeId** | `string` |  | [Defaults to `undefined`] |

### Return type

[**SponsorPledge**](SponsorPledge.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pledge details |  -  |
| **401** | Unauthorized |  -  |
| **404** | Pledge not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1PledgesPledgeIdPatch

> SponsorPledge gamificationV1PledgesPledgeIdPatch(pledgeId, updatePledgeRequest)

Update pledge

Updates pledge status or payment info

### Example

```ts
import {
  Configuration,
  PledgesApi,
} from '@briskstack/platform';
import type { GamificationV1PledgesPledgeIdPatchRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new PledgesApi(config);

  const body = {
    // string
    pledgeId: 123e4567-e89b-12d3-a456-426614174000,
    // UpdatePledgeRequest (optional)
    updatePledgeRequest: ...,
  } satisfies GamificationV1PledgesPledgeIdPatchRequest;

  try {
    const data = await api.gamificationV1PledgesPledgeIdPatch(body);
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
| **pledgeId** | `string` |  | [Defaults to `undefined`] |
| **updatePledgeRequest** | [UpdatePledgeRequest](UpdatePledgeRequest.md) |  | [Optional] |

### Return type

[**SponsorPledge**](SponsorPledge.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Pledge updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Pledge not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## gamificationV1PledgesPost

> SponsorPledge gamificationV1PledgesPost(createPledgeRequest)

Create pledge

Creates a sponsor pledge for a goal

### Example

```ts
import {
  Configuration,
  PledgesApi,
} from '@briskstack/platform';
import type { GamificationV1PledgesPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new PledgesApi(config);

  const body = {
    // CreatePledgeRequest (optional)
    createPledgeRequest: ...,
  } satisfies GamificationV1PledgesPostRequest;

  try {
    const data = await api.gamificationV1PledgesPost(body);
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
| **createPledgeRequest** | [CreatePledgeRequest](CreatePledgeRequest.md) |  | [Optional] |

### Return type

[**SponsorPledge**](SponsorPledge.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Pledge created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Goal not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

