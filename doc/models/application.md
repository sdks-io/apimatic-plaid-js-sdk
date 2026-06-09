
# Application

Metadata about the application

*This model accepts additional fields of type unknown.*

## Structure

`Application`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `applicationId` | `string` | Required | This field will map to the application ID that is returned from /item/applications/list, or provided to the institution in an oauth redirect. |
| `name` | `string` | Required | The name of the application |
| `createdAt` | `string` | Required | The date this application was linked in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) (YYYY-MM-DD) format in UTC. |
| `logoUrl` | `string \| null` | Required | A URL that links to the application logo image. |
| `applicationUrl` | `string \| null` | Required | The URL for the application's website |
| `reasonForAccess` | `string \| null` | Required | A string provided by the connected app stating why they use their respective enabled products. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example (as JSON)

```json
{
  "application_id": "application_id8",
  "name": "name2",
  "created_at": "2016-03-13T12:52:32.123Z",
  "logo_url": "logo_url8",
  "application_url": "application_url2",
  "reason_for_access": "reason_for_access0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

