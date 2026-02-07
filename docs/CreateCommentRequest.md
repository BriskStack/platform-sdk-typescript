
# CreateCommentRequest


## Properties

Name | Type
------------ | -------------
`content` | string
`parentId` | string

## Example

```typescript
import type { CreateCommentRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "content": Great job!,
  "parentId": 123e4567-e89b-12d3-a456-426614174003,
} satisfies CreateCommentRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateCommentRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


