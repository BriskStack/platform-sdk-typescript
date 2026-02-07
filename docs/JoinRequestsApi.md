# JoinRequestsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**groupsV1GroupsGroupIdJoinRequestsPost**](JoinRequestsApi.md#groupsv1groupsgroupidjoinrequestspostoperation) | **POST** /groups/v1/groups/{groupId}/join-requests | Request to join |



## groupsV1GroupsGroupIdJoinRequestsPost

> GroupMembership groupsV1GroupsGroupIdJoinRequestsPost(groupId, groupsV1GroupsGroupIdJoinRequestsPostRequest)

Request to join

Creates a pending membership for a user to join a group

### Example

```ts
import {
  Configuration,
  JoinRequestsApi,
} from '@briskstack/platform';
import type { GroupsV1GroupsGroupIdJoinRequestsPostOperationRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new JoinRequestsApi(config);

  const body = {
    // string
    groupId: 123e4567-e89b-12d3-a456-426614174000,
    // GroupsV1GroupsGroupIdJoinRequestsPostRequest (optional)
    groupsV1GroupsGroupIdJoinRequestsPostRequest: ...,
  } satisfies GroupsV1GroupsGroupIdJoinRequestsPostOperationRequest;

  try {
    const data = await api.groupsV1GroupsGroupIdJoinRequestsPost(body);
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
| **groupsV1GroupsGroupIdJoinRequestsPostRequest** | [GroupsV1GroupsGroupIdJoinRequestsPostRequest](GroupsV1GroupsGroupIdJoinRequestsPostRequest.md) |  | [Optional] |

### Return type

[**GroupMembership**](GroupMembership.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Join request created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Group not found |  -  |
| **409** | Already a member or pending |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

