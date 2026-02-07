
# NotificationPreferences

Per-type notification preferences

## Properties

Name | Type
------------ | -------------
`feedItem` | [NotificationPreferenceType](NotificationPreferenceType.md)
`reaction` | [NotificationPreferenceType](NotificationPreferenceType.md)
`comment` | [NotificationPreferenceType](NotificationPreferenceType.md)
`goalReminder` | [NotificationPreferenceType](NotificationPreferenceType.md)
`streakWarning` | [NotificationPreferenceType](NotificationPreferenceType.md)

## Example

```typescript
import type { NotificationPreferences } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "feedItem": null,
  "reaction": null,
  "comment": null,
  "goalReminder": null,
  "streakWarning": null,
} satisfies NotificationPreferences

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as NotificationPreferences
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


