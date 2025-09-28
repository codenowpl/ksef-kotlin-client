# CertyfikatyKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2CertificatesCertificateSerialNumberRevokePost**](CertyfikatyKsefApi.md#apiV2CertificatesCertificateSerialNumberRevokePost) | **POST** /api/v2/certificates/{certificateSerialNumber}/revoke | Unieważnienie certyfikatu |
| [**apiV2CertificatesEnrollmentsDataGet**](CertyfikatyKsefApi.md#apiV2CertificatesEnrollmentsDataGet) | **GET** /api/v2/certificates/enrollments/data | Pobranie danych do wniosku certyfikacyjnego |
| [**apiV2CertificatesEnrollmentsPost**](CertyfikatyKsefApi.md#apiV2CertificatesEnrollmentsPost) | **POST** /api/v2/certificates/enrollments | Wysyłka wniosku certyfikacyjnego |
| [**apiV2CertificatesEnrollmentsReferenceNumberGet**](CertyfikatyKsefApi.md#apiV2CertificatesEnrollmentsReferenceNumberGet) | **GET** /api/v2/certificates/enrollments/{referenceNumber} | Pobranie statusu przetwarzania wniosku certyfikacyjnego |
| [**apiV2CertificatesLimitsGet**](CertyfikatyKsefApi.md#apiV2CertificatesLimitsGet) | **GET** /api/v2/certificates/limits | Pobranie danych o limitach certyfikatów |
| [**apiV2CertificatesQueryPost**](CertyfikatyKsefApi.md#apiV2CertificatesQueryPost) | **POST** /api/v2/certificates/query | Pobranie listy metadanych certyfikatów |
| [**apiV2CertificatesRetrievePost**](CertyfikatyKsefApi.md#apiV2CertificatesRetrievePost) | **POST** /api/v2/certificates/retrieve | Pobranie certyfikatu lub listy certyfikatów |


<a id="apiV2CertificatesCertificateSerialNumberRevokePost"></a>
# **apiV2CertificatesCertificateSerialNumberRevokePost**
> apiV2CertificatesCertificateSerialNumberRevokePost(certificateSerialNumber, revokeCertificateRequest)

Unieważnienie certyfikatu

Unieważnia certyfikat o podanym numerze seryjnym.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = CertyfikatyKsefApi()
val certificateSerialNumber : kotlin.String = certificateSerialNumber_example // kotlin.String | Numer seryjny certyfikatu (w formacie szesnastkowym).
val revokeCertificateRequest : RevokeCertificateRequest =  // RevokeCertificateRequest | 
try {
    apiInstance.apiV2CertificatesCertificateSerialNumberRevokePost(certificateSerialNumber, revokeCertificateRequest)
} catch (e: ClientException) {
    println("4xx response calling CertyfikatyKsefApi#apiV2CertificatesCertificateSerialNumberRevokePost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CertyfikatyKsefApi#apiV2CertificatesCertificateSerialNumberRevokePost")
    e.printStackTrace()
}
```

### Parameters
| **certificateSerialNumber** | **kotlin.String**| Numer seryjny certyfikatu (w formacie szesnastkowym). | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **revokeCertificateRequest** | [**RevokeCertificateRequest**](RevokeCertificateRequest.md)|  | [optional] |

### Return type

null (empty response body)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2CertificatesEnrollmentsDataGet"></a>
# **apiV2CertificatesEnrollmentsDataGet**
> CertificateEnrollmentDataResponse apiV2CertificatesEnrollmentsDataGet()

Pobranie danych do wniosku certyfikacyjnego

Zwraca dane wymagane do przygotowania wniosku certyfikacyjnego PKCS#10.  Dane te są zwracane na podstawie certyfikatu użytego w procesie uwierzytelnienia i identyfikują podmiot, który składa wniosek o certyfikat.   &gt; Więcej informacji: &gt; - [Pobranie danych do wniosku certyfikacyjnego](https://github.com/CIRFMF/ksef-client-docs/blob/main/certyfikaty-wewn%C4%99trzne-KSeF.md#2-pobranie-danych-do-wniosku-certyfikacyjnego) &gt; - [Przygotowanie wniosku](https://github.com/CIRFMF/ksef-client-docs/blob/main/certyfikaty-wewn%C4%99trzne-KSeF.md#3-przygotowanie-csr-certificate-signing-request)

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = CertyfikatyKsefApi()
try {
    val result : CertificateEnrollmentDataResponse = apiInstance.apiV2CertificatesEnrollmentsDataGet()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CertyfikatyKsefApi#apiV2CertificatesEnrollmentsDataGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CertyfikatyKsefApi#apiV2CertificatesEnrollmentsDataGet")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**CertificateEnrollmentDataResponse**](CertificateEnrollmentDataResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2CertificatesEnrollmentsPost"></a>
# **apiV2CertificatesEnrollmentsPost**
> EnrollCertificateResponse apiV2CertificatesEnrollmentsPost(enrollCertificateRequest)

Wysyłka wniosku certyfikacyjnego

Przyjmuje wniosek certyfikacyjny i rozpoczyna jego przetwarzanie.  Dozwolone typy kluczy prywatnych: - RSA (OID: 1.2.840.113549.1.1.1), długość klucza równa 2048 bitów, - EC (klucze oparte na krzywych eliptycznych, OID: 1.2.840.10045.2.1), krzywa NIST P-256 (secp256r1)  Zalecane jest stosowanie kluczy EC.  Dozwolone algorytmy podpisu: - RSA PKCS#1 v1.5, - RSA PSS, - ECDSA (format podpisu zgodny z RFC 3279)  Dozwolone funkcje skrótu użyte do podpisu CSR: - SHA1, - SHA256, - SHA384, - SHA512  &gt; Więcej informacji: &gt; - [Wysłanie wniosku certyfikacyjnego](https://github.com/CIRFMF/ksef-client-docs/blob/main/certyfikaty-wewn%C4%99trzne-KSeF.md#4-wys%C5%82anie-wniosku-certyfikacyjnego)

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = CertyfikatyKsefApi()
val enrollCertificateRequest : EnrollCertificateRequest =  // EnrollCertificateRequest | 
try {
    val result : EnrollCertificateResponse = apiInstance.apiV2CertificatesEnrollmentsPost(enrollCertificateRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CertyfikatyKsefApi#apiV2CertificatesEnrollmentsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CertyfikatyKsefApi#apiV2CertificatesEnrollmentsPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **enrollCertificateRequest** | [**EnrollCertificateRequest**](EnrollCertificateRequest.md)|  | [optional] |

### Return type

[**EnrollCertificateResponse**](EnrollCertificateResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2CertificatesEnrollmentsReferenceNumberGet"></a>
# **apiV2CertificatesEnrollmentsReferenceNumberGet**
> CertificateEnrollmentStatusResponse apiV2CertificatesEnrollmentsReferenceNumberGet(referenceNumber)

Pobranie statusu przetwarzania wniosku certyfikacyjnego

Zwraca informacje o statusie wniosku certyfikacyjnego.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = CertyfikatyKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny wniosku certyfikacyjnego
try {
    val result : CertificateEnrollmentStatusResponse = apiInstance.apiV2CertificatesEnrollmentsReferenceNumberGet(referenceNumber)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CertyfikatyKsefApi#apiV2CertificatesEnrollmentsReferenceNumberGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CertyfikatyKsefApi#apiV2CertificatesEnrollmentsReferenceNumberGet")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **referenceNumber** | **kotlin.String**| Numer referencyjny wniosku certyfikacyjnego | |

### Return type

[**CertificateEnrollmentStatusResponse**](CertificateEnrollmentStatusResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2CertificatesLimitsGet"></a>
# **apiV2CertificatesLimitsGet**
> CertificateLimitsResponse apiV2CertificatesLimitsGet()

Pobranie danych o limitach certyfikatów

Zwraca informacje o limitach certyfikatów oraz informacje czy użytkownik może zawnioskować o certyfikat KSeF.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = CertyfikatyKsefApi()
try {
    val result : CertificateLimitsResponse = apiInstance.apiV2CertificatesLimitsGet()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CertyfikatyKsefApi#apiV2CertificatesLimitsGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CertyfikatyKsefApi#apiV2CertificatesLimitsGet")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**CertificateLimitsResponse**](CertificateLimitsResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2CertificatesQueryPost"></a>
# **apiV2CertificatesQueryPost**
> QueryCertificatesResponse apiV2CertificatesQueryPost(pageSize, pageOffset, queryCertificatesRequest)

Pobranie listy metadanych certyfikatów

Zwraca listę certyfikatów spełniających podane kryteria wyszukiwania. W przypadku braku podania kryteriów wyszukiwania zwrócona zostanie nieprzefiltrowana lista.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = CertyfikatyKsefApi()
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników
val pageOffset : kotlin.Int = 56 // kotlin.Int | Numer strony wyników
val queryCertificatesRequest : QueryCertificatesRequest =  // QueryCertificatesRequest | Kryteria filtrowania
try {
    val result : QueryCertificatesResponse = apiInstance.apiV2CertificatesQueryPost(pageSize, pageOffset, queryCertificatesRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CertyfikatyKsefApi#apiV2CertificatesQueryPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CertyfikatyKsefApi#apiV2CertificatesQueryPost")
    e.printStackTrace()
}
```

### Parameters
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników | [optional] [default to 10] |
| **pageOffset** | **kotlin.Int**| Numer strony wyników | [optional] [default to 0] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **queryCertificatesRequest** | [**QueryCertificatesRequest**](QueryCertificatesRequest.md)| Kryteria filtrowania | [optional] |

### Return type

[**QueryCertificatesResponse**](QueryCertificatesResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2CertificatesRetrievePost"></a>
# **apiV2CertificatesRetrievePost**
> RetrieveCertificatesResponse apiV2CertificatesRetrievePost(retrieveCertificatesRequest)

Pobranie certyfikatu lub listy certyfikatów

Zwraca certyfikaty o podanych numerach seryjnych w formacie DER zakodowanym w Base64.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = CertyfikatyKsefApi()
val retrieveCertificatesRequest : RetrieveCertificatesRequest = {"certificateSerialNumbers":["0321C82DA41B4362","0321F21DA462A362"]} // RetrieveCertificatesRequest | 
try {
    val result : RetrieveCertificatesResponse = apiInstance.apiV2CertificatesRetrievePost(retrieveCertificatesRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling CertyfikatyKsefApi#apiV2CertificatesRetrievePost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling CertyfikatyKsefApi#apiV2CertificatesRetrievePost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **retrieveCertificatesRequest** | [**RetrieveCertificatesRequest**](RetrieveCertificatesRequest.md)|  | [optional] |

### Return type

[**RetrieveCertificatesResponse**](RetrieveCertificatesResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

