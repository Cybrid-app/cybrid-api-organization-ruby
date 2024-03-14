# CybridApiOrganization::SubscriptionOrganizationModel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **guid** | **String** | Auto-generated unique identifier for the subscription. |  |
| **name** | **String** | Name provided for the subscription. |  |
| **type** | **String** | The type of subscription. |  |
| **url** | **String** | The url for the subscription. |  |
| **environment** | **String** | The environment that the subscription is configured for; one of sandbox or production. |  |
| **state** | **String** | The state of the subscription; one of storing, completed, failed, deleting, or deleted. |  |
| **failure_code** | **String** | The failure code of a subscription (if any) | [optional] |
| **created_at** | **Time** | ISO8601 datetime the record was created at. | [optional] |
| **updated_at** | **Time** | ISO8601 datetime the record was last updated at. | [optional] |

## Example

```ruby
require 'cybrid_api_organization_ruby'

instance = CybridApiOrganization::SubscriptionOrganizationModel.new(
  guid: null,
  name: null,
  type: null,
  url: null,
  environment: null,
  state: null,
  failure_code: null,
  created_at: null,
  updated_at: null
)
```

