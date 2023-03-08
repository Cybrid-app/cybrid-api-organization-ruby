# CybridApiOrganization::OrganizationsOrganizationApi

All URIs are relative to *https://organization.sandbox.cybrid.app*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_organization**](OrganizationsOrganizationApi.md#get_organization) | **GET** /api/organizations/{organization_guid} | Get organization |
| [**update_organization**](OrganizationsOrganizationApi.md#update_organization) | **PATCH** /api/organizations/{organization_guid} | Patch organization |


## get_organization

> <OrganizationOrganizationModel> get_organization(organization_guid)

Get organization

Retrieve an organization.  Required scope: **organizations:read**

### Examples

```ruby
require 'time'
require 'cybrid_api_organization_ruby'
# setup authorization
CybridApiOrganization.configure do |config|
  # Configure Bearer authorization (JWT): BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'

  # Configure OAuth2 access token for authorization: oauth2
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = CybridApiOrganization::OrganizationsOrganizationApi.new
organization_guid = 'organization_guid_example' # String | Identifier for the organization.

begin
  # Get organization
  result = api_instance.get_organization(organization_guid)
  p result
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling OrganizationsOrganizationApi->get_organization: #{e}"
end
```

#### Using the get_organization_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OrganizationOrganizationModel>, Integer, Hash)> get_organization_with_http_info(organization_guid)

```ruby
begin
  # Get organization
  data, status_code, headers = api_instance.get_organization_with_http_info(organization_guid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OrganizationOrganizationModel>
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling OrganizationsOrganizationApi->get_organization_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **organization_guid** | **String** | Identifier for the organization. |  |

### Return type

[**OrganizationOrganizationModel**](OrganizationOrganizationModel.md)

### Authorization

[BearerAuth](../README.md#BearerAuth), [oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_organization

> <OrganizationOrganizationModel> update_organization(organization_guid, patch_organization_organization_model)

Patch organization

Update an organization.  Required scope: **organizations:write**

### Examples

```ruby
require 'time'
require 'cybrid_api_organization_ruby'
# setup authorization
CybridApiOrganization.configure do |config|
  # Configure Bearer authorization (JWT): BearerAuth
  config.access_token = 'YOUR_BEARER_TOKEN'

  # Configure OAuth2 access token for authorization: oauth2
  config.access_token = 'YOUR ACCESS TOKEN'
end

api_instance = CybridApiOrganization::OrganizationsOrganizationApi.new
organization_guid = 'organization_guid_example' # String | Identifier for the organization.
patch_organization_organization_model = CybridApiOrganization::PatchOrganizationOrganizationModel.new({name: 'name_example'}) # PatchOrganizationOrganizationModel | 

begin
  # Patch organization
  result = api_instance.update_organization(organization_guid, patch_organization_organization_model)
  p result
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling OrganizationsOrganizationApi->update_organization: #{e}"
end
```

#### Using the update_organization_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<OrganizationOrganizationModel>, Integer, Hash)> update_organization_with_http_info(organization_guid, patch_organization_organization_model)

```ruby
begin
  # Patch organization
  data, status_code, headers = api_instance.update_organization_with_http_info(organization_guid, patch_organization_organization_model)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <OrganizationOrganizationModel>
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling OrganizationsOrganizationApi->update_organization_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **organization_guid** | **String** | Identifier for the organization. |  |
| **patch_organization_organization_model** | [**PatchOrganizationOrganizationModel**](PatchOrganizationOrganizationModel.md) |  |  |

### Return type

[**OrganizationOrganizationModel**](OrganizationOrganizationModel.md)

### Authorization

[BearerAuth](../README.md#BearerAuth), [oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

