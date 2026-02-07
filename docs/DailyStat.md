
# DailyStat


## Properties

Name | Type
------------ | -------------
`date` | string
`byType` | [{ [key: string]: DailyStatByTypeValue; }](DailyStatByTypeValue.md)

## Example

```typescript
import type { DailyStat } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "date": 2025-01-15,
  "byType": {"reading":{"value":30,"count":2},"study":{"value":45,"count":1}},
} satisfies DailyStat

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as DailyStat
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


