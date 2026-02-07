
# UserLeaderboard


## Properties

Name | Type
------------ | -------------
`group` | [LeaderboardResponseGroup](LeaderboardResponseGroup.md)
`rank` | number
`totalMembers` | number
`xp` | number

## Example

```typescript
import type { UserLeaderboard } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "group": null,
  "rank": 2,
  "totalMembers": 3,
  "xp": 450,
} satisfies UserLeaderboard

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UserLeaderboard
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


