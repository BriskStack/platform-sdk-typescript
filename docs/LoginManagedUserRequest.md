
# LoginManagedUserRequest


## Properties

Name | Type
------------ | -------------
`managedUserId` | string
`ventureId` | string

## Example

```typescript
import type { LoginManagedUserRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "managedUserId": 123e4567-e89b-12d3-a456-426614174000,
  "ventureId": 550e8400-e29b-41d4-a716-446655440000,
} satisfies LoginManagedUserRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as LoginManagedUserRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


