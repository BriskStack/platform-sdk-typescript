
# ActivityListResponse


## Properties

Name | Type
------------ | -------------
`activities` | [Array&lt;Activity&gt;](Activity.md)
`pagination` | [ActivityListResponsePagination](ActivityListResponsePagination.md)

## Example

```typescript
import type { ActivityListResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "activities": null,
  "pagination": null,
} satisfies ActivityListResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ActivityListResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


