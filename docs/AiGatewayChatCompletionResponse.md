
# AiGatewayChatCompletionResponse


## Properties

Name | Type
------------ | -------------
`id` | string
`object` | string
`created` | number
`model` | string
`choices` | [Array&lt;AiGatewayChatCompletionResponseChoicesInner&gt;](AiGatewayChatCompletionResponseChoicesInner.md)
`usage` | [AiGatewayChatCompletionResponseUsage](AiGatewayChatCompletionResponseUsage.md)
`systemFingerprint` | string

## Example

```typescript
import type { AiGatewayChatCompletionResponse } from '@briskstack/platform-sdk'

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "object": null,
  "created": null,
  "model": null,
  "choices": null,
  "usage": null,
  "systemFingerprint": null,
} satisfies AiGatewayChatCompletionResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as AiGatewayChatCompletionResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


