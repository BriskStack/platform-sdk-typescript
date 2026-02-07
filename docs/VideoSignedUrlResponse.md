
# VideoSignedUrlResponse


## Properties

Name | Type
------------ | -------------
`signedUrl` | string
`thumbnailUrl` | string
`expiresAt` | Date

## Example

```typescript
import type { VideoSignedUrlResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "signedUrl": https://customer-xyz.cloudflarestream.com/.../manifest/video.m3u8?token=...,
  "thumbnailUrl": https://customer-xyz.cloudflarestream.com/.../thumbnails/thumbnail.jpg?token=...,
  "expiresAt": 2025-01-15T13:00Z,
} satisfies VideoSignedUrlResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as VideoSignedUrlResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


