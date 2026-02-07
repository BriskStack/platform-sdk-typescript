
# AwardXpResponse


## Properties

Name | Type
------------ | -------------
`id` | string
`userId` | string
`amount` | number
`totalXp` | number
`level` | number
`currentStreak` | number
`newBadges` | [Array&lt;AwardXpResponseNewBadgesInner&gt;](AwardXpResponseNewBadgesInner.md)

## Example

```typescript
import type { AwardXpResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "amount": 30,
  "totalXp": 1250,
  "level": 5,
  "currentStreak": 5,
  "newBadges": [{"id":"...","code":"bookworm","name":"Bookworm","icon":"📚"}],
} satisfies AwardXpResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as AwardXpResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


