
# Institutions Get by Id Request Options

Specifies optional parameters for `/institutions/get_by_id`. If provided, must not be `null`.

## Structure

`InstitutionsGetByIdRequestOptions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `includeOptionalMetadata` | `boolean \| undefined` | Optional | When `true`, return an institution's logo, brand color, and URL. When available, the bank's logo is returned as a base64 encoded 152x152 PNG, the brand color is in hexadecimal format. The default value is `false`.<br><br>Note that Plaid does not own any of the logos shared by the API and that by accessing or using these logos, you agree that you are doing so at your own risk and will, if necessary, obtain all required permissions from the appropriate rights holders and adhere to any applicable usage guidelines. Plaid disclaims all express or implied warranties with respect to the logos.<br><br>**Default**: `false` |
| `includeStatus` | `boolean \| undefined` | Optional | If `true`, the response will include status information about the institution. Default value is `false`.<br><br>**Default**: `false` |
| `includeAuthMetadata` | `boolean \| undefined` | Optional | When `true`, returns metadata related to the Auth product indicating which auth methods are supported.<br><br>**Default**: `false` |
| `includePaymentInitiationMetadata` | `boolean \| undefined` | Optional | When `true`, returns metadata related to the Payment Initiation product indicating which payment configurations are supported.<br><br>**Default**: `false` |

## Example (as JSON)

```json
{
  "include_optional_metadata": false,
  "include_status": false,
  "include_auth_metadata": false,
  "include_payment_initiation_metadata": false
}
```

