
# PledgeListResponse


## Properties

Name | Type
------------ | -------------
`pledges` | [Array&lt;SponsorPledge&gt;](SponsorPledge.md)

## Example

```typescript
import type { PledgeListResponse } from '@briskstack/platform'

// TODO: Update the object below with actual values
const example = {
  "pledges": null,
} satisfies PledgeListResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as PledgeListResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


