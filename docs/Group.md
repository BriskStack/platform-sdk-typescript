
# Group


## Properties

Name | Type
------------ | -------------
`id` | string
`ventureId` | string
`groupType` | string
`externalId` | string
`name` | string
`description` | string
`metadata` | { [key: string]: any | null; }
`isPublic` | boolean
`isActive` | boolean
`createdAt` | Date
`updatedAt` | Date

## Example

```typescript
import type { Group } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "id": 123e4567-e89b-12d3-a456-426614174000,
  "ventureId": 123e4567-e89b-12d3-a456-426614174001,
  "groupType": family,
  "externalId": bg-family-uuid,
  "name": Smith Family,
  "description": The Smith family reading group,
  "metadata": {"avatar":"https://example.com/avatar.png"},
  "isPublic": false,
  "isActive": true,
  "createdAt": 2025-01-15T12:00Z,
  "updatedAt": 2025-01-15T12:00Z,
} satisfies Group

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Group
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


