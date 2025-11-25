
# HelloWorldCreateMessageRequest


## Properties

Name | Type
------------ | -------------
`message` | string
`priority` | string

## Example

```typescript
import type { HelloWorldCreateMessageRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "message": Hello World,
  "priority": medium,
} satisfies HelloWorldCreateMessageRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as HelloWorldCreateMessageRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


