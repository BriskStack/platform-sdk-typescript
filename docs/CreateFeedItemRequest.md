
# CreateFeedItemRequest


## Properties

Name | Type
------------ | -------------
`groupId` | string
`userId` | string
`itemType` | string
`title` | string
`subtitle` | string
`icon` | string
`metadata` | { [key: string]: any | null; }
`sourceType` | string
`sourceId` | string
`occurredAt` | Date

## Example

```typescript
import type { CreateFeedItemRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "groupId": 123e4567-e89b-12d3-a456-426614174002,
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "itemType": book_finished,
  "title": Emma finished 'Charlotte's Web',
  "subtitle": Her 5th book this month!,
  "icon": 📚,
  "metadata": {"bookId":"book-123","rating":5},
  "sourceType": bg_child_books,
  "sourceId": child-book-456,
  "occurredAt": 2025-01-15T10:00Z,
} satisfies CreateFeedItemRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateFeedItemRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


