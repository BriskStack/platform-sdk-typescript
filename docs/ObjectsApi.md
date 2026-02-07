# ObjectsApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**storageV1DownloadUrlPost**](ObjectsApi.md#storagev1downloadurlpost) | **POST** /storage/v1/download-url | Get signed download URL |
| [**storageV1ObjectDelete**](ObjectsApi.md#storagev1objectdelete) | **DELETE** /storage/v1/object | Delete object |
| [**storageV1ObjectMetaPost**](ObjectsApi.md#storagev1objectmetapost) | **POST** /storage/v1/object/meta | Get object metadata |
| [**storageV1ObjectsPost**](ObjectsApi.md#storagev1objectspost) | **POST** /storage/v1/objects | List objects |
| [**storageV1UploadUrlPost**](ObjectsApi.md#storagev1uploadurlpost) | **POST** /storage/v1/upload-url | Get signed upload URL |



## storageV1DownloadUrlPost

> DownloadUrlResponse storageV1DownloadUrlPost(downloadUrlRequest)

Get signed download URL

Generate a pre-signed URL for downloading an object from R2 storage

### Example

```ts
import {
  Configuration,
  ObjectsApi,
} from '@briskstack/platform';
import type { StorageV1DownloadUrlPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ObjectsApi(config);

  const body = {
    // DownloadUrlRequest (optional)
    downloadUrlRequest: ...,
  } satisfies StorageV1DownloadUrlPostRequest;

  try {
    const data = await api.storageV1DownloadUrlPost(body);
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
| **downloadUrlRequest** | [DownloadUrlRequest](DownloadUrlRequest.md) |  | [Optional] |

### Return type

[**DownloadUrlResponse**](DownloadUrlResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Download URL generated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **404** | Object not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## storageV1ObjectDelete

> DeleteObjectResponse storageV1ObjectDelete(deleteObjectRequest)

Delete object

Delete an object from R2 storage

### Example

```ts
import {
  Configuration,
  ObjectsApi,
} from '@briskstack/platform';
import type { StorageV1ObjectDeleteRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ObjectsApi(config);

  const body = {
    // DeleteObjectRequest (optional)
    deleteObjectRequest: ...,
  } satisfies StorageV1ObjectDeleteRequest;

  try {
    const data = await api.storageV1ObjectDelete(body);
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
| **deleteObjectRequest** | [DeleteObjectRequest](DeleteObjectRequest.md) |  | [Optional] |

### Return type

[**DeleteObjectResponse**](DeleteObjectResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Object deleted |  -  |
| **401** | Unauthorized |  -  |
| **404** | Object not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## storageV1ObjectMetaPost

> ObjectMetadata storageV1ObjectMetaPost(getMetadataRequest)

Get object metadata

Retrieve metadata for an object without downloading it

### Example

```ts
import {
  Configuration,
  ObjectsApi,
} from '@briskstack/platform';
import type { StorageV1ObjectMetaPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ObjectsApi(config);

  const body = {
    // GetMetadataRequest (optional)
    getMetadataRequest: ...,
  } satisfies StorageV1ObjectMetaPostRequest;

  try {
    const data = await api.storageV1ObjectMetaPost(body);
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
| **getMetadataRequest** | [GetMetadataRequest](GetMetadataRequest.md) |  | [Optional] |

### Return type

[**ObjectMetadata**](ObjectMetadata.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Object metadata |  -  |
| **401** | Unauthorized |  -  |
| **404** | Object not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## storageV1ObjectsPost

> ListObjectsResponse storageV1ObjectsPost(listObjectsRequest)

List objects

List objects in a bucket with optional prefix filtering and pagination

### Example

```ts
import {
  Configuration,
  ObjectsApi,
} from '@briskstack/platform';
import type { StorageV1ObjectsPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ObjectsApi(config);

  const body = {
    // ListObjectsRequest (optional)
    listObjectsRequest: ...,
  } satisfies StorageV1ObjectsPostRequest;

  try {
    const data = await api.storageV1ObjectsPost(body);
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
| **listObjectsRequest** | [ListObjectsRequest](ListObjectsRequest.md) |  | [Optional] |

### Return type

[**ListObjectsResponse**](ListObjectsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Objects list |  -  |
| **401** | Unauthorized |  -  |
| **403** | Bucket access forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## storageV1UploadUrlPost

> UploadUrlResponse storageV1UploadUrlPost(uploadUrlRequest)

Get signed upload URL

Generate a pre-signed URL for uploading an object to R2 storage

### Example

```ts
import {
  Configuration,
  ObjectsApi,
} from '@briskstack/platform';
import type { StorageV1UploadUrlPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new ObjectsApi(config);

  const body = {
    // UploadUrlRequest (optional)
    uploadUrlRequest: ...,
  } satisfies StorageV1UploadUrlPostRequest;

  try {
    const data = await api.storageV1UploadUrlPost(body);
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
| **uploadUrlRequest** | [UploadUrlRequest](UploadUrlRequest.md) |  | [Optional] |

### Return type

[**UploadUrlResponse**](UploadUrlResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Upload URL generated |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |
| **403** | Bucket access forbidden |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

