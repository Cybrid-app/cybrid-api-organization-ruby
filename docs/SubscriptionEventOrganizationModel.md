# CybridApiOrganization::SubscriptionEventOrganizationModel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **guid** | **String** | Auto-generated unique identifier for the subscription event. |  |
| **bank_guid** | **String** | The bank guid for which the event is received. | [optional] |
| **event_type** | **String** | The type of the subscription event. One of trade.storing, trade.pending, trade.cancelled, trade.completed, trade.settling, trade.failed, transfer.storing, transfer.pending, transfer.holding, transfer.reviewing, transfer.completed, transfer.failed, identity_verification.storing, identity_verification.pending, identity_verification.reviewing, identity_verification.waiting, identity_verification.expired, or identity_verification.completed. |  |
| **object_guid** | **String** | The object guid for which the event is received. |  |
| **environment** | **String** | The environment that the subscription event is configured for; one of sandbox or production. |  |
| **organization_guid** | **String** | The organization guid of the subscription event. |  |
| **created_at** | **Time** | ISO8601 datetime the record was created at. |  |
| **updated_at** | **Time** | ISO8601 datetime the record was last updated at. | [optional] |

## Example

```ruby
require 'cybrid_api_organization_ruby'

instance = CybridApiOrganization::SubscriptionEventOrganizationModel.new(
  guid: null,
  bank_guid: null,
  event_type: null,
  object_guid: null,
  environment: null,
  organization_guid: null,
  created_at: null,
  updated_at: null
)
```

