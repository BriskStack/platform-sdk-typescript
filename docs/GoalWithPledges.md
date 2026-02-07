
# GoalWithPledges


## Properties

Name | Type
------------ | -------------
`goal` | [Goal](Goal.md)
`pledges` | [Array&lt;SponsorPledge&gt;](SponsorPledge.md)
`totalPledged` | number
`totalOwed` | number

## Example

```typescript
import type { GoalWithPledges } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "goal": null,
  "pledges": null,
  "totalPledged": 25,
  "totalOwed": 6,
} satisfies GoalWithPledges

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as GoalWithPledges
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


