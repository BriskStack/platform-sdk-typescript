
# OAuthStartResponse


## Properties

Name | Type
------------ | -------------
`authUrl` | string
`state` | string

## Example

```typescript
import type { OAuthStartResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "authUrl": https://accounts.google.com/o/oauth2/v2/auth?...,
  "state": state_abc123,
} satisfies OAuthStartResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as OAuthStartResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


