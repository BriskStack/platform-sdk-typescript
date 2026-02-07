
# UserBadge


## Properties

Name | Type
------------ | -------------
`id` | string
`userId` | string
`badge` | [Badge](Badge.md)
`earnedAt` | Date
`metadata` | { [key: string]: any | null; }

## Example

```typescript
import type { UserBadge } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "badge": null,
  "earnedAt": 2025-01-15T12:00Z,
  "metadata": {"earnedFor":"Reading 10 books"},
} satisfies UserBadge

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UserBadge
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


