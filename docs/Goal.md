
# Goal


## Properties

Name | Type
------------ | -------------
`id` | string
`userId` | string
`name` | string
`description` | string
`goalType` | string
`targetValue` | number
`currentValue` | number
`status` | string
`startDate` | string
`endDate` | string
`reward` | [Reward](Reward.md)
`progress` | number
`createdBy` | string
`createdAt` | Date
`completedAt` | Date

## Example

```typescript
import type { Goal } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "name": Read 10 books this month,
  "description": Complete 10 books before the end of January,
  "goalType": activity_count,
  "targetValue": 10,
  "currentValue": 3,
  "status": active,
  "startDate": 2025-01-01,
  "endDate": 2025-01-31,
  "reward": null,
  "progress": 0.3,
  "createdBy": 123e4567-e89b-12d3-a456-426614174002,
  "createdAt": 2025-01-15T12:00Z,
  "completedAt": null,
} satisfies Goal

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Goal
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


