# RegistrationApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**register**](RegistrationApi.md#register) | **POST** /v1/eventdetection/events | Register
[**unregister**](RegistrationApi.md#unregister) | **DELETE** /v1/eventdetection/events/{eventType} | Unregister


<a name="register"></a>
# **register**
> ResisterPhoneNumberList register(body)

Register

Register for an event

### Example
```java
// Import classes:
//import com.telstra.ApiClient;
//import com.telstra.ApiException;
//import com.telstra.Configuration;
//import com.telstra.auth.*;
//import com.telstra.eventdetection.RegistrationApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: auth
OAuth auth = (OAuth) defaultClient.getAuthentication("auth");
auth.setAccessToken("YOUR ACCESS TOKEN");

RegistrationApi apiInstance = new RegistrationApi();
SubscriptionObj body = new SubscriptionObj(); // SubscriptionObj | Subscribe with a list of phone numbers, push notification URL (optional) and the event type.
try {
    ResisterPhoneNumberList result = apiInstance.register(body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RegistrationApi#register");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**SubscriptionObj**](SubscriptionObj.md)| Subscribe with a list of phone numbers, push notification URL (optional) and the event type. |

### Return type

[**ResisterPhoneNumberList**](ResisterPhoneNumberList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="unregister"></a>
# **unregister**
> ResisterPhoneNumberList unregister(eventType, body)

Unregister

Unregister from an event

### Example
```java
// Import classes:
//import com.telstra.ApiClient;
//import com.telstra.ApiException;
//import com.telstra.Configuration;
//import com.telstra.auth.*;
//import com.telstra.eventdetection.RegistrationApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: auth
OAuth auth = (OAuth) defaultClient.getAuthentication("auth");
auth.setAccessToken("YOUR ACCESS TOKEN");

RegistrationApi apiInstance = new RegistrationApi();
String eventType = "eventType_example"; // String | Event Type
UnregisterRequestObj body = new UnregisterRequestObj(); // UnregisterRequestObj | List of subscribed phone numbers and notification URL (optional)
try {
    ResisterPhoneNumberList result = apiInstance.unregister(eventType, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling RegistrationApi#unregister");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **eventType** | **String**| Event Type | [enum: simswap]
 **body** | [**UnregisterRequestObj**](UnregisterRequestObj.md)| List of subscribed phone numbers and notification URL (optional) |

### Return type

[**ResisterPhoneNumberList**](ResisterPhoneNumberList.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

