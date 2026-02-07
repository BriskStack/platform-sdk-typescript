
# ChatCompletionRequest


## Properties

Name | Type
------------ | -------------
`model` | string
`messages` | [Array&lt;ChatMessage&gt;](ChatMessage.md)
`temperature` | number
`topP` | number
`n` | number
`stream` | boolean
`stop` | [ChatCompletionRequestStop](ChatCompletionRequestStop.md)
`maxTokens` | number
`presencePenalty` | number
`frequencyPenalty` | number
`logitBias` | { [key: string]: number; }
`user` | string
`tools` | Array&lt;any | null&gt;
`toolChoice` | string
`responseFormat` | [ChatCompletionRequestResponseFormat](ChatCompletionRequestResponseFormat.md)
`seed` | number

## Example

```typescript
import type { ChatCompletionRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "model": openai/gpt-4,
  "messages": null,
  "temperature": 0.7,
  "topP": 1,
  "n": 1,
  "stream": false,
  "stop": null,
  "maxTokens": 1000,
  "presencePenalty": 0,
  "frequencyPenalty": 0,
  "logitBias": null,
  "user": null,
  "tools": null,
  "toolChoice": null,
  "responseFormat": null,
  "seed": null,
} satisfies ChatCompletionRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ChatCompletionRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


