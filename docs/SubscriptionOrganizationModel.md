# CybridApiOrganization::SubscriptionOrganizationModel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **guid** | **String** | Auto-generated unique identifier for the subscription. |  |
| **organization_guid** | **String** | The organization guid for the subscription. | [optional] |
| **name** | **String** | Name provided for the subscription. |  |
| **type** | **String** | The type of subscription. |  |
| **url** | **String** | The url for the subscription. Required when subscription_type is webhook. | [optional] |
| **signing_key** | **String** | Subscription private signing key. Optional when subscription_type is webhook. | [optional] |
| **recipient** | **String** | Recipient email address. Required when subscription_type is email. | [optional] |
| **event_types** | **Array&lt;String&gt;** | Event types delivered to the subscription, within those its channel supports; null means no narrowing. | [optional] |
| **deliveries_failing_since** | **Time** | ISO8601 datetime the deliveries started failing. | [optional] |
| **environment** | **String** | The environment that the subscription is configured for; one of sandbox or production. |  |
| **state** | **String** | The state of the subscription; one of storing, completed, or failed. |  |
| **scheduled_deletion_at** | **Time** | ISO8601 datetime the subscription is scheduled to be deleted at; events continue to be delivered until then. | [optional] |
| **protection_enabled** | **Boolean** | Whether the subscription is protected from deletion. | [optional] |
| **failure_code** | **String** | The failure code of a subscription (if any) | [optional] |
| **created_at** | **Time** | ISO8601 datetime the record was created at. | [optional] |
| **updated_at** | **Time** | ISO8601 datetime the record was last updated at. | [optional] |

## Example

```ruby
require 'cybrid_api_organization_ruby'

instance = CybridApiOrganization::SubscriptionOrganizationModel.new(
  guid: null,
  organization_guid: null,
  name: null,
  type: null,
  url: null,
  signing_key: null,
  recipient: null,
  event_types: null,
  deliveries_failing_since: null,
  environment: null,
  state: null,
  scheduled_deletion_at: null,
  protection_enabled: null,
  failure_code: null,
  created_at: null,
  updated_at: null
)
```

