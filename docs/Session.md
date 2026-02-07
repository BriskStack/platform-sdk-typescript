
# Session


## Properties

Name | Type
------------ | -------------
`id` | string
`userAgent` | string
`ipAddress` | string
`createdAt` | Date
`lastUsedAt` | Date
`current` | boolean

## Example

```typescript
import type { Session } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "userAgent": Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7)...,
  "ipAddress": 192.168.1.1,
  "createdAt": 2025-01-15T12:00Z,
  "lastUsedAt": 2025-01-15T12:30Z,
  "current": true,
} satisfies Session

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Session
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


