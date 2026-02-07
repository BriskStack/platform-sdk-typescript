
# VideoStatus


## Properties

Name | Type
------------ | -------------
`id` | string
`status` | string
`duration` | number
`size` | number
`playbackUrl` | string
`thumbnailUrl` | string
`createdAt` | Date
`readyToStream` | boolean
`errorMessage` | string
`metadata` | { [key: string]: string; }

## Example

```typescript
import type { VideoStatus } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "status": ready,
  "duration": 45.5,
  "size": 10485760,
  "playbackUrl": https://customer-xyz.cloudflarestream.com/.../manifest/video.m3u8,
  "thumbnailUrl": https://customer-xyz.cloudflarestream.com/.../thumbnails/thumbnail.jpg,
  "createdAt": 2025-01-15T12:00Z,
  "readyToStream": true,
  "errorMessage": null,
  "metadata": {"ventureId":"briskgrow"},
} satisfies VideoStatus

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as VideoStatus
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


