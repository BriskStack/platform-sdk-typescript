
# AwardBadgeRequest


## Properties

Name | Type
------------ | -------------
`userId` | string
`badgeCode` | string
`metadata` | { [key: string]: any | null; }

## Example

```typescript
import type { AwardBadgeRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "badgeCode": bookworm,
  "metadata": {"earnedFor":"Special achievement"},
} satisfies AwardBadgeRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as AwardBadgeRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


