
# LeaderboardResponse


## Properties

Name | Type
------------ | -------------
`group` | [LeaderboardResponseGroup](LeaderboardResponseGroup.md)
`period` | string
`rankings` | [Array&lt;LeaderboardRanking&gt;](LeaderboardRanking.md)

## Example

```typescript
import type { LeaderboardResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "group": null,
  "period": week,
  "rankings": null,
} satisfies LeaderboardResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as LeaderboardResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


