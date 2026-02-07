
# AddMemberRequest


## Properties

Name | Type
------------ | -------------
`userId` | string
`role` | string
`metadata` | { [key: string]: any | null; }

## Example

```typescript
import type { AddMemberRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "role": member,
  "metadata": {"displayName":"Emma"},
} satisfies AddMemberRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as AddMemberRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


