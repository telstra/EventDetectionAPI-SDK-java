# LongPollApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**longpoll**](LongPollApi.md#longpoll) | **POST** /v1/eventdetection/events/{eventType} | Poll events


<a name="longpoll"></a>
# **longpoll**
> GetEventResponse longpoll(eventType, body)

Poll events

Poll events for a given set of MSISDNs

### Example
```java
// Import classes:
//import com.telstra.ApiClient;
//import com.telstra.ApiException;
//import com.telstra.Configuration;
//import com.telstra.auth.*;
//import com.telstra.eventdetection.LongPollApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure OAuth2 access token for authorization: auth
OAuth auth = (OAuth) defaultClient.getAuthentication("auth");
auth.setAccessToken("YOUR ACCESS TOKEN");

LongPollApi apiInstance = new LongPollApi();
String eventType = "eventType_example"; // String | Event Type
PollingObj body = new PollingObj(); // PollingObj | List of MSISDNs to pull the events
try {
    GetEventResponse result = apiInstance.longpoll(eventType, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling LongPollApi#longpoll");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **eventType** | **String**| Event Type | [enum: simswap]
 **body** | [**PollingObj**](PollingObj.md)| List of MSISDNs to pull the events |

### Return type

[**GetEventResponse**](GetEventResponse.md)

### Authorization

[auth](../README.md#auth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

