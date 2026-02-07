
# OAuthCallbackRequest


## Properties

Name | Type
------------ | -------------
`provider` | string
`code` | string
`state` | string

## Example

```typescript
import type { OAuthCallbackRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "provider": google,
  "code": auth_code_xyz789,
  "state": state_abc123,
} satisfies OAuthCallbackRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as OAuthCallbackRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


