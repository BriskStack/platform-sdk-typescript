
# CreateActivityTypeRequest


## Properties

Name | Type
------------ | -------------
`code` | string
`name` | string
`description` | string
`category` | string
`icon` | string
`unit` | string
`aggregation` | string
`xpPerUnit` | number
`streakEligible` | boolean
`metadataSchema` | { [key: string]: any | null; }

## Example

```typescript
import type { CreateActivityTypeRequest } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "code": reading,
  "name": Reading,
  "description": Track reading sessions and books,
  "category": learn,
  "icon": 📚,
  "unit": minutes,
  "aggregation": sum,
  "xpPerUnit": 1,
  "streakEligible": true,
  "metadataSchema": {"properties":{"bookId":{"type":"string"}}},
} satisfies CreateActivityTypeRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateActivityTypeRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


