# OperacjeKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2PermissionsAttachmentsStatusGet**](OperacjeKsefApi.md#apiV2PermissionsAttachmentsStatusGet) | **GET** /api/v2/permissions/attachments/status | Sprawdzenie statusu zgody na wystawianie faktur z załącznikiem |
| [**apiV2PermissionsOperationsOperationReferenceNumberGet**](OperacjeKsefApi.md#apiV2PermissionsOperationsOperationReferenceNumberGet) | **GET** /api/v2/permissions/operations/{operationReferenceNumber} | Pobranie statusu operacji |


<a id="apiV2PermissionsAttachmentsStatusGet"></a>
# **apiV2PermissionsAttachmentsStatusGet**
> CheckAttachmentPermissionStatusResponse apiV2PermissionsAttachmentsStatusGet()

Sprawdzenie statusu zgody na wystawianie faktur z załącznikiem

Sprawdzenie czy obecny kontekst posiada zgodę na wystawianie faktur z załącznikiem.  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;, &#x60;CredentialsRead&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = OperacjeKsefApi()
try {
    val result : CheckAttachmentPermissionStatusResponse = apiInstance.apiV2PermissionsAttachmentsStatusGet()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OperacjeKsefApi#apiV2PermissionsAttachmentsStatusGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OperacjeKsefApi#apiV2PermissionsAttachmentsStatusGet")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**CheckAttachmentPermissionStatusResponse**](CheckAttachmentPermissionStatusResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2PermissionsOperationsOperationReferenceNumberGet"></a>
# **apiV2PermissionsOperationsOperationReferenceNumberGet**
> PermissionsOperationStatusResponse apiV2PermissionsOperationsOperationReferenceNumberGet(operationReferenceNumber)

Pobranie statusu operacji

Zwraca status operacji asynchronicznej związanej z nadaniem lub odebraniem uprawnień.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = OperacjeKsefApi()
val operationReferenceNumber : kotlin.String = operationReferenceNumber_example // kotlin.String | Numer referencyjny operacji
try {
    val result : PermissionsOperationStatusResponse = apiInstance.apiV2PermissionsOperationsOperationReferenceNumberGet(operationReferenceNumber)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling OperacjeKsefApi#apiV2PermissionsOperationsOperationReferenceNumberGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling OperacjeKsefApi#apiV2PermissionsOperationsOperationReferenceNumberGet")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **operationReferenceNumber** | **kotlin.String**| Numer referencyjny operacji | |

### Return type

[**PermissionsOperationStatusResponse**](PermissionsOperationStatusResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

