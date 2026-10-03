# CybridApiOrganization::PostSubscriptionOrganizationModel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **environment** | **String** | The environment that the subscription is configured for. |  |
| **type** | **String** | Type of the subscription. |  |
| **name** | **String** | Name provided for the subscription. |  |
| **event_types** | **Array&lt;String&gt;** | Event types delivered to the subscription, within those its channel supports; omitted or null means no narrowing. | [optional] |
| **url** | **String** | URL provided for the subscription. Required when type is webhook. | [optional] |
| **recipient** | **String** | Recipient email address. Required when type is email. | [optional] |

## Example

```ruby
require 'cybrid_api_organization_ruby'

instance = CybridApiOrganization::PostSubscriptionOrganizationModel.new(
  environment: null,
  type: null,
  name: null,
  event_types: null,
  url: null,
  recipient: null
)
```

