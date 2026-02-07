
# StatsResponsePeriod

Query period

## Properties

Name | Type
------------ | -------------
`from` | string
`to` | string
`label` | string

## Example

```typescript
import type { StatsResponsePeriod } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "from": 2025-01-01,
  "to": 2025-01-07,
  "label": This Week,
} satisfies StatsResponsePeriod

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as StatsResponsePeriod
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


