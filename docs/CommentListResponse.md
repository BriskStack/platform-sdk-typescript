
# CommentListResponse


## Properties

Name | Type
------------ | -------------
`comments` | [Array&lt;Comment&gt;](Comment.md)
`nextCursor` | string
`hasMore` | boolean

## Example

```typescript
import type { CommentListResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "comments": null,
  "nextCursor": 2025-01-15T10:00:00Z_123e4567,
  "hasMore": true,
} satisfies CommentListResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CommentListResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


