# CybridApiOrganization::OrganizationOrganizationModel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **guid** | **String** | Auto-generated unique identifier for the organization. |  |
| **name** | **String** | Name provided for the organization. |  |
| **created_at** | **Time** | ISO8601 datetime the record was created at. |  |
| **updated_at** | **Time** | ISO8601 datetime the record was last updated at. | [optional] |

## Example

```ruby
require 'cybrid_api_organization_ruby'

instance = CybridApiOrganization::OrganizationOrganizationModel.new(
  guid: null,
  name: null,
  created_at: null,
  updated_at: null
)
```

