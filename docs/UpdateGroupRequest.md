
# UpdateGroupRequest


## Properties

Name | Type
------------ | -------------
`name` | string
`description` | string
`metadata` | { [key: string]: any | null; }
`isPublic` | boolean
`isActive` | boolean

## Example

```typescript
import type { UpdateGroupRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "name": Smith Family,
  "description": The Smith family reading group,
  "metadata": {"avatar":"https://example.com/avatar.png"},
  "isPublic": false,
  "isActive": true,
} satisfies UpdateGroupRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UpdateGroupRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


