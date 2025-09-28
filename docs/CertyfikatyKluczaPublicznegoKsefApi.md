# CertyfikatyKluczaPublicznegoKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2SecurityPublicKeyCertificatesGet**](CertyfikatyKluczaPublicznegoKsefApi.md#apiV2SecurityPublicKeyCertificatesGet) | **GET** /api/v2/security/public-key-certificates | Pobranie certyfikatów |


<a id="apiV2SecurityPublicKeyCertificatesGet"></a>
# **apiV2SecurityPublicKeyCertificatesGet**
> kotlin.collections.List&lt;PublicKeyCertificate&gt; apiV2SecurityPublicKeyCertificatesGet()

Pobranie certyfikatów

Zwraca informacje o kluczach publicznych używanych do szyfrowania danych przesyłanych do systemu KSeF.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = CertyfikatyKluczaPublicznegoKsefApi()
try {
    val result : kotlin.collections.List<PublicKeyCertificate> = apiInstance.apiV2SecurityPublicKeyCertificatesGet()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CertyfikatyKluczaPublicznegoKsefApi#apiV2SecurityPublicKeyCertificatesGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CertyfikatyKluczaPublicznegoKsefApi#apiV2SecurityPublicKeyCertificatesGet")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**kotlin.collections.List&lt;PublicKeyCertificate&gt;**](PublicKeyCertificate.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

