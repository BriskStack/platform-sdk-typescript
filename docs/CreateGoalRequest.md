
# CreateGoalRequest


## Properties

Name | Type
------------ | -------------
`userId` | string
`name` | string
`description` | string
`goalType` | string
`targetValue` | number
`activityType` | string
`startDate` | string
`endDate` | string
`rewardId` | string

## Example

```typescript
import type { CreateGoalRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "name": Read 10 books this month,
  "description": Complete 10 books before the end of January,
  "goalType": activity_count,
  "targetValue": 10,
  "activityType": reading,
  "startDate": 2025-01-01,
  "endDate": 2025-01-31,
  "rewardId": 123e4567-e89b-12d3-a456-426614174004,
} satisfies CreateGoalRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateGoalRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


