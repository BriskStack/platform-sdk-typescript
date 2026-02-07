
# ObjectMetadata


## Properties

Name | Type
------------ | -------------
`bucket` | string
`key` | string
`size` | number
`contentType` | string
`etag` | string
`lastModified` | Date
`customMetadata` | { [key: string]: string; }

## Example

```typescript
import type { ObjectMetadata } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "bucket": briskgrow-media,
  "key": bg/books/123e4567-e89b-12d3-a456-426614174000/cover.jpg,
  "size": 1048576,
  "contentType": image/jpeg,
  "etag": "abc123def456",
  "lastModified": 2025-01-15T12:00Z,
  "customMetadata": {"x-venture":"briskgrow","x-user-id":"123"},
} satisfies ObjectMetadata

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ObjectMetadata
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


