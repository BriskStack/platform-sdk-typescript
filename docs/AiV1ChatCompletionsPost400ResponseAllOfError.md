
# AiV1ChatCompletionsPost400ResponseAllOfError


## Properties

Name | Type
------------ | -------------
`code` | string
`message` | string
`details` | { [key: string]: any | null; }

## Example

```typescript
import type { AiV1ChatCompletionsPost400ResponseAllOfError } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "code": VALIDATION_ERROR,
  "message": Invalid request,
  "details": null,
} satisfies AiV1ChatCompletionsPost400ResponseAllOfError

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as AiV1ChatCompletionsPost400ResponseAllOfError
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


