
# HelloWorldProtectedResponse


## Properties

Name | Type
------------ | -------------
`message` | string
`userId` | string
`roles` | Array&lt;string&gt;
`timestamp` | Date

## Example

```typescript
import type { HelloWorldProtectedResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "message": Access granted! You are authenticated.,
  "userId": user-123,
  "roles": [authenticated],
  "timestamp": 2025-01-15T12:00:00Z,
} satisfies HelloWorldProtectedResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as HelloWorldProtectedResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


