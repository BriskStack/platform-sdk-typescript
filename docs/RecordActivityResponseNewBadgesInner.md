
# RecordActivityResponseNewBadgesInner


## Properties

Name | Type
------------ | -------------
`id` | string
`code` | string
`name` | string
`icon` | string

## Example

```typescript
import type { RecordActivityResponseNewBadgesInner } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "code": bookworm,
  "name": Bookworm,
  "icon": 📚,
} satisfies RecordActivityResponseNewBadgesInner

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RecordActivityResponseNewBadgesInner
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


