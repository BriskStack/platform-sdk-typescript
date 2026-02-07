
# ReactionSummary


## Properties

Name | Type
------------ | -------------
`emoji` | string
`count` | number
`userReacted` | boolean

## Example

```typescript
import type { ReactionSummary } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "emoji": 🎉,
  "count": 3,
  "userReacted": true,
} satisfies ReactionSummary

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ReactionSummary
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


