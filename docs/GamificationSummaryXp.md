
# GamificationSummaryXp

XP summary

## Properties

Name | Type
------------ | -------------
`total` | number
`level` | number
`xpToNextLevel` | number
`levelProgress` | number

## Example

```typescript
import type { GamificationSummaryXp } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "total": 1250,
  "level": 5,
  "xpToNextLevel": 250,
  "levelProgress": 0.75,
} satisfies GamificationSummaryXp

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as GamificationSummaryXp
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


