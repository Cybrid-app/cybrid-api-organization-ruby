# CybridApiOrganization::SubscriptionEventsOrganizationApi

All URIs are relative to *https://organization.sandbox.cybrid.app*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_subscription_event**](SubscriptionEventsOrganizationApi.md#get_subscription_event) | **GET** /api/subscription_events/{subscription_event_guid} | Get Subscription Event  |
| [**list_subscription_events**](SubscriptionEventsOrganizationApi.md#list_subscription_events) | **GET** /api/subscription_events | Get subscription events list |


## get_subscription_event

> <SubscriptionEventOrganizationModel> get_subscription_event(subscription_event_guid)

Get Subscription Event 

Retrieves a Subscription Event.  Required scope: **subscription_events:read**

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

api_instance = CybridApiOrganization::SubscriptionEventsOrganizationApi.new
subscription_event_guid = 'subscription_event_guid_example' # String | Identifier for the Subscription Event.

begin
  # Get Subscription Event 
  result = api_instance.get_subscription_event(subscription_event_guid)
  p result
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionEventsOrganizationApi->get_subscription_event: #{e}"
end
```

#### Using the get_subscription_event_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubscriptionEventOrganizationModel>, Integer, Hash)> get_subscription_event_with_http_info(subscription_event_guid)

```ruby
begin
  # Get Subscription Event 
  data, status_code, headers = api_instance.get_subscription_event_with_http_info(subscription_event_guid)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubscriptionEventOrganizationModel>
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionEventsOrganizationApi->get_subscription_event_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subscription_event_guid** | **String** | Identifier for the Subscription Event. |  |

### Return type

[**SubscriptionEventOrganizationModel**](SubscriptionEventOrganizationModel.md)

### Authorization

[BearerAuth](../README.md#BearerAuth), [oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_subscription_events

> <SubscriptionEventListOrganizationModel> list_subscription_events(opts)

Get subscription events list

Retrieves a listing of subscription events s.  Required scope: **subscription_events:read**

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

api_instance = CybridApiOrganization::SubscriptionEventsOrganizationApi.new
opts = {
  page: 56, # Integer | The page index to retrieve.
  per_page: 56, # Integer | The number of entities per page to return.
  guid: 'guid_example' # String | Comma separated subscription_event_guids to list subscription events for.
}

begin
  # Get subscription events list
  result = api_instance.list_subscription_events(opts)
  p result
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionEventsOrganizationApi->list_subscription_events: #{e}"
end
```

#### Using the list_subscription_events_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SubscriptionEventListOrganizationModel>, Integer, Hash)> list_subscription_events_with_http_info(opts)

```ruby
begin
  # Get subscription events list
  data, status_code, headers = api_instance.list_subscription_events_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SubscriptionEventListOrganizationModel>
rescue CybridApiOrganization::ApiError => e
  puts "Error when calling SubscriptionEventsOrganizationApi->list_subscription_events_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **Integer** | The page index to retrieve. | [optional] |
| **per_page** | **Integer** | The number of entities per page to return. | [optional] |
| **guid** | **String** | Comma separated subscription_event_guids to list subscription events for. | [optional] |

### Return type

[**SubscriptionEventListOrganizationModel**](SubscriptionEventListOrganizationModel.md)

### Authorization

[BearerAuth](../README.md#BearerAuth), [oauth2](../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

