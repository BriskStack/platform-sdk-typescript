
# StatsResponseComparison

Comparison with previous period (if includeComparison=true)

## Properties

Name | Type
------------ | -------------
`previousPeriodValue` | number
`changePercent` | number

## Example

```typescript
import type { StatsResponseComparison } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "previousPeriodValue": 280,
  "changePercent": 28.6,
} satisfies StatsResponseComparison

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as StatsResponseComparison
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


