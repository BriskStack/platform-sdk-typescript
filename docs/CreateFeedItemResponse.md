
# CreateFeedItemResponse


## Properties

Name | Type
------------ | -------------
`id` | string
`itemType` | string
`group` | [FeedGroup](FeedGroup.md)
`user` | [FeedUser](FeedUser.md)
`title` | string
`subtitle` | string
`icon` | string
`metadata` | { [key: string]: any | null; }
`occurredAt` | Date
`createdAt` | Date
`reactions` | [Array&lt;ReactionSummary&gt;](ReactionSummary.md)
`commentCount` | number
`recentComments` | [Array&lt;CommentPreview&gt;](CommentPreview.md)

## Example

```typescript
import type { CreateFeedItemResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "itemType": book_finished,
  "group": null,
  "user": null,
  "title": Emma finished 'Charlotte's Web',
  "subtitle": Her 5th book this month!,
  "icon": 📚,
  "metadata": {"bookId":"book-123","rating":5},
  "occurredAt": 2025-01-15T10:00Z,
  "createdAt": 2025-01-15T10:05Z,
  "reactions": null,
  "commentCount": 2,
  "recentComments": null,
} satisfies CreateFeedItemResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateFeedItemResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


