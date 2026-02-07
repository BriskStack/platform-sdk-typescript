
# StatsResponse


## Properties

Name | Type
------------ | -------------
`userId` | string
`period` | [StatsResponsePeriod](StatsResponsePeriod.md)
`summary` | [StatsResponseSummary](StatsResponseSummary.md)
`byType` | [Array&lt;StatsByType&gt;](StatsByType.md)
`daily` | [Array&lt;DailyStat&gt;](DailyStat.md)
`comparison` | [StatsResponseComparison](StatsResponseComparison.md)

## Example

```typescript
import type { StatsResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "period": null,
  "summary": null,
  "byType": null,
  "daily": null,
  "comparison": null,
} satisfies StatsResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as StatsResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


