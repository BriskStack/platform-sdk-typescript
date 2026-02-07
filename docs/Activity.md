
# Activity


## Properties

Name | Type
------------ | -------------
`id` | string
`userId` | string
`activityType` | string
`value` | number
`metadata` | { [key: string]: any | null; }
`notes` | string
`performedAt` | Date
`createdAt` | Date
`xpAwarded` | number

## Example

```typescript
import type { Activity } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "userId": 123e4567-e89b-12d3-a456-426614174001,
  "activityType": reading,
  "value": 30,
  "metadata": {"bookId":"book-123","title":"Charlotte's Web"},
  "notes": Finished chapter 5,
  "performedAt": 2025-01-15T10:00Z,
  "createdAt": 2025-01-15T12:00Z,
  "xpAwarded": 30,
} satisfies Activity

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Activity
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


