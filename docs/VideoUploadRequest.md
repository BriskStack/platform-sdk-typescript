
# VideoUploadRequest


## Properties

Name | Type
------------ | -------------
`name` | string
`maxDurationSeconds` | number
`requireSignedUrls` | boolean
`allowedOrigins` | Array&lt;string&gt;
`metadata` | { [key: string]: string; }

## Example

```typescript
import type { VideoUploadRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "name": grandpa-video-message.mp4,
  "maxDurationSeconds": 300,
  "requireSignedUrls": true,
  "allowedOrigins": ["https://app.briskgrow.com"],
  "metadata": {"ventureId":"briskgrow","achievementId":"123"},
} satisfies VideoUploadRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as VideoUploadRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


