# Telstra_EventDetection

## Requirements

Building the API client library requires [Maven](https://maven.apache.org/) to be installed.

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn deploy
```

Refer to the [official documentation](https://maven.apache.org/plugins/maven-deploy-plugin/usage.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
    <groupId>Telstra</groupId>
    <artifactId>Telstra_EventDetection</artifactId>
    <version>1.0.0</version>
    <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "Telstra:Telstra_EventDetection:1.0.0"
```

### Others

At first generate the JAR by executing:


Then manually install the following JARs:

* target/Telstra_EventDetection-1.0.0.jar
* target/lib/*.jar

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import com.telstra.*;
import com.telstra.auth.*;
import com.telstra.eventdetection.*;
import com.telstra.eventdetection.AuthenticationApi;

import java.io.File;
import java.util.*;

public class AuthenticationApiExample {

    public static void main(String[] args) {
        
        AuthenticationApi apiInstance = new AuthenticationApi();
        String clientId = "clientId_example"; // String | 
        String clientSecret = "clientSecret_example"; // String | 
        String grantType = "client_credentials"; // String | 
        try {
            OAuthResponse result = apiInstance.authToken(clientId, clientSecret, grantType);
            System.out.println(result);
        } catch (ApiException e) {
            System.err.println("Exception when calling AuthenticationApi#authToken");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *https://tapi.telstra.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthenticationApi* | [**authToken**](docs/AuthenticationApi.md#authToken) | **POST** /v2/oauth/token | Generate authentication token
*GetSubscriptionApi* | [**getSubscription**](docs/GetSubscriptionApi.md#getSubscription) | **POST** /v1/eventdetection/events/subscriptions | Get Event Subscriptions
*LongPollApi* | [**longpoll**](docs/LongPollApi.md#longpoll) | **POST** /v1/eventdetection/events/{eventType} | Poll events
*PushNotificationsApi* | [**pushNotifications**](docs/PushNotificationsApi.md#pushNotifications) | **POST** /v1/eventdetection/events/notifications | Push event notifications
*RegistrationApi* | [**register**](docs/RegistrationApi.md#register) | **POST** /v1/eventdetection/events | Register
*RegistrationApi* | [**unregister**](docs/RegistrationApi.md#unregister) | **DELETE** /v1/eventdetection/events/{eventType} | Unregister


## Documentation for Models

 - [Eventsattr](docs/Eventsattr.md)
 - [GetEventResponse](docs/GetEventResponse.md)
 - [GetSubscriptionResponse](docs/GetSubscriptionResponse.md)
 - [NotificationPayload](docs/NotificationPayload.md)
 - [OAuthResponse](docs/OAuthResponse.md)
 - [PhoneNumberList](docs/PhoneNumberList.md)
 - [PollingObj](docs/PollingObj.md)
 - [PushNotificationObj](docs/PushNotificationObj.md)
 - [ResisterPhoneNumberList](docs/ResisterPhoneNumberList.md)
 - [ServiceEventsAttr](docs/ServiceEventsAttr.md)
 - [SubscriptionObj](docs/SubscriptionObj.md)
 - [Subscriptionattr](docs/Subscriptionattr.md)
 - [Test](docs/Test.md)
 - [UnregisterRequestObj](docs/UnregisterRequestObj.md)


## Documentation for Authorisation

Authentication schemes defined for the API:
### auth

- **Type**: OAuth
- **Flow**: application
- **Authorisation URL**: 
- **Scopes**: 
  - v1_eventdetection_simswap: v1_eventdetection_simswap


## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author



