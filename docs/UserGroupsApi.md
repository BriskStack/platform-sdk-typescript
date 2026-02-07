# UserGroupsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**groupsV1UsersUserIdGroupsGet**](UserGroupsApi.md#groupsv1usersuseridgroupsget) | **GET** /groups/v1/users/{userId}/groups | Get user groups |



## groupsV1UsersUserIdGroupsGet

> UserGroupsResponse groupsV1UsersUserIdGroupsGet(userId, groupType, status)

Get user groups

Returns all groups a user belongs to

### Example

```ts
import {
  Configuration,
  UserGroupsApi,
} from '@briskstack/platform';
import type { GroupsV1UsersUserIdGroupsGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new UserGroupsApi(config);

  const body = {
    // string
    userId: 123e4567-e89b-12d3-a456-426614174001,
    // string (optional)
    groupType: family,
    // 'active' | 'pending' | 'rejected' (optional)
    status: active,
  } satisfies GroupsV1UsersUserIdGroupsGetRequest;

  try {
    const data = await api.groupsV1UsersUserIdGroupsGet(body);
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
| **groupType** | `string` |  | [Optional] [Defaults to `undefined`] |
| **status** | `active`, `pending`, `rejected` |  | [Optional] [Defaults to `undefined`] [Enum: active, pending, rejected] |

### Return type

[**UserGroupsResponse**](UserGroupsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | User groups |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

