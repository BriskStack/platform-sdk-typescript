
# CreatePledgeRequest


## Properties

Name | Type
------------ | -------------
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
`message` | string

## Example

```typescript
import type { CreatePledgeRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
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
  "message": Keep reading! Love, Grandma,
} satisfies CreatePledgeRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreatePledgeRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


