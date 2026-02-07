
# LogoutRequest


## Properties

Name | Type
------------ | -------------
`refreshToken` | string
`allSessions` | boolean

## Example

```typescript
import type { LogoutRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "refreshToken": rt_abc123...,
  "allSessions": false,
} satisfies LogoutRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as LogoutRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


