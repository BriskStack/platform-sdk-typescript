# GroupsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**groupsV1GroupsByExternalGet**](GroupsApi.md#groupsv1groupsbyexternalget) | **GET** /groups/v1/groups/by-external | Get group by external ID |
| [**groupsV1GroupsGet**](GroupsApi.md#groupsv1groupsget) | **GET** /groups/v1/groups | List groups |
| [**groupsV1GroupsGroupIdDelete**](GroupsApi.md#groupsv1groupsgroupiddelete) | **DELETE** /groups/v1/groups/{groupId} | Delete group |
| [**groupsV1GroupsGroupIdGet**](GroupsApi.md#groupsv1groupsgroupidget) | **GET** /groups/v1/groups/{groupId} | Get group |
| [**groupsV1GroupsGroupIdPatch**](GroupsApi.md#groupsv1groupsgroupidpatch) | **PATCH** /groups/v1/groups/{groupId} | Update group |
| [**groupsV1GroupsPost**](GroupsApi.md#groupsv1groupspost) | **POST** /groups/v1/groups | Create group |
| [**groupsV1GroupsSearchGet**](GroupsApi.md#groupsv1groupssearchget) | **GET** /groups/v1/groups/search | Search public groups |



## groupsV1GroupsByExternalGet

> Group groupsV1GroupsByExternalGet(groupType, externalId)

Get group by external ID

Returns a group by type and external ID

### Example

```ts
import {
  Configuration,
  GroupsApi,
} from '@briskstack/platform';
import type { GroupsV1GroupsByExternalGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new GroupsApi(config);

  const body = {
    // string
    groupType: family,
    // string
    externalId: bg-family-uuid,
  } satisfies GroupsV1GroupsByExternalGetRequest;

  try {
    const data = await api.groupsV1GroupsByExternalGet(body);
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
| **groupType** | `string` |  | [Defaults to `undefined`] |
| **externalId** | `string` |  | [Defaults to `undefined`] |

### Return type

[**Group**](Group.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Group details |  -  |
| **401** | Unauthorized |  -  |
| **404** | Group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## groupsV1GroupsGet

> GroupListResponse groupsV1GroupsGet(groupType, limit, offset)

List groups

Returns groups for this venture

### Example

```ts
import {
  Configuration,
  GroupsApi,
} from '@briskstack/platform';
import type { GroupsV1GroupsGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new GroupsApi(config);

  const body = {
    // string (optional)
    groupType: family,
    // number (optional)
    limit: 50,
    // number (optional)
    offset: 0,
  } satisfies GroupsV1GroupsGetRequest;

  try {
    const data = await api.groupsV1GroupsGet(body);
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
| **groupType** | `string` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `undefined`] |
| **offset** | `number` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**GroupListResponse**](GroupListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | List of groups |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## groupsV1GroupsGroupIdDelete

> groupsV1GroupsGroupIdDelete(groupId)

Delete group

Deletes a group

### Example

```ts
import {
  Configuration,
  GroupsApi,
} from '@briskstack/platform';
import type { GroupsV1GroupsGroupIdDeleteRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new GroupsApi(config);

  const body = {
    // string
    groupId: 123e4567-e89b-12d3-a456-426614174000,
  } satisfies GroupsV1GroupsGroupIdDeleteRequest;

  try {
    const data = await api.groupsV1GroupsGroupIdDelete(body);
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
| **204** | Group deleted |  -  |
| **401** | Unauthorized |  -  |
| **404** | Group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## groupsV1GroupsGroupIdGet

> Group groupsV1GroupsGroupIdGet(groupId)

Get group

Returns a group by ID

### Example

```ts
import {
  Configuration,
  GroupsApi,
} from '@briskstack/platform';
import type { GroupsV1GroupsGroupIdGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new GroupsApi(config);

  const body = {
    // string
    groupId: 123e4567-e89b-12d3-a456-426614174000,
  } satisfies GroupsV1GroupsGroupIdGetRequest;

  try {
    const data = await api.groupsV1GroupsGroupIdGet(body);
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

### Return type

[**Group**](Group.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Group details |  -  |
| **401** | Unauthorized |  -  |
| **404** | Group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## groupsV1GroupsGroupIdPatch

> Group groupsV1GroupsGroupIdPatch(groupId, updateGroupRequest)

Update group

Updates a group

### Example

```ts
import {
  Configuration,
  GroupsApi,
} from '@briskstack/platform';
import type { GroupsV1GroupsGroupIdPatchRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new GroupsApi(config);

  const body = {
    // string
    groupId: 123e4567-e89b-12d3-a456-426614174000,
    // UpdateGroupRequest (optional)
    updateGroupRequest: ...,
  } satisfies GroupsV1GroupsGroupIdPatchRequest;

  try {
    const data = await api.groupsV1GroupsGroupIdPatch(body);
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
| **updateGroupRequest** | [UpdateGroupRequest](UpdateGroupRequest.md) |  | [Optional] |

### Return type

[**Group**](Group.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Group updated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## groupsV1GroupsPost

> Group groupsV1GroupsPost(createGroupRequest)

Create group

Creates a new group for this venture

### Example

```ts
import {
  Configuration,
  GroupsApi,
} from '@briskstack/platform';
import type { GroupsV1GroupsPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new GroupsApi(config);

  const body = {
    // CreateGroupRequest (optional)
    createGroupRequest: ...,
  } satisfies GroupsV1GroupsPostRequest;

  try {
    const data = await api.groupsV1GroupsPost(body);
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
| **createGroupRequest** | [CreateGroupRequest](CreateGroupRequest.md) |  | [Optional] |

### Return type

[**Group**](Group.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Group created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **409** | Group already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## groupsV1GroupsSearchGet

> GroupListResponse groupsV1GroupsSearchGet(query, groupType, limit, offset)

Search public groups

Search for public/joinable groups

### Example

```ts
import {
  Configuration,
  GroupsApi,
} from '@briskstack/platform';
import type { GroupsV1GroupsSearchGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new GroupsApi(config);

  const body = {
    // string (optional)
    query: Lincoln Elementary,
    // string (optional)
    groupType: school,
    // number (optional)
    limit: 20,
    // number (optional)
    offset: 0,
  } satisfies GroupsV1GroupsSearchGetRequest;

  try {
    const data = await api.groupsV1GroupsSearchGet(body);
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
| **query** | `string` |  | [Optional] [Defaults to `undefined`] |
| **groupType** | `string` |  | [Optional] [Defaults to `undefined`] |
| **limit** | `number` |  | [Optional] [Defaults to `undefined`] |
| **offset** | `number` |  | [Optional] [Defaults to `undefined`] |

### Return type

[**GroupListResponse**](GroupListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Search results |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

