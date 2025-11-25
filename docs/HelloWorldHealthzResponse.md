
# HelloWorldHealthzResponse


## Properties

Name | Type
------------ | -------------
`status` | string
`service` | string
`environment` | string
`version` | string
`timestamp` | Date
`uptime` | number

## Example

```typescript
import type { HelloWorldHealthzResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "status": ok,
  "service": hello-world,
  "environment": production,
  "version": 1.0.0,
  "timestamp": 2025-01-15T12:00:00Z,
  "uptime": 3600,
} satisfies HelloWorldHealthzResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as HelloWorldHealthzResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


