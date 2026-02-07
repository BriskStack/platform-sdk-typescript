
# RegisterRequest


## Properties

Name | Type
------------ | -------------
`email` | string
`password` | string
`name` | string
`accountType` | string
`birthYear` | number
`ventureId` | string
`clientType` | string

## Example

```typescript
import type { RegisterRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "email": user@example.com,
  "password": SecurePass123!,
  "name": John Doe,
  "accountType": adult,
  "birthYear": 1990,
  "ventureId": 550e8400-e29b-41d4-a716-446655440000,
  "clientType": web,
} satisfies RegisterRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RegisterRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


