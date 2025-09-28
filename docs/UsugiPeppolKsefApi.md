# UsugiPeppolKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2PeppolQueryGet**](UsugiPeppolKsefApi.md#apiV2PeppolQueryGet) | **GET** /api/v2/peppol/query | Pobranie listy dostawców usług Peppol |


<a id="apiV2PeppolQueryGet"></a>
# **apiV2PeppolQueryGet**
> QueryPeppolProvidersResponse apiV2PeppolQueryGet(pageOffset, pageSize)

Pobranie listy dostawców usług Peppol

Zwraca listę dostawców usług Peppol zarejestrowanych w systemie.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = UsugiPeppolKsefApi()
val pageOffset : kotlin.Int = 56 // kotlin.Int | Numer strony wyników.
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników.
try {
    val result : QueryPeppolProvidersResponse = apiInstance.apiV2PeppolQueryGet(pageOffset, pageSize)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling UsugiPeppolKsefApi#apiV2PeppolQueryGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling UsugiPeppolKsefApi#apiV2PeppolQueryGet")
    e.printStackTrace()
}
```

### Parameters
| **pageOffset** | **kotlin.Int**| Numer strony wyników. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. | [optional] |

### Return type

[**QueryPeppolProvidersResponse**](QueryPeppolProvidersResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

