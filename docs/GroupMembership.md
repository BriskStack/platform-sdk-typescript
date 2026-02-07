
# GroupMembership


## Properties

Name | Type
------------ | -------------
`id` | string
`userId` | string
`groupId` | string
`role` | string
`status` | string
`metadata` | { [key: string]: any | null; }
`joinedAt` | Date

## Example

```typescript
import type { GroupMembership } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "groupId": 123e4567-e89b-12d3-a456-426614174002,
  "role": member,
  "status": active,
  "metadata": {"displayName":"Emma"},
  "joinedAt": 2025-01-15T12:00Z,
} satisfies GroupMembership

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as GroupMembership
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


