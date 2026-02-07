
# StatsByType


## Properties

Name | Type
------------ | -------------
`activityType` | string
`value` | number
`count` | number
`unit` | string
`xpEarned` | number
`breakdown` | { [key: string]: number; }

## Example

```typescript
import type { StatsByType } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "activityType": reading,
  "value": 180,
  "count": 12,
  "unit": minutes,
  "xpEarned": 180,
  "breakdown": {"fiction":120,"non-fiction":60},
} satisfies StatsByType

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as StatsByType
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


