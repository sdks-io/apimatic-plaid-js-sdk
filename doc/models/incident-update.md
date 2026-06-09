
# Incident Update

## Structure

`IncidentUpdate`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| undefined` | Optional | The content of the update. |
| `status` | [`Status1Enum \| undefined`](../../doc/models/status-1-enum.md) | Optional | The status of the incident. |
| `updatedDate` | `string \| undefined` | Optional | The date when the update was published, in [ISO 8601](https://wikipedia.org/wiki/ISO_8601) format, e.g. `"2020-10-30T15:26:48Z"`. |

## Example (as JSON)

```json
{
  "description": "description8",
  "status": "INVESTIGATING",
  "updated_date": "2016-03-13T12:52:32.123Z"
}
```

