
# GetMetadataRequest


## Properties

Name | Type
------------ | -------------
`bucket` | string
`key` | string

## Example

```typescript
import type { GetMetadataRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "bucket": briskgrow-media,
  "key": bg/books/123e4567-e89b-12d3-a456-426614174000/cover.jpg,
} satisfies GetMetadataRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as GetMetadataRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


