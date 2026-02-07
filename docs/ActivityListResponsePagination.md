
# ActivityListResponsePagination

Pagination info

## Properties

Name | Type
------------ | -------------
`total` | number
`limit` | number
`offset` | number
`hasMore` | boolean

## Example

```typescript
import type { ActivityListResponsePagination } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "total": 100,
  "limit": 50,
  "offset": 0,
  "hasMore": true,
} satisfies ActivityListResponsePagination

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ActivityListResponsePagination
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


