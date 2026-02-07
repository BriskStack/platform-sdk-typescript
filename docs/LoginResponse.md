
# LoginResponse


## Properties

Name | Type
------------ | -------------
`user` | [UserProfile](UserProfile.md)
`accessToken` | string
`refreshToken` | string
`expiresAt` | Date

## Example

```typescript
import type { LoginResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "user": null,
  "accessToken": eyJhbGciOiJIUzI1NiIs...,
  "refreshToken": rt_abc123...,
  "expiresAt": 2025-01-15T13:00Z,
} satisfies LoginResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as LoginResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


