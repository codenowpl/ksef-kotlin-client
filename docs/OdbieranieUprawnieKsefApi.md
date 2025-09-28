# OdbieranieUprawnieKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2PermissionsAuthorizationsGrantsPermissionIdDelete**](OdbieranieUprawnieKsefApi.md#apiV2PermissionsAuthorizationsGrantsPermissionIdDelete) | **DELETE** /api/v2/permissions/authorizations/grants/{permissionId} | Odebranie uprawnień podmiotowych |
| [**apiV2PermissionsCommonGrantsPermissionIdDelete**](OdbieranieUprawnieKsefApi.md#apiV2PermissionsCommonGrantsPermissionIdDelete) | **DELETE** /api/v2/permissions/common/grants/{permissionId} | Odebranie uprawnień |


<a id="apiV2PermissionsAuthorizationsGrantsPermissionIdDelete"></a>
# **apiV2PermissionsAuthorizationsGrantsPermissionIdDelete**
> PermissionsOperationResponse apiV2PermissionsAuthorizationsGrantsPermissionIdDelete(permissionId)

Odebranie uprawnień podmiotowych

Rozpoczyna asynchroniczną operacje odbierania uprawnienia o podanym identyfikatorze. Ta metoda służy do odbierania uprawnień podmiotowych.  &gt; Więcej informacji: &gt; - [Odbieranie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#odebranie-uprawnie%C5%84-podmiotowych)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = OdbieranieUprawnieKsefApi()
val permissionId : kotlin.String = permissionId_example // kotlin.String | Id uprawnienia.
try {
    val result : PermissionsOperationResponse = apiInstance.apiV2PermissionsAuthorizationsGrantsPermissionIdDelete(permissionId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OdbieranieUprawnieKsefApi#apiV2PermissionsAuthorizationsGrantsPermissionIdDelete")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OdbieranieUprawnieKsefApi#apiV2PermissionsAuthorizationsGrantsPermissionIdDelete")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **permissionId** | **kotlin.String**| Id uprawnienia. | |

### Return type

[**PermissionsOperationResponse**](PermissionsOperationResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2PermissionsCommonGrantsPermissionIdDelete"></a>
# **apiV2PermissionsCommonGrantsPermissionIdDelete**
> PermissionsOperationResponse apiV2PermissionsCommonGrantsPermissionIdDelete(permissionId)

Odebranie uprawnień

Rozpoczyna asynchroniczną operacje odbierania uprawnienia o podanym identyfikatorze.  Ta metoda służy do odbierania uprawnień takich jak: - nadanych nadanych osobom fizycznym lub podmiotom do pracy w KSeF - nadanych podmiotom do obsługi faktur - nadanych w sposób pośredni - administratorów jednostek i podmiotów podrzędnych - administratorów podmiotów unijnych uprawnionych do samofakturowania - reprezentantów podmiotów unijnych  &gt; Więcej informacji: &gt; - [Odbieranie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#odebranie-uprawnie%C5%84)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;, &#x60;VatUeManage&#x60;, &#x60;SubunitManage&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = OdbieranieUprawnieKsefApi()
val permissionId : kotlin.String = permissionId_example // kotlin.String | Id uprawnienia.
try {
    val result : PermissionsOperationResponse = apiInstance.apiV2PermissionsCommonGrantsPermissionIdDelete(permissionId)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OdbieranieUprawnieKsefApi#apiV2PermissionsCommonGrantsPermissionIdDelete")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OdbieranieUprawnieKsefApi#apiV2PermissionsCommonGrantsPermissionIdDelete")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **permissionId** | **kotlin.String**| Id uprawnienia. | |

### Return type

[**PermissionsOperationResponse**](PermissionsOperationResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

