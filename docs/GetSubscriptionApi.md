# GetSubscriptionApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getSubscription**](GetSubscriptionApi.md#getSubscription) | **POST** /v1/eventdetection/events/subscriptions | Get Event Subscriptions


<a name="getSubscription"></a>
# **getSubscription**
> GetSubscriptionResponse getSubscription(body)

Get Event Subscriptions

Get the list of events subscribed for

### Example
```java
// Import classes:
//import com.telstra.ApiClient;
//import com.telstra.ApiException;
//import com.telstra.Configuration;
//import com.telstra.auth.*;
//import com.telstra.eventdetection.GetSubscriptionApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: auth
OAuth auth = (OAuth) defaultClient.getAuthentication("auth");
auth.setAccessToken("YOUR ACCESS TOKEN");

GetSubscriptionApi apiInstance = new GetSubscriptionApi();
PhoneNumberList body = new PhoneNumberList(); // PhoneNumberList | List of subscribed phone numbers
try {
    GetSubscriptionResponse result = apiInstance.getSubscription(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling GetSubscriptionApi#getSubscription");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PhoneNumberList**](PhoneNumberList.md)| List of subscribed phone numbers |

### Return type

[**GetSubscriptionResponse**](GetSubscriptionResponse.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

