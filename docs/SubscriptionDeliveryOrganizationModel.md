# CybridApiOrganization::SubscriptionDeliveryOrganizationModel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **guid** | **String** | Auto-generated unique identifier for the subscription delivery. |  |
| **response** | **String** | The response of the subscription delivery. | [optional] |
| **subscription_event_guid** | **String** | The subscription event guid of the subscription delivery. |  |
| **subscription_guid** | **String** | The subscription guid of the subscription delivery. |  |
| **state** | **String** | The state of the subscription delivery. |  |
| **next_attempt_at** | **Time** | ISO8601 datetime the next attempt will be made. | [optional] |
| **attempt_count** | **Integer** | The number of attempts made to deliver the event. |  |
| **completed_at** | **Time** | ISO8601 datetime the event was delivered. | [optional] |
| **failed_at** | **Time** | ISO8601 datetime the event delivery was marked as failed. | [optional] |
| **created_at** | **Time** | ISO8601 datetime the record was created at. | [optional] |
| **updated_at** | **Time** | ISO8601 datetime the record was last updated at. | [optional] |

## Example

```ruby
require 'cybrid_api_organization_ruby'

instance = CybridApiOrganization::SubscriptionDeliveryOrganizationModel.new(
  guid: null,
  response: null,
  subscription_event_guid: null,
  subscription_guid: null,
  state: null,
  next_attempt_at: null,
  attempt_count: null,
  completed_at: null,
  failed_at: null,
  created_at: null,
  updated_at: null
)
```

