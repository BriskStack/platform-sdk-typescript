
# ChatMessage


## Properties

Name | Type
------------ | -------------
`role` | string
`content` | string
`name` | string
`toolCalls` | Array&lt;any | null&gt;
`toolCallId` | string

## Example

```typescript
import type { ChatMessage } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "role": user,
  "content": null,
  "name": user_123,
  "toolCalls": null,
  "toolCallId": call_abc123,
} satisfies ChatMessage

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ChatMessage
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


