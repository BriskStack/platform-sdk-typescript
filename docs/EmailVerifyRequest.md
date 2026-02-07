
# EmailVerifyRequest


## Properties

Name | Type
------------ | -------------
`token` | string

## Example

```typescript
import type { EmailVerifyRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "token": verify_token_abc123,
} satisfies EmailVerifyRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as EmailVerifyRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


