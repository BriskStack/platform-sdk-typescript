
# CreateBadgeRequest


## Properties

Name | Type
------------ | -------------
`code` | string
`name` | string
`description` | string
`icon` | string
`category` | string
`xpThreshold` | number
`streakThreshold` | number
`activityCountThreshold` | number
`criteria` | { [key: string]: any | null; }
`sortOrder` | number

## Example

```typescript
import type { CreateBadgeRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "code": bookworm,
  "name": Bookworm,
  "description": Read 10 books,
  "icon": 📚,
  "category": achievement,
  "xpThreshold": 1000,
  "streakThreshold": 7,
  "activityCountThreshold": 50,
  "criteria": {"activityType":"reading","minValue":100},
  "sortOrder": 10,
} satisfies CreateBadgeRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateBadgeRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


