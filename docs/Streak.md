
# Streak


## Properties

Name | Type
------------ | -------------
`id` | string
`userId` | string
`streakType` | string
`currentCount` | number
`longestCount` | number
`lastActivityDate` | string
`updatedAt` | Date

## Example

```typescript
import type { Streak } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "streakType": global,
  "currentCount": 5,
  "longestCount": 12,
  "lastActivityDate": 2025-01-15,
  "updatedAt": 2025-01-15T12:00Z,
} satisfies Streak

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Streak
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


