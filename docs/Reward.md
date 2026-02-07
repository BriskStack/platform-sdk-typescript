
# Reward


## Properties

Name | Type
------------ | -------------
`id` | string
`name` | string
`description` | string
`rewardType` | string
`monetaryValue` | number
`currency` | string
`recipientId` | string
`groupId` | string
`providedBy` | string
`providerName` | string
`status` | string
`isActive` | boolean
`fulfilledAt` | Date
`fulfilledBy` | string
`createdAt` | Date

## Example

```typescript
import type { Reward } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "name": Ice Cream Trip,
  "description": A special trip to the ice cream shop,
  "rewardType": monetary,
  "monetaryValue": 10,
  "currency": USD,
  "recipientId": 123e4567-e89b-12d3-a456-426614174010,
  "groupId": 123e4567-e89b-12d3-a456-426614174020,
  "providedBy": 123e4567-e89b-12d3-a456-426614174001,
  "providerName": Grandma,
  "status": active,
  "isActive": true,
  "fulfilledAt": null,
  "fulfilledBy": null,
  "createdAt": 2025-01-15T12:00Z,
} satisfies Reward

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Reward
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


