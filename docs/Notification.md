
# Notification


## Properties

Name | Type
------------ | -------------
`id` | string
`notificationType` | string
`title` | string
`body` | string
`icon` | string
`sourceType` | string
`sourceId` | string
`actionUrl` | string
`readAt` | Date
`createdAt` | Date

## Example

```typescript
import type { Notification } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "notificationType": feed_item,
  "title": Emma finished a book!,
  "body": Charlotte's Web - Her 5th book this month,
  "icon": 📚,
  "sourceType": feed_item,
  "sourceId": 123e4567-e89b-12d3-a456-426614174001,
  "actionUrl": /feed/item/123,
  "readAt": 2025-01-15T12:00Z,
  "createdAt": 2025-01-15T10:00Z,
} satisfies Notification

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Notification
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


