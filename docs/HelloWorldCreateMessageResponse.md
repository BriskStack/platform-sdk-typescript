
# HelloWorldCreateMessageResponse


## Properties

Name | Type
------------ | -------------
`id` | string
`message` | string
`priority` | string
`createdAt` | Date

## Example

```typescript
import type { HelloWorldCreateMessageResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "message": Hello World,
  "priority": medium,
  "createdAt": 2025-01-15T12:00:00Z,
} satisfies HelloWorldCreateMessageResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as HelloWorldCreateMessageResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


