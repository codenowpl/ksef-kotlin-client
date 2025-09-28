# DaneTestoweKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2TestdataAttachmentPost**](DaneTestoweKsefApi.md#apiV2TestdataAttachmentPost) | **POST** /api/v2/testdata/attachment | Umożliwienie wysyłania faktur z załącznikiem |
| [**apiV2TestdataAttachmentRevokePost**](DaneTestoweKsefApi.md#apiV2TestdataAttachmentRevokePost) | **POST** /api/v2/testdata/attachment/revoke | Odebranie możliwości wysyłania faktur z załącznikiem |
| [**apiV2TestdataPermissionsPost**](DaneTestoweKsefApi.md#apiV2TestdataPermissionsPost) | **POST** /api/v2/testdata/permissions | Nadanie uprawnień testowemu podmiotowi/osobie fizycznej |
| [**apiV2TestdataPermissionsRevokePost**](DaneTestoweKsefApi.md#apiV2TestdataPermissionsRevokePost) | **POST** /api/v2/testdata/permissions/revoke | Odebranie uprawnień testowemu podmiotowi/osobie fizycznej |
| [**apiV2TestdataPersonPost**](DaneTestoweKsefApi.md#apiV2TestdataPersonPost) | **POST** /api/v2/testdata/person | Utworzenie osoby fizycznej |
| [**apiV2TestdataPersonRemovePost**](DaneTestoweKsefApi.md#apiV2TestdataPersonRemovePost) | **POST** /api/v2/testdata/person/remove | Usunięcie osoby fizycznej |
| [**apiV2TestdataSubjectPost**](DaneTestoweKsefApi.md#apiV2TestdataSubjectPost) | **POST** /api/v2/testdata/subject | Utworzenie podmiotu |
| [**apiV2TestdataSubjectRemovePost**](DaneTestoweKsefApi.md#apiV2TestdataSubjectRemovePost) | **POST** /api/v2/testdata/subject/remove | Usunięcie podmiotu |


<a id="apiV2TestdataAttachmentPost"></a>
# **apiV2TestdataAttachmentPost**
> apiV2TestdataAttachmentPost(attachmentPermissionGrantRequest)

Umożliwienie wysyłania faktur z załącznikiem

Dodaje możliwość wysyłania faktur z załącznikiem przez wskazany podmiot

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = DaneTestoweKsefApi()
val attachmentPermissionGrantRequest : AttachmentPermissionGrantRequest =  // AttachmentPermissionGrantRequest | 
try {
    apiInstance.apiV2TestdataAttachmentPost(attachmentPermissionGrantRequest)
} catch (e: ClientException) {
    println("4xx response calling DaneTestoweKsefApi#apiV2TestdataAttachmentPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DaneTestoweKsefApi#apiV2TestdataAttachmentPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **attachmentPermissionGrantRequest** | [**AttachmentPermissionGrantRequest**](AttachmentPermissionGrantRequest.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2TestdataAttachmentRevokePost"></a>
# **apiV2TestdataAttachmentRevokePost**
> apiV2TestdataAttachmentRevokePost(attachmentPermissionRevokeRequest)

Odebranie możliwości wysyłania faktur z załącznikiem

Odbiera możliwość wysyłania faktur z załącznikiem przez wskazany podmiot

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = DaneTestoweKsefApi()
val attachmentPermissionRevokeRequest : AttachmentPermissionRevokeRequest =  // AttachmentPermissionRevokeRequest | 
try {
    apiInstance.apiV2TestdataAttachmentRevokePost(attachmentPermissionRevokeRequest)
} catch (e: ClientException) {
    println("4xx response calling DaneTestoweKsefApi#apiV2TestdataAttachmentRevokePost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DaneTestoweKsefApi#apiV2TestdataAttachmentRevokePost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **attachmentPermissionRevokeRequest** | [**AttachmentPermissionRevokeRequest**](AttachmentPermissionRevokeRequest.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2TestdataPermissionsPost"></a>
# **apiV2TestdataPermissionsPost**
> apiV2TestdataPermissionsPost(testDataPermissionsGrantRequest)

Nadanie uprawnień testowemu podmiotowi/osobie fizycznej

Nadawanie uprawnień testowemu podmiotowi lub osobie fizycznej, a także w ich kontekście.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = DaneTestoweKsefApi()
val testDataPermissionsGrantRequest : TestDataPermissionsGrantRequest =  // TestDataPermissionsGrantRequest | 
try {
    apiInstance.apiV2TestdataPermissionsPost(testDataPermissionsGrantRequest)
} catch (e: ClientException) {
    println("4xx response calling DaneTestoweKsefApi#apiV2TestdataPermissionsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DaneTestoweKsefApi#apiV2TestdataPermissionsPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **testDataPermissionsGrantRequest** | [**TestDataPermissionsGrantRequest**](TestDataPermissionsGrantRequest.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2TestdataPermissionsRevokePost"></a>
# **apiV2TestdataPermissionsRevokePost**
> apiV2TestdataPermissionsRevokePost(testDataPermissionsRevokeRequest)

Odebranie uprawnień testowemu podmiotowi/osobie fizycznej

Odbieranie uprawnień nadanych testowemu podmiotowi lub osobie fizycznej, a także w ich kontekście.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = DaneTestoweKsefApi()
val testDataPermissionsRevokeRequest : TestDataPermissionsRevokeRequest =  // TestDataPermissionsRevokeRequest | 
try {
    apiInstance.apiV2TestdataPermissionsRevokePost(testDataPermissionsRevokeRequest)
} catch (e: ClientException) {
    println("4xx response calling DaneTestoweKsefApi#apiV2TestdataPermissionsRevokePost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DaneTestoweKsefApi#apiV2TestdataPermissionsRevokePost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **testDataPermissionsRevokeRequest** | [**TestDataPermissionsRevokeRequest**](TestDataPermissionsRevokeRequest.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2TestdataPersonPost"></a>
# **apiV2TestdataPersonPost**
> apiV2TestdataPersonPost(personCreateRequest)

Utworzenie osoby fizycznej

Tworzenie nowej osoby fizycznej, której system nadaje uprawnienia właścicielskie. Można również określić, czy osoba ta jest komornikiem – wówczas otrzyma odpowiednie uprawnienie egzekucyjne.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = DaneTestoweKsefApi()
val personCreateRequest : PersonCreateRequest =  // PersonCreateRequest | 
try {
    apiInstance.apiV2TestdataPersonPost(personCreateRequest)
} catch (e: ClientException) {
    println("4xx response calling DaneTestoweKsefApi#apiV2TestdataPersonPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DaneTestoweKsefApi#apiV2TestdataPersonPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **personCreateRequest** | [**PersonCreateRequest**](PersonCreateRequest.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2TestdataPersonRemovePost"></a>
# **apiV2TestdataPersonRemovePost**
> apiV2TestdataPersonRemovePost(personRemoveRequest)

Usunięcie osoby fizycznej

Usuwanie testowej osoby fizycznej. System automatycznie odbierze jej wszystkie uprawnienia.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = DaneTestoweKsefApi()
val personRemoveRequest : PersonRemoveRequest =  // PersonRemoveRequest | 
try {
    apiInstance.apiV2TestdataPersonRemovePost(personRemoveRequest)
} catch (e: ClientException) {
    println("4xx response calling DaneTestoweKsefApi#apiV2TestdataPersonRemovePost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DaneTestoweKsefApi#apiV2TestdataPersonRemovePost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **personRemoveRequest** | [**PersonRemoveRequest**](PersonRemoveRequest.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2TestdataSubjectPost"></a>
# **apiV2TestdataSubjectPost**
> apiV2TestdataSubjectPost(subjectCreateRequest)

Utworzenie podmiotu

Tworzenie nowego podmiotu testowego. W przypadku grupy VAT i JST istnieje możliwość stworzenia jednostek podrzędnych. W wyniku takiego działania w systemie powstanie powiązanie między tymi podmiotami.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = DaneTestoweKsefApi()
val subjectCreateRequest : SubjectCreateRequest =  // SubjectCreateRequest | 
try {
    apiInstance.apiV2TestdataSubjectPost(subjectCreateRequest)
} catch (e: ClientException) {
    println("4xx response calling DaneTestoweKsefApi#apiV2TestdataSubjectPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DaneTestoweKsefApi#apiV2TestdataSubjectPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subjectCreateRequest** | [**SubjectCreateRequest**](SubjectCreateRequest.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2TestdataSubjectRemovePost"></a>
# **apiV2TestdataSubjectRemovePost**
> apiV2TestdataSubjectRemovePost(subjectRemoveRequest)

Usunięcie podmiotu

Usuwanie podmiotu testowego. W przypadku grupy VAT i JST usunięte zostaną również jednostki podrzędne.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = DaneTestoweKsefApi()
val subjectRemoveRequest : SubjectRemoveRequest =  // SubjectRemoveRequest | 
try {
    apiInstance.apiV2TestdataSubjectRemovePost(subjectRemoveRequest)
} catch (e: ClientException) {
    println("4xx response calling DaneTestoweKsefApi#apiV2TestdataSubjectRemovePost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling DaneTestoweKsefApi#apiV2TestdataSubjectRemovePost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subjectRemoveRequest** | [**SubjectRemoveRequest**](SubjectRemoveRequest.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

