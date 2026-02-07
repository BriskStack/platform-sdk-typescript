
# CommentPreview


## Properties

Name | Type
------------ | -------------
`id` | string
`userId` | string
`userName` | string
`content` | string
`createdAt` | Date

## Example

```typescript
import type { CommentPreview } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174003,
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "userName": Dad,
  "content": Great job!,
  "createdAt": 2025-01-15T12:00Z,
} satisfies CommentPreview

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CommentPreview
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


