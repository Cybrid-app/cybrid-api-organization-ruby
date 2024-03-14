# CybridApiOrganization::PostSubscriptionOrganizationModel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Name provided for the subscription. |  |
| **type** | **String** | The type of subscription. |  |
| **url** | **String** | The url for the subscription. |  |
| **environment** | **String** | The environment that the subscription is configured for; one of sandbox or production. |  |

## Example

```ruby
require 'cybrid_api_organization_ruby'

instance = CybridApiOrganization::PostSubscriptionOrganizationModel.new(
  name: null,
  type: null,
  url: null,
  environment: null
)
```

