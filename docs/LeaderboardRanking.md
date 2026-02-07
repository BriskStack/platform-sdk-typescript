
# LeaderboardRanking


## Properties

Name | Type
------------ | -------------
`rank` | number
`userId` | string
`displayName` | string
`xp` | number
`level` | number

## Example

```typescript
import type { LeaderboardRanking } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "rank": 1,
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "displayName": Emma,
  "xp": 450,
  "level": 5,
} satisfies LeaderboardRanking

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as LeaderboardRanking
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


