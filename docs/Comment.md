
# Comment


## Properties

Name | Type
------------ | -------------
`id` | string
`feedItemId` | string
`parentId` | string
`userId` | string
`userName` | string
`userAvatarUrl` | string
`content` | string
`createdAt` | Date
`updatedAt` | Date

## Example

```typescript
import type { Comment } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174003,
  "feedItemId": 123e4567-e89b-12d3-a456-426614174000,
  "parentId": 123e4567-e89b-12d3-a456-426614174003,
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "userName": Dad,
  "userAvatarUrl": https://example.com/avatar.jpg,
  "content": Great job!,
  "createdAt": 2025-01-15T12:00Z,
  "updatedAt": 2025-01-15T12:30Z,
} satisfies Comment

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Comment
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


