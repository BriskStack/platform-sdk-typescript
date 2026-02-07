
# FeedListResponse


## Properties

Name | Type
------------ | -------------
`items` | [Array&lt;FeedItem&gt;](FeedItem.md)
`nextCursor` | string
`hasMore` | boolean

## Example

```typescript
import type { FeedListResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "items": null,
  "nextCursor": 2025-01-15T10:00:00Z_123e4567,
  "hasMore": true,
} satisfies FeedListResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as FeedListResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


