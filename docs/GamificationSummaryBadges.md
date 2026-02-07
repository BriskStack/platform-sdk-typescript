
# GamificationSummaryBadges

Badge summary

## Properties

Name | Type
------------ | -------------
`earned` | number
`recent` | [Array&lt;GamificationSummaryBadgesRecentInner&gt;](GamificationSummaryBadgesRecentInner.md)

## Example

```typescript
import type { GamificationSummaryBadges } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "earned": 5,
  "recent": null,
} satisfies GamificationSummaryBadges

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as GamificationSummaryBadges
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


