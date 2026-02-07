
# StatsResponseSummary

Summary statistics

## Properties

Name | Type
------------ | -------------
`totalActivities` | number
`totalValue` | number
`totalXp` | number

## Example

```typescript
import type { StatsResponseSummary } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "totalActivities": 45,
  "totalValue": 360,
  "totalXp": 720,
} satisfies StatsResponseSummary

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as StatsResponseSummary
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


