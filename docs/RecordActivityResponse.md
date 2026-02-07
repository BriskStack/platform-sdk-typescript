
# RecordActivityResponse


## Properties

Name | Type
------------ | -------------
`id` | string
`activityType` | string
`value` | number
`xpAwarded` | number
`performedAt` | Date
`totalXp` | number
`level` | number
`currentStreak` | number
`newBadges` | [Array&lt;RecordActivityResponseNewBadgesInner&gt;](RecordActivityResponseNewBadgesInner.md)

## Example

```typescript
import type { RecordActivityResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "activityType": reading,
  "value": 30,
  "xpAwarded": 30,
  "performedAt": 2025-01-15T10:00Z,
  "totalXp": 1250,
  "level": 5,
  "currentStreak": 5,
  "newBadges": null,
} satisfies RecordActivityResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RecordActivityResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


