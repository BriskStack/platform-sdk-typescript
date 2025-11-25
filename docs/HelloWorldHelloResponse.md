
# HelloWorldHelloResponse


## Properties

Name | Type
------------ | -------------
`message` | string
`service` | string
`environment` | string
`timestamp` | Date
`version` | string

## Example

```typescript
import type { HelloWorldHelloResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "message": Hello from BriskStack Platform!,
  "service": hello-world,
  "environment": development,
  "timestamp": 2025-01-15T12:00:00Z,
  "version": 0.1.0,
} satisfies HelloWorldHelloResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as HelloWorldHelloResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


