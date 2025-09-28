# WysykaInteraktywnaKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2SessionsOnlineReferenceNumberClosePost**](WysykaInteraktywnaKsefApi.md#apiV2SessionsOnlineReferenceNumberClosePost) | **POST** /api/v2/sessions/online/{referenceNumber}/close | Zamknięcie sesji interaktywnej |
| [**apiV2SessionsOnlineReferenceNumberInvoicesPost**](WysykaInteraktywnaKsefApi.md#apiV2SessionsOnlineReferenceNumberInvoicesPost) | **POST** /api/v2/sessions/online/{referenceNumber}/invoices | Wysłanie faktury |
| [**onlineSessionOpen**](WysykaInteraktywnaKsefApi.md#onlineSessionOpen) | **POST** /api/v2/sessions/online | Otwarcie sesji interaktywnej |


<a id="apiV2SessionsOnlineReferenceNumberClosePost"></a>
# **apiV2SessionsOnlineReferenceNumberClosePost**
> apiV2SessionsOnlineReferenceNumberClosePost(referenceNumber)

Zamknięcie sesji interaktywnej

Zamyka sesję interaktywną i rozpoczyna generowanie zbiorczego UPO dla sesji.  Wymagane uprawnienia: &#x60;InvoiceWrite&#x60;, &#x60;PefInvoiceWrite&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = WysykaInteraktywnaKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny sesji
try {
    apiInstance.apiV2SessionsOnlineReferenceNumberClosePost(referenceNumber)
} catch (e: ClientException) {
    println("4xx response calling WysykaInteraktywnaKsefApi#apiV2SessionsOnlineReferenceNumberClosePost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WysykaInteraktywnaKsefApi#apiV2SessionsOnlineReferenceNumberClosePost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **referenceNumber** | **kotlin.String**| Numer referencyjny sesji | |

### Return type

null (empty response body)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2SessionsOnlineReferenceNumberInvoicesPost"></a>
# **apiV2SessionsOnlineReferenceNumberInvoicesPost**
> SendInvoiceResponse apiV2SessionsOnlineReferenceNumberInvoicesPost(referenceNumber, sendInvoiceRequest)

Wysłanie faktury

Przyjmuje zaszyfrowaną fakturę oraz jej metadane i rozpoczyna jej przetwarzanie.  &gt; Więcej informacji: &gt; - [Wysłanie faktury](https://github.com/CIRFMF/ksef-docs/blob/main/sesja-interaktywna.md#2-wys%C5%82anie-faktury)  Wymagane uprawnienia: &#x60;InvoiceWrite&#x60;, &#x60;PefInvoiceWrite&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = WysykaInteraktywnaKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny sesji
val sendInvoiceRequest : SendInvoiceRequest = {"invoiceHash":"EbrK4cOSjW4hEpJaHU71YXSOZZmqP5++dK9nLgTzgV4=","invoiceSize":6480,"encryptedInvoiceHash":"miYb1z3Ljw5VucTZslv3Tlt+V/EK1V8Q8evD8HMQ0dc=","encryptedInvoiceSize":6496,"encryptedInvoiceContent":"...","offlineMode":false} // SendInvoiceRequest | Dane faktury
try {
    val result : SendInvoiceResponse = apiInstance.apiV2SessionsOnlineReferenceNumberInvoicesPost(referenceNumber, sendInvoiceRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WysykaInteraktywnaKsefApi#apiV2SessionsOnlineReferenceNumberInvoicesPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WysykaInteraktywnaKsefApi#apiV2SessionsOnlineReferenceNumberInvoicesPost")
    e.printStackTrace()
}
```

### Parameters
| **referenceNumber** | **kotlin.String**| Numer referencyjny sesji | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **sendInvoiceRequest** | [**SendInvoiceRequest**](SendInvoiceRequest.md)| Dane faktury | [optional] |

### Return type

[**SendInvoiceResponse**](SendInvoiceResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="onlineSessionOpen"></a>
# **onlineSessionOpen**
> OpenOnlineSessionResponse onlineSessionOpen(openOnlineSessionRequest)

Otwarcie sesji interaktywnej

Otwiera sesję do wysyłki pojedynczych faktur. Należy przekazać schemat wysyłanych faktur oraz informacje o kluczu używanym do szyfrowania.  &gt; Więcej informacji: &gt; - [Otwarcie sesji interaktywnej](https://github.com/CIRFMF/ksef-docs/blob/main/sesja-interaktywna.md#1-otwarcie-sesji) &gt; - [Klucz publiczny Ministersta Finansów](/docs/v2/index.html#tag/Certyfikaty-klucza-publicznego)  Wymagane uprawnienia: &#x60;InvoiceWrite&#x60;, &#x60;PefInvoiceWrite&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = WysykaInteraktywnaKsefApi()
val openOnlineSessionRequest : OpenOnlineSessionRequest = {"formCode":{"systemCode":"FA (3)","schemaVersion":"1-0E","value":"FA"},"encryption":{"encryptedSymmetricKey":"bdUVjqLj+y2q6aBUuLxxXYAMqeDuIBRTyr+hB96DaWKaGzuVHw9p+Nk9vhzgF/Q5cavK2k6eCh6SdsrWI0s9mFFj4A4UJtsyD8Dn3esLfUZ5A1juuG3q3SBi/XOC/+9W+0T/KdwdE393mbiUNyx1K/0bw31vKJL0COeJIDP7usAMDl42/H1TNvkjk+8iZ80V0qW7D+RZdz+tdiY1xV0f2mfgwJ46V0CpZ+sB9UAssRj+eVffavJ0TOg2b5JaBxE8MCAvrF6rO5K4KBjUmoy7PP7g1qIbm8xI2GO0KnfPOO5OWj8rsotRwBgu7x19Ine3qYUvuvCZlXRGGZ5NHIzWPM4O74+gNalaMgFCsmv8mMhETSU4SfAGmJr9edxPjQSbgD5i2X4eDRDMwvyaAa7CP1b2oICju+0L7Fywd2ZtUcr6El++eTVoi8HYsTArntET++gULT7XXjmb8e3O0nxrYiYsE9GMJ7HBGv3NOoJ1NTm3a7U6+c0ZJiBVLvn6xXw10LQX243xH+ehsKo6djQJKYtqcNPaXtCwM1c9RrsOx/wRXyWCtTffqLiaR0LbYvfMJAcEWceG+RaeAx4p37OiQqdJypd6LAv9/0ECWK8Bip8yyoA+0EYiAJb9YuDz2YlQX9Mx9E9FzFIAsgEQ2w723HZYWgPywLb+dlsum4lTZKQ=","initializationVector":"OmtDQdl6vkOI1GLKZSjgEg=="}} // OpenOnlineSessionRequest | 
try {
    val result : OpenOnlineSessionResponse = apiInstance.onlineSessionOpen(openOnlineSessionRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WysykaInteraktywnaKsefApi#onlineSessionOpen")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WysykaInteraktywnaKsefApi#onlineSessionOpen")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **openOnlineSessionRequest** | [**OpenOnlineSessionRequest**](OpenOnlineSessionRequest.md)|  | [optional] |

### Return type

[**OpenOnlineSessionResponse**](OpenOnlineSessionResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

