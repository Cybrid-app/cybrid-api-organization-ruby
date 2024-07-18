# CybridApiOrganization::SubscriptionsOrganizationApi

All URIs are relative to *https://organization.sandbox.cybrid.app*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_subscription**](SubscriptionsOrganizationApi.md#create_subscription) | **POST** /api/subscriptions/ | Create Subscription |
| [**delete_subscription**](SubscriptionsOrganizationApi.md#delete_subscription) | **DELETE** /api/subscriptions/{subscription_guid} | Delete Subscription |
| [**get_subscription**](SubscriptionsOrganizationApi.md#get_subscription) | **GET** /api/subscriptions/{subscription_guid} | Get Subscription  |
| [**list_subscriptions**](SubscriptionsOrganizationApi.md#list_subscriptions) | **GET** /api/subscriptions | Get subscriptions list |


## create_subscription

> <SubscriptionOrganizationModel> create_subscription(post_subscription_organization_model)

Create Subscription

Creates a Subscription.  ## Subscription creation  Subscriptions can be created for webhook endpoints.  ## State  | State | Description | |-------|-------------| | storing | The Platform is storing the subscription details in our private store | | completed | The Platform has created the subscription | | failed | The Platform was not able to successfully create the subscription | | deleting | The Platform is deleting the subscription | | deleted | The Platform has deleted the subscription|    Required scope: **subscriptions:execute

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

api_instance = CybridApiOrganization::SubscriptionsOrganizationApi.new
post_subscription_organization_model = CybridApiOrganization::PostSubscriptionOrganizationModel.new({name: 'name_example', type: 'webhook', url: 'url_example', environment: 'environment_example'}) # PostSubscriptionOrganizationModel | 

begin
  # Create Subscription
  result = api_instance.create_subscription(post_subscription_organization_model)
  p result
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionsOrganizationApi->create_subscription: #{e}"
end
```

#### Using the create_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubscriptionOrganizationModel>, Integer, Hash)> create_subscription_with_http_info(post_subscription_organization_model)

```ruby
begin
  # Create Subscription
  data, status_code, headers = api_instance.create_subscription_with_http_info(post_subscription_organization_model)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubscriptionOrganizationModel>
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionsOrganizationApi->create_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_subscription_organization_model** | [**PostSubscriptionOrganizationModel**](PostSubscriptionOrganizationModel.md) |  |  |

### Return type

[**SubscriptionOrganizationModel**](SubscriptionOrganizationModel.md)

### Authorization

[BearerAuth](../README.md#BearerAuth), [oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_subscription

> delete_subscription(subscription_guid)

Delete Subscription

Deletes a subscription.  Required scope: **subscriptions:execute**

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

api_instance = CybridApiOrganization::SubscriptionsOrganizationApi.new
subscription_guid = 'subscription_guid_example' # String | Identifier for the subscription.

begin
  # Delete Subscription
  api_instance.delete_subscription(subscription_guid)
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionsOrganizationApi->delete_subscription: #{e}"
end
```

#### Using the delete_subscription_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_subscription_with_http_info(subscription_guid)

```ruby
begin
  # Delete Subscription
  data, status_code, headers = api_instance.delete_subscription_with_http_info(subscription_guid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionsOrganizationApi->delete_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subscription_guid** | **String** | Identifier for the subscription. |  |

### Return type

nil (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth), [oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_subscription

> <SubscriptionOrganizationModel> get_subscription(subscription_guid)

Get Subscription 

Retrieves a subscription.  Required scope: **subscriptions:read**

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

api_instance = CybridApiOrganization::SubscriptionsOrganizationApi.new
subscription_guid = 'subscription_guid_example' # String | Identifier for the subscription.

begin
  # Get Subscription 
  result = api_instance.get_subscription(subscription_guid)
  p result
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionsOrganizationApi->get_subscription: #{e}"
end
```

#### Using the get_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubscriptionOrganizationModel>, Integer, Hash)> get_subscription_with_http_info(subscription_guid)

```ruby
begin
  # Get Subscription 
  data, status_code, headers = api_instance.get_subscription_with_http_info(subscription_guid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubscriptionOrganizationModel>
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionsOrganizationApi->get_subscription_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subscription_guid** | **String** | Identifier for the subscription. |  |

### Return type

[**SubscriptionOrganizationModel**](SubscriptionOrganizationModel.md)

### Authorization

[BearerAuth](../README.md#BearerAuth), [oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_subscriptions

> <SubscriptionListOrganizationModel> list_subscriptions(opts)

Get subscriptions list

Retrieves a listing of subscriptions.  Required scope: **subscriptions:read**

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

api_instance = CybridApiOrganization::SubscriptionsOrganizationApi.new
opts = {
  page: 56, # Integer | The page index to retrieve.
  per_page: 56, # Integer | The number of entities per page to return.
  guid: 'guid_example' # String | Comma separated subscription_guids to list subscriptions for.
}

begin
  # Get subscriptions list
  result = api_instance.list_subscriptions(opts)
  p result
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionsOrganizationApi->list_subscriptions: #{e}"
end
```

#### Using the list_subscriptions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubscriptionListOrganizationModel>, Integer, Hash)> list_subscriptions_with_http_info(opts)

```ruby
begin
  # Get subscriptions list
  data, status_code, headers = api_instance.list_subscriptions_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubscriptionListOrganizationModel>
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionsOrganizationApi->list_subscriptions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** | The page index to retrieve. | [optional] |
| **per_page** | **Integer** | The number of entities per page to return. | [optional] |
| **guid** | **String** | Comma separated subscription_guids to list subscriptions for. | [optional] |

### Return type

[**SubscriptionListOrganizationModel**](SubscriptionListOrganizationModel.md)

### Authorization

[BearerAuth](../README.md#BearerAuth), [oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

