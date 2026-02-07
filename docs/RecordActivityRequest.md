
# RecordActivityRequest


## Properties

Name | Type
------------ | -------------
`userId` | string
`activityType` | string
`value` | number
`metadata` | { [key: string]: any | null; }
`performedAt` | Date
`notes` | string
`evidenceUrl` | string
`sourceId` | string
`sourceType` | string

## Example

```typescript
import type { RecordActivityRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "activityType": reading,
  "value": 30,
  "metadata": {"bookId":"book-123","title":"Charlotte's Web"},
  "performedAt": 2025-01-15T10:00Z,
  "notes": Finished chapter 5,
  "evidenceUrl": https://storage.example.com/photo.jpg,
  "sourceId": bg_child_books-123,
  "sourceType": bg_child_books,
} satisfies RecordActivityRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RecordActivityRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


