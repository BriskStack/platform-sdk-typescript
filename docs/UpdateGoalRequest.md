
# UpdateGoalRequest


## Properties

Name | Type
------------ | -------------
`currentValue` | number
`status` | string

## Example

```typescript
import type { UpdateGoalRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "currentValue": 5,
  "status": completed,
} satisfies UpdateGoalRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UpdateGoalRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


