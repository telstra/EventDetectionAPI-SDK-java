# PushNotificationsApi

All URIs are relative to *https://tapi.telstra.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**pushNotifications**](PushNotificationsApi.md#pushNotifications) | **POST** /v1/eventdetection/events/notifications | Push event notifications


<a name="pushNotifications"></a>
# **pushNotifications**
> PushNotificationObj pushNotifications(contentType, body)

Push event notifications

Push event notifications to the notification URL configured during the MSISDN registration process

### Example
```java
// Import classes:
//import com.telstra.ApiException;
//import com.telstra.eventdetection.PushNotificationsApi;


PushNotificationsApi apiInstance = new PushNotificationsApi();
String contentType = "contentType_example"; // String | application/json
NotificationPayload body = new NotificationPayload(); // NotificationPayload | Application Id, MSISDN, Event Id and Event Date
try {
    PushNotificationObj result = apiInstance.pushNotifications(contentType, body);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling PushNotificationsApi#pushNotifications");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contentType** | **String**| application/json |
 **body** | [**NotificationPayload**](NotificationPayload.md)| Application Id, MSISDN, Event Id and Event Date |

### Return type

[**PushNotificationObj**](PushNotificationObj.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

