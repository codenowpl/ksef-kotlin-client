# AktywneSesjeKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2AuthSessionsCurrentDelete**](AktywneSesjeKsefApi.md#apiV2AuthSessionsCurrentDelete) | **DELETE** /api/v2/auth/sessions/current | Unieważnienie aktualnej sesji uwierzytelnienia |
| [**apiV2AuthSessionsGet**](AktywneSesjeKsefApi.md#apiV2AuthSessionsGet) | **GET** /api/v2/auth/sessions | Pobranie listy aktywnych sesji |
| [**apiV2AuthSessionsReferenceNumberDelete**](AktywneSesjeKsefApi.md#apiV2AuthSessionsReferenceNumberDelete) | **DELETE** /api/v2/auth/sessions/{referenceNumber} | Unieważnienie sesji uwierzytelnienia |


<a id="apiV2AuthSessionsCurrentDelete"></a>
# **apiV2AuthSessionsCurrentDelete**
> apiV2AuthSessionsCurrentDelete()

Unieważnienie aktualnej sesji uwierzytelnienia

Unieważnia sesję powiązaną z tokenem użytym do wywołania tej operacji.  Unieważnienie sesji sprawia, że powiązany z nią refresh token przestaje działać i nie można już za jego pomocą uzyskać kolejnych access tokenów. **Aktywne access tokeny działają do czasu minięcia ich termin ważności.**  Sposób uwierzytelnienia: &#x60;RefreshToken&#x60; lub &#x60;AccessToken&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = AktywneSesjeKsefApi()
try {
    apiInstance.apiV2AuthSessionsCurrentDelete()
} catch (e: ClientException) {
    println("4xx response calling AktywneSesjeKsefApi#apiV2AuthSessionsCurrentDelete")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AktywneSesjeKsefApi#apiV2AuthSessionsCurrentDelete")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2AuthSessionsGet"></a>
# **apiV2AuthSessionsGet**
> AuthenticationListResponse apiV2AuthSessionsGet(xContinuationToken, pageSize)

Pobranie listy aktywnych sesji

Zwraca listę aktywnych sesji uwierzytelnienia.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = AktywneSesjeKsefApi()
val xContinuationToken : kotlin.String = xContinuationToken_example // kotlin.String | Token służący do pobrania kolejnej strony wyników.
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników.
try {
    val result : AuthenticationListResponse = apiInstance.apiV2AuthSessionsGet(xContinuationToken, pageSize)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling AktywneSesjeKsefApi#apiV2AuthSessionsGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AktywneSesjeKsefApi#apiV2AuthSessionsGet")
    e.printStackTrace()
}
```

### Parameters
| **xContinuationToken** | **kotlin.String**| Token służący do pobrania kolejnej strony wyników. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. | [optional] [default to 10] |

### Return type

[**AuthenticationListResponse**](AuthenticationListResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2AuthSessionsReferenceNumberDelete"></a>
# **apiV2AuthSessionsReferenceNumberDelete**
> apiV2AuthSessionsReferenceNumberDelete(referenceNumber)

Unieważnienie sesji uwierzytelnienia

Unieważnia sesję o podanym numerze referencyjnym.  Unieważnienie sesji sprawia, że powiązany z nią refresh token przestaje działać i nie można już za jego pomocą uzyskać kolejnych access tokenów. **Aktywne access tokeny działają do czasu minięcia ich termin ważności.**

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = AktywneSesjeKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny sesji uwierzytelnienia.
try {
    apiInstance.apiV2AuthSessionsReferenceNumberDelete(referenceNumber)
} catch (e: ClientException) {
    println("4xx response calling AktywneSesjeKsefApi#apiV2AuthSessionsReferenceNumberDelete")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling AktywneSesjeKsefApi#apiV2AuthSessionsReferenceNumberDelete")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **referenceNumber** | **kotlin.String**| Numer referencyjny sesji uwierzytelnienia. | |

### Return type

null (empty response body)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

