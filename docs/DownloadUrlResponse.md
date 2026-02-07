
# DownloadUrlResponse


## Properties

Name | Type
------------ | -------------
`downloadUrl` | string
`expiresAt` | Date

## Example

```typescript
import type { DownloadUrlResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "downloadUrl": https://storage.briskstack.com/download/...,
  "expiresAt": 2025-01-15T13:00Z,
} satisfies DownloadUrlResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as DownloadUrlResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


