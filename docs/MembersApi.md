# MembersApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**groupsV1GroupsGroupIdMembersGet**](MembersApi.md#groupsv1groupsgroupidmembersget) | **GET** /groups/v1/groups/{groupId}/members | Get members |
| [**groupsV1GroupsGroupIdMembersPost**](MembersApi.md#groupsv1groupsgroupidmemberspost) | **POST** /groups/v1/groups/{groupId}/members | Add member |
| [**groupsV1GroupsGroupIdMembersUserIdDelete**](MembersApi.md#groupsv1groupsgroupidmembersuseriddelete) | **DELETE** /groups/v1/groups/{groupId}/members/{userId} | Remove member |
| [**groupsV1GroupsGroupIdMembersUserIdPatch**](MembersApi.md#groupsv1groupsgroupidmembersuseridpatch) | **PATCH** /groups/v1/groups/{groupId}/members/{userId} | Update member |



## groupsV1GroupsGroupIdMembersGet

> MemberListResponse groupsV1GroupsGroupIdMembersGet(groupId, status)

Get members

Returns all members of a group

### Example

```ts
import {
  Configuration,
  MembersApi,
} from '@briskstack/platform';
import type { GroupsV1GroupsGroupIdMembersGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new MembersApi(config);

  const body = {
    // string
    groupId: 123e4567-e89b-12d3-a456-426614174000,
    // 'active' | 'pending' | 'rejected' (optional)
    status: active,
  } satisfies GroupsV1GroupsGroupIdMembersGetRequest;

  try {
    const data = await api.groupsV1GroupsGroupIdMembersGet(body);
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
| **status** | `active`, `pending`, `rejected` |  | [Optional] [Defaults to `undefined`] [Enum: active, pending, rejected] |

### Return type

[**MemberListResponse**](MemberListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Group members |  -  |
| **401** | Unauthorized |  -  |
| **404** | Group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## groupsV1GroupsGroupIdMembersPost

> GroupMembership groupsV1GroupsGroupIdMembersPost(groupId, addMemberRequest)

Add member

Adds a user to a group

### Example

```ts
import {
  Configuration,
  MembersApi,
} from '@briskstack/platform';
import type { GroupsV1GroupsGroupIdMembersPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new MembersApi(config);

  const body = {
    // string
    groupId: 123e4567-e89b-12d3-a456-426614174000,
    // AddMemberRequest (optional)
    addMemberRequest: ...,
  } satisfies GroupsV1GroupsGroupIdMembersPostRequest;

  try {
    const data = await api.groupsV1GroupsGroupIdMembersPost(body);
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
| **addMemberRequest** | [AddMemberRequest](AddMemberRequest.md) |  | [Optional] |

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
| **201** | Member added |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Group not found |  -  |
| **409** | User already a member |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## groupsV1GroupsGroupIdMembersUserIdDelete

> groupsV1GroupsGroupIdMembersUserIdDelete(groupId, userId)

Remove member

Removes a user from a group

### Example

```ts
import {
  Configuration,
  MembersApi,
} from '@briskstack/platform';
import type { GroupsV1GroupsGroupIdMembersUserIdDeleteRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new MembersApi(config);

  const body = {
    // string
    groupId: 123e4567-e89b-12d3-a456-426614174000,
    // string
    userId: 123e4567-e89b-12d3-a456-426614174001,
  } satisfies GroupsV1GroupsGroupIdMembersUserIdDeleteRequest;

  try {
    const data = await api.groupsV1GroupsGroupIdMembersUserIdDelete(body);
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
| **userId** | `string` |  | [Defaults to `undefined`] |

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
| **204** | Member removed |  -  |
| **401** | Unauthorized |  -  |
| **404** | Member not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## groupsV1GroupsGroupIdMembersUserIdPatch

> GroupMembership groupsV1GroupsGroupIdMembersUserIdPatch(groupId, userId, updateMemberRequest)

Update member

Updates a member role or status

### Example

```ts
import {
  Configuration,
  MembersApi,
} from '@briskstack/platform';
import type { GroupsV1GroupsGroupIdMembersUserIdPatchRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new MembersApi(config);

  const body = {
    // string
    groupId: 123e4567-e89b-12d3-a456-426614174000,
    // string
    userId: 123e4567-e89b-12d3-a456-426614174001,
    // UpdateMemberRequest (optional)
    updateMemberRequest: ...,
  } satisfies GroupsV1GroupsGroupIdMembersUserIdPatchRequest;

  try {
    const data = await api.groupsV1GroupsGroupIdMembersUserIdPatch(body);
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
| **userId** | `string` |  | [Defaults to `undefined`] |
| **updateMemberRequest** | [UpdateMemberRequest](UpdateMemberRequest.md) |  | [Optional] |

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
| **200** | Member updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Member not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

