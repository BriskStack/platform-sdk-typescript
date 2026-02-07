
# SponsorPledge


## Properties

Name | Type
------------ | -------------
`id` | string
`goalId` | string
`sponsorId` | string
`sponsorName` | string
`pledgeType` | string
`amountPerUnit` | number
`maxAmount` | number
`bonusAmount` | number
`currency` | string
`isMonetary` | boolean
`rewardDescription` | string
`status` | string
`amountOwed` | number
`amountPaid` | number
`message` | string
`createdAt` | Date

## Example

```typescript
import type { SponsorPledge } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "goalId": 123e4567-e89b-12d3-a456-426614174001,
  "sponsorId": 123e4567-e89b-12d3-a456-426614174002,
  "sponsorName": Grandma,
  "pledgeType": per_unit,
  "amountPerUnit": 2,
  "maxAmount": 25,
  "bonusAmount": 10,
  "currency": USD,
  "isMonetary": true,
  "rewardDescription": Trip to the zoo,
  "status": active,
  "amountOwed": 6,
  "amountPaid": 0,
  "message": Keep reading! Love, Grandma,
  "createdAt": 2025-01-15T12:00Z,
} satisfies SponsorPledge

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as SponsorPledge
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


