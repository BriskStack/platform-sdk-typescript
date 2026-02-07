
# DeleteObjectResponse


## Properties

Name | Type
------------ | -------------
`success` | boolean
`message` | string

## Example

```typescript
import type { DeleteObjectResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "success": true,
  "message": Object deleted successfully,
} satisfies DeleteObjectResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as DeleteObjectResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


