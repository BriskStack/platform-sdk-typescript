
# UploadUrlResponse


## Properties

Name | Type
------------ | -------------
`uploadUrl` | string
`publicUrl` | string
`expiresAt` | Date

## Example

```typescript
import type { UploadUrlResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "uploadUrl": https://storage.briskstack.com/upload/...,
  "publicUrl": https://cdn.briskstack.com/briskgrow-media/bg/books/.../cover.jpg,
  "expiresAt": 2025-01-15T13:00Z,
} satisfies UploadUrlResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UploadUrlResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


