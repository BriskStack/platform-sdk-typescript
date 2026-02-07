
# ListObjectsResponse


## Properties

Name | Type
------------ | -------------
`objects` | [Array&lt;ObjectMetadata&gt;](ObjectMetadata.md)
`cursor` | string
`truncated` | boolean

## Example

```typescript
import type { ListObjectsResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "objects": null,
  "cursor": eyJrZXkiOiJiZy9ib29rcy8xMjMuanBnIn0=,
  "truncated": false,
} satisfies ListObjectsResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ListObjectsResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


