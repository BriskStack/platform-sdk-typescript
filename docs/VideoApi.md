# VideoApi

All URIs are relative to *https://api.briskstack.com/platform/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**storageV1VideoSignedUrlPost**](VideoApi.md#storagev1videosignedurlpost) | **POST** /storage/v1/video/signed-url | Get signed playback URL |
| [**storageV1VideoUploadPost**](VideoApi.md#storagev1videouploadpost) | **POST** /storage/v1/video/upload | Create video upload |
| [**storageV1VideoVideoIdDelete**](VideoApi.md#storagev1videovideoiddelete) | **DELETE** /storage/v1/video/{videoId} | Delete video |
| [**storageV1VideoVideoIdGet**](VideoApi.md#storagev1videovideoidget) | **GET** /storage/v1/video/{videoId} | Get video status |



## storageV1VideoSignedUrlPost

> VideoSignedUrlResponse storageV1VideoSignedUrlPost(videoSignedUrlRequest)

Get signed playback URL

Generate a signed URL for video playback (required if requireSignedUrls is true)

### Example

```ts
import {
  Configuration,
  VideoApi,
} from '@briskstack/platform';
import type { StorageV1VideoSignedUrlPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new VideoApi(config);

  const body = {
    // VideoSignedUrlRequest (optional)
    videoSignedUrlRequest: ...,
  } satisfies StorageV1VideoSignedUrlPostRequest;

  try {
    const data = await api.storageV1VideoSignedUrlPost(body);
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
| **videoSignedUrlRequest** | [VideoSignedUrlRequest](VideoSignedUrlRequest.md) |  | [Optional] |

### Return type

[**VideoSignedUrlResponse**](VideoSignedUrlResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Signed URL generated |  -  |
| **401** | Unauthorized |  -  |
| **404** | Video not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## storageV1VideoUploadPost

> VideoUploadResponse storageV1VideoUploadPost(videoUploadRequest)

Create video upload

Create a video upload session using Cloudflare Stream TUS protocol

### Example

```ts
import {
  Configuration,
  VideoApi,
} from '@briskstack/platform';
import type { StorageV1VideoUploadPostRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new VideoApi(config);

  const body = {
    // VideoUploadRequest (optional)
    videoUploadRequest: ...,
  } satisfies StorageV1VideoUploadPostRequest;

  try {
    const data = await api.storageV1VideoUploadPost(body);
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
| **videoUploadRequest** | [VideoUploadRequest](VideoUploadRequest.md) |  | [Optional] |

### Return type

[**VideoUploadResponse**](VideoUploadResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Video upload created |  -  |
| **400** | Invalid request |  -  |
| **401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## storageV1VideoVideoIdDelete

> DeleteVideoResponse storageV1VideoVideoIdDelete(videoId)

Delete video

Delete a video from Cloudflare Stream

### Example

```ts
import {
  Configuration,
  VideoApi,
} from '@briskstack/platform';
import type { StorageV1VideoVideoIdDeleteRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new VideoApi(config);

  const body = {
    // string
    videoId: 123e4567-e89b-12d3-a456-426614174000,
  } satisfies StorageV1VideoVideoIdDeleteRequest;

  try {
    const data = await api.storageV1VideoVideoIdDelete(body);
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
| **videoId** | `string` |  | [Defaults to `undefined`] |

### Return type

[**DeleteVideoResponse**](DeleteVideoResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Video deleted |  -  |
| **401** | Unauthorized |  -  |
| **404** | Video not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## storageV1VideoVideoIdGet

> VideoStatus storageV1VideoVideoIdGet(videoId)

Get video status

Get the current status and metadata of a video

### Example

```ts
import {
  Configuration,
  VideoApi,
} from '@briskstack/platform';
import type { StorageV1VideoVideoIdGetRequest } from '@briskstack/platform';

async function example() {
  console.log("🚀 Testing @briskstack/platform SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearerAuth
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new VideoApi(config);

  const body = {
    // string
    videoId: 123e4567-e89b-12d3-a456-426614174000,
  } satisfies StorageV1VideoVideoIdGetRequest;

  try {
    const data = await api.storageV1VideoVideoIdGet(body);
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
| **videoId** | `string` |  | [Defaults to `undefined`] |

### Return type

[**VideoStatus**](VideoStatus.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Video status |  -  |
| **401** | Unauthorized |  -  |
| **404** | Video not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

