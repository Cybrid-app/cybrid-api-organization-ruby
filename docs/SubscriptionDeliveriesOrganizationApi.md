# CybridApiOrganization::SubscriptionDeliveriesOrganizationApi

All URIs are relative to *https://organization.sandbox.cybrid.app*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_subscription_delivery**](SubscriptionDeliveriesOrganizationApi.md#create_subscription_delivery) | **POST** /api/subscription_deliveries/ | Create SubscriptionDelivery |
| [**get_subscription_delivery**](SubscriptionDeliveriesOrganizationApi.md#get_subscription_delivery) | **GET** /api/subscription_deliveries/{subscription_delivery_guid} | Get Subscription Delivery  |
| [**list_subscription_deliveries**](SubscriptionDeliveriesOrganizationApi.md#list_subscription_deliveries) | **GET** /api/subscription_deliveries | Get subscription deliveries list |


## create_subscription_delivery

> <SubscriptionDeliveryOrganizationModel> create_subscription_delivery(post_subscription_delivery_organization_model)

Create SubscriptionDelivery

Creates a SubscriptionDelivery.  post  Required scope: **subscription_events:execute

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

api_instance = CybridApiOrganization::SubscriptionDeliveriesOrganizationApi.new
post_subscription_delivery_organization_model = CybridApiOrganization::PostSubscriptionDeliveryOrganizationModel.new({subscription_event_guid: 'subscription_event_guid_example', subscription_guid: 'subscription_guid_example'}) # PostSubscriptionDeliveryOrganizationModel | 

begin
  # Create SubscriptionDelivery
  result = api_instance.create_subscription_delivery(post_subscription_delivery_organization_model)
  p result
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionDeliveriesOrganizationApi->create_subscription_delivery: #{e}"
end
```

#### Using the create_subscription_delivery_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubscriptionDeliveryOrganizationModel>, Integer, Hash)> create_subscription_delivery_with_http_info(post_subscription_delivery_organization_model)

```ruby
begin
  # Create SubscriptionDelivery
  data, status_code, headers = api_instance.create_subscription_delivery_with_http_info(post_subscription_delivery_organization_model)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubscriptionDeliveryOrganizationModel>
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionDeliveriesOrganizationApi->create_subscription_delivery_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **post_subscription_delivery_organization_model** | [**PostSubscriptionDeliveryOrganizationModel**](PostSubscriptionDeliveryOrganizationModel.md) |  |  |

### Return type

[**SubscriptionDeliveryOrganizationModel**](SubscriptionDeliveryOrganizationModel.md)

### Authorization

[BearerAuth](../README.md#BearerAuth), [oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_subscription_delivery

> <SubscriptionDeliveryOrganizationModel> get_subscription_delivery(subscription_delivery_guid)

Get Subscription Delivery 

Retrieves a subscription delivery.  Required scope: **subscription_events:read**

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

api_instance = CybridApiOrganization::SubscriptionDeliveriesOrganizationApi.new
subscription_delivery_guid = 'subscription_delivery_guid_example' # String | Identifier for the subscription delivery.

begin
  # Get Subscription Delivery 
  result = api_instance.get_subscription_delivery(subscription_delivery_guid)
  p result
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionDeliveriesOrganizationApi->get_subscription_delivery: #{e}"
end
```

#### Using the get_subscription_delivery_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubscriptionDeliveryOrganizationModel>, Integer, Hash)> get_subscription_delivery_with_http_info(subscription_delivery_guid)

```ruby
begin
  # Get Subscription Delivery 
  data, status_code, headers = api_instance.get_subscription_delivery_with_http_info(subscription_delivery_guid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubscriptionDeliveryOrganizationModel>
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionDeliveriesOrganizationApi->get_subscription_delivery_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subscription_delivery_guid** | **String** | Identifier for the subscription delivery. |  |

### Return type

[**SubscriptionDeliveryOrganizationModel**](SubscriptionDeliveryOrganizationModel.md)

### Authorization

[BearerAuth](../README.md#BearerAuth), [oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_subscription_deliveries

> <SubscriptionDeliveryListOrganizationModel> list_subscription_deliveries(opts)

Get subscription deliveries list

Retrieves a listing of subscription deliveries s.  Required scope: **subscription_events:read**

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

api_instance = CybridApiOrganization::SubscriptionDeliveriesOrganizationApi.new
opts = {
  page: 56, # Integer | The page index to retrieve.
  per_page: 56, # Integer | The number of entities per page to return.
  guid: 'guid_example', # String | Comma separated subscription_delivery_guids to list subscription deliveries for.
  subscription_event_guid: 'subscription_event_guid_example', # String | Comma separated subscription_event_guids to list subscription deliveries for.
  subscription_guid: 'subscription_guid_example' # String | Comma separated subscription_guids to list subscription deliveries for.
}

begin
  # Get subscription deliveries list
  result = api_instance.list_subscription_deliveries(opts)
  p result
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionDeliveriesOrganizationApi->list_subscription_deliveries: #{e}"
end
```

#### Using the list_subscription_deliveries_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubscriptionDeliveryListOrganizationModel>, Integer, Hash)> list_subscription_deliveries_with_http_info(opts)

```ruby
begin
  # Get subscription deliveries list
  data, status_code, headers = api_instance.list_subscription_deliveries_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubscriptionDeliveryListOrganizationModel>
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionDeliveriesOrganizationApi->list_subscription_deliveries_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** | The page index to retrieve. | [optional] |
| **per_page** | **Integer** | The number of entities per page to return. | [optional] |
| **guid** | **String** | Comma separated subscription_delivery_guids to list subscription deliveries for. | [optional] |
| **subscription_event_guid** | **String** | Comma separated subscription_event_guids to list subscription deliveries for. | [optional] |
| **subscription_guid** | **String** | Comma separated subscription_guids to list subscription deliveries for. | [optional] |

### Return type

[**SubscriptionDeliveryListOrganizationModel**](SubscriptionDeliveryListOrganizationModel.md)

### Authorization

[BearerAuth](../README.md#BearerAuth), [oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

