
# VideoUploadResponse


## Properties

Name | Type
------------ | -------------
`videoId` | string
`uploadUrl` | string
`status` | string
`expiresAt` | Date

## Example

```typescript
import type { VideoUploadResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "videoId": 123e4567-e89b-12d3-a456-426614174000,
  "uploadUrl": https://upload.videodelivery.net/...,
  "status": pending,
  "expiresAt": 2025-01-15T13:00Z,
} satisfies VideoUploadResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as VideoUploadResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


