
# CreateManagedUserRequest


## Properties

Name | Type
------------ | -------------
`name` | string
`accountType` | string
`birthYear` | number
`avatarUrl` | string
`parentUserId` | string

## Example

```typescript
import type { CreateManagedUserRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "name": Emma,
  "accountType": child,
  "birthYear": 2015,
  "avatarUrl": https://example.com/avatar.jpg,
  "parentUserId": 123e4567-e89b-12d3-a456-426614174000,
} satisfies CreateManagedUserRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateManagedUserRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


