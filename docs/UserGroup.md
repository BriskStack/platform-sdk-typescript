
# UserGroup


## Properties

Name | Type
------------ | -------------
`membership` | [GroupMembership](GroupMembership.md)
`group` | [Group](Group.md)

## Example

```typescript
import type { UserGroup } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "membership": null,
  "group": null,
} satisfies UserGroup

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as UserGroup
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


