# StatusWysykiIUPOKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2SessionsGet**](StatusWysykiIUPOKsefApi.md#apiV2SessionsGet) | **GET** /api/v2/sessions | Pobranie listy sesji |
| [**apiV2SessionsReferenceNumberGet**](StatusWysykiIUPOKsefApi.md#apiV2SessionsReferenceNumberGet) | **GET** /api/v2/sessions/{referenceNumber} | Pobranie statusu sesji |
| [**apiV2SessionsReferenceNumberInvoicesFailedGet**](StatusWysykiIUPOKsefApi.md#apiV2SessionsReferenceNumberInvoicesFailedGet) | **GET** /api/v2/sessions/{referenceNumber}/invoices/failed | Pobranie niepoprawnie przetworzonych faktur sesji |
| [**apiV2SessionsReferenceNumberInvoicesGet**](StatusWysykiIUPOKsefApi.md#apiV2SessionsReferenceNumberInvoicesGet) | **GET** /api/v2/sessions/{referenceNumber}/invoices | Pobranie faktur sesji |
| [**apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet**](StatusWysykiIUPOKsefApi.md#apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet) | **GET** /api/v2/sessions/{referenceNumber}/invoices/{invoiceReferenceNumber} | Pobranie statusu faktury z sesji |
| [**apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet**](StatusWysykiIUPOKsefApi.md#apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet) | **GET** /api/v2/sessions/{referenceNumber}/invoices/{invoiceReferenceNumber}/upo | Pobranie UPO faktury z sesji na podstawie numeru referencyjnego faktury |
| [**apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet**](StatusWysykiIUPOKsefApi.md#apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet) | **GET** /api/v2/sessions/{referenceNumber}/invoices/ksef/{ksefNumber}/upo | Pobranie UPO faktury z sesji na podstawie numeru KSeF |
| [**apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet**](StatusWysykiIUPOKsefApi.md#apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet) | **GET** /api/v2/sessions/{referenceNumber}/upo/{upoReferenceNumber} | Pobranie UPO dla sesji |


<a id="apiV2SessionsGet"></a>
# **apiV2SessionsGet**
> SessionsQueryResponse apiV2SessionsGet(sessionType, pageSize, referenceNumber, dateCreatedFrom, dateCreatedTo, dateClosedFrom, dateClosedTo, dateModifiedFrom, dateModifiedTo, statuses, xContinuationToken)

Pobranie listy sesji

Zwraca listę sesji spełniających podane kryteria wyszukiwania.  Wymagane uprawnienia: - &#x60;Introspection&#x60; – pozwala pobrać wszystkie sesje w bieżącym kontekście uwierzytelnienia &#x60;(ContextIdentifier)&#x60;. - &#x60;InvoiceWrite&#x60; – pozwala pobrać wyłącznie sesje utworzone przez podmiot uwierzytelniający, czyli podmiot inicjujący uwierzytelnienie.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = StatusWysykiIUPOKsefApi()
val sessionType : SessionType =  // SessionType | Typ sesji. | Wartość | Opis | | --- | --- | | Online | Wysyłka interaktywna (pojedyncze faktury). | | Batch | Wysyłka wsadowa (paczka faktur). | 
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony.
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny sesji.
val dateCreatedFrom : java.time.LocalDateTime = 2013-10-20T19:20:30+01:00 // java.time.LocalDateTime | Data utworzenia sesji (od).
val dateCreatedTo : java.time.LocalDateTime = 2013-10-20T19:20:30+01:00 // java.time.LocalDateTime | Data utworzenia sesji (do).
val dateClosedFrom : java.time.LocalDateTime = 2013-10-20T19:20:30+01:00 // java.time.LocalDateTime | Data zamknięcia sesji (od).
val dateClosedTo : java.time.LocalDateTime = 2013-10-20T19:20:30+01:00 // java.time.LocalDateTime | Data zamknięcia sesji (do).
val dateModifiedFrom : java.time.LocalDateTime = 2013-10-20T19:20:30+01:00 // java.time.LocalDateTime | Data ostatniej aktywności (wysyłka faktury lub zmiana statusu) w ramach sesji (od).
val dateModifiedTo : java.time.LocalDateTime = 2013-10-20T19:20:30+01:00 // java.time.LocalDateTime | Data ostatniej aktywności (wysyłka faktury lub zmiana statusu) w ramach sesji (do).
val statuses : kotlin.collections.List<CommonSessionStatus> =  // kotlin.collections.List<CommonSessionStatus> | Statusy sesji. | Wartość | Opis | | --- | --- | | InProgress | Sesja aktywna. | | Succeeded | Sesja przetworzona poprawnie.            W trakcie przetwarzania sesji nie wystąpiły żadne błędy, ale część faktur nadal mogła zostać odrzucona. | | Failed | Sesja nie przetworzona z powodu błędów.            Na etapie rozpoczynania lub kończenia sesji wystąpiły błędy, które nie pozwoliły na jej poprawne przetworzenie. | | Cancelled | Sesja anulowania.            Został przekroczony czas na wysyłkę w sesji wsadowej, lub nie przesłano żadnych faktur w sesji interaktywnej. | 
val xContinuationToken : kotlin.String = xContinuationToken_example // kotlin.String | Token służący do pobrania kolejnej strony wyników.
try {
    val result : SessionsQueryResponse = apiInstance.apiV2SessionsGet(sessionType, pageSize, referenceNumber, dateCreatedFrom, dateCreatedTo, dateClosedFrom, dateClosedTo, dateModifiedFrom, dateModifiedTo, statuses, xContinuationToken)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsGet")
    e.printStackTrace()
}
```

### Parameters
| **sessionType** | [**SessionType**](.md)| Typ sesji. | Wartość | Opis | | --- | --- | | Online | Wysyłka interaktywna (pojedyncze faktury). | | Batch | Wysyłka wsadowa (paczka faktur). |  | [enum: Online, Batch] |
| **pageSize** | **kotlin.Int**| Rozmiar strony. | [optional] |
| **referenceNumber** | **kotlin.String**| Numer referencyjny sesji. | [optional] |
| **dateCreatedFrom** | **java.time.LocalDateTime**| Data utworzenia sesji (od). | [optional] |
| **dateCreatedTo** | **java.time.LocalDateTime**| Data utworzenia sesji (do). | [optional] |
| **dateClosedFrom** | **java.time.LocalDateTime**| Data zamknięcia sesji (od). | [optional] |
| **dateClosedTo** | **java.time.LocalDateTime**| Data zamknięcia sesji (do). | [optional] |
| **dateModifiedFrom** | **java.time.LocalDateTime**| Data ostatniej aktywności (wysyłka faktury lub zmiana statusu) w ramach sesji (od). | [optional] |
| **dateModifiedTo** | **java.time.LocalDateTime**| Data ostatniej aktywności (wysyłka faktury lub zmiana statusu) w ramach sesji (do). | [optional] |
| **statuses** | [**kotlin.collections.List&lt;CommonSessionStatus&gt;**](CommonSessionStatus.md)| Statusy sesji. | Wartość | Opis | | --- | --- | | InProgress | Sesja aktywna. | | Succeeded | Sesja przetworzona poprawnie.            W trakcie przetwarzania sesji nie wystąpiły żadne błędy, ale część faktur nadal mogła zostać odrzucona. | | Failed | Sesja nie przetworzona z powodu błędów.            Na etapie rozpoczynania lub kończenia sesji wystąpiły błędy, które nie pozwoliły na jej poprawne przetworzenie. | | Cancelled | Sesja anulowania.            Został przekroczony czas na wysyłkę w sesji wsadowej, lub nie przesłano żadnych faktur w sesji interaktywnej. |  | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xContinuationToken** | **kotlin.String**| Token służący do pobrania kolejnej strony wyników. | [optional] |

### Return type

[**SessionsQueryResponse**](SessionsQueryResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2SessionsReferenceNumberGet"></a>
# **apiV2SessionsReferenceNumberGet**
> SessionStatusResponse apiV2SessionsReferenceNumberGet(referenceNumber)

Pobranie statusu sesji

Sprawdza bieżący status sesji o podanym numerze referencyjnym.  Wymagane uprawnienia: &#x60;InvoiceWrite&#x60;, &#x60;Introspection&#x60;, &#x60;PefInvoiceWrite&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = StatusWysykiIUPOKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny sesji.
try {
    val result : SessionStatusResponse = apiInstance.apiV2SessionsReferenceNumberGet(referenceNumber)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberGet")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **referenceNumber** | **kotlin.String**| Numer referencyjny sesji. | |

### Return type

[**SessionStatusResponse**](SessionStatusResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2SessionsReferenceNumberInvoicesFailedGet"></a>
# **apiV2SessionsReferenceNumberInvoicesFailedGet**
> SessionInvoicesResponse apiV2SessionsReferenceNumberInvoicesFailedGet(referenceNumber, xContinuationToken, pageSize)

Pobranie niepoprawnie przetworzonych faktur sesji

Zwraca listę niepoprawnie przetworzonych faktur przesłanych w sesji wraz z ich statusami.  Wymagane uprawnienia: &#x60;InvoiceWrite&#x60;, &#x60;Introspection&#x60;, &#x60;PefInvoiceWrite&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = StatusWysykiIUPOKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny sesji.
val xContinuationToken : kotlin.String = xContinuationToken_example // kotlin.String | Token służący do pobrania kolejnej strony wyników.
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników.
try {
    val result : SessionInvoicesResponse = apiInstance.apiV2SessionsReferenceNumberInvoicesFailedGet(referenceNumber, xContinuationToken, pageSize)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberInvoicesFailedGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberInvoicesFailedGet")
    e.printStackTrace()
}
```

### Parameters
| **referenceNumber** | **kotlin.String**| Numer referencyjny sesji. | |
| **xContinuationToken** | **kotlin.String**| Token służący do pobrania kolejnej strony wyników. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. | [optional] [default to 10] |

### Return type

[**SessionInvoicesResponse**](SessionInvoicesResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2SessionsReferenceNumberInvoicesGet"></a>
# **apiV2SessionsReferenceNumberInvoicesGet**
> SessionInvoicesResponse apiV2SessionsReferenceNumberInvoicesGet(referenceNumber, xContinuationToken, pageSize)

Pobranie faktur sesji

Zwraca listę faktur przesłanych w sesji wraz z ich statusami, oraz informacje na temat ilości poprawnie i niepoprawnie przetworzonych faktur.  Wymagane uprawnienia: &#x60;InvoiceWrite&#x60;, &#x60;Introspection&#x60;, &#x60;PefInvoiceWrite&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = StatusWysykiIUPOKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny sesji.
val xContinuationToken : kotlin.String = xContinuationToken_example // kotlin.String | Token służący do pobrania kolejnej strony wyników.
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników.
try {
    val result : SessionInvoicesResponse = apiInstance.apiV2SessionsReferenceNumberInvoicesGet(referenceNumber, xContinuationToken, pageSize)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberInvoicesGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberInvoicesGet")
    e.printStackTrace()
}
```

### Parameters
| **referenceNumber** | **kotlin.String**| Numer referencyjny sesji. | |
| **xContinuationToken** | **kotlin.String**| Token służący do pobrania kolejnej strony wyników. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. | [optional] [default to 10] |

### Return type

[**SessionInvoicesResponse**](SessionInvoicesResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet"></a>
# **apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet**
> SessionInvoiceStatusResponse apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet(referenceNumber, invoiceReferenceNumber)

Pobranie statusu faktury z sesji

Zwraca fakturę przesłaną w sesji wraz ze statusem.  Wymagane uprawnienia: &#x60;InvoiceWrite&#x60;, &#x60;Introspection&#x60;, &#x60;PefInvoiceWrite&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = StatusWysykiIUPOKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny sesji.
val invoiceReferenceNumber : kotlin.String = invoiceReferenceNumber_example // kotlin.String | Numer referencyjny faktury.
try {
    val result : SessionInvoiceStatusResponse = apiInstance.apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet(referenceNumber, invoiceReferenceNumber)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberGet")
    e.printStackTrace()
}
```

### Parameters
| **referenceNumber** | **kotlin.String**| Numer referencyjny sesji. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoiceReferenceNumber** | **kotlin.String**| Numer referencyjny faktury. | |

### Return type

[**SessionInvoiceStatusResponse**](SessionInvoiceStatusResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet"></a>
# **apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet**
> kotlin.String apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet(referenceNumber, invoiceReferenceNumber)

Pobranie UPO faktury z sesji na podstawie numeru referencyjnego faktury

Zwraca UPO faktury przesłanego w sesji na podstawie jego numeru KSeF.  Wymagane uprawnienia: &#x60;InvoiceWrite&#x60;, &#x60;Introspection&#x60;, &#x60;PefInvoiceWrite&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = StatusWysykiIUPOKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny sesji.
val invoiceReferenceNumber : kotlin.String = invoiceReferenceNumber_example // kotlin.String | Numer referencyjny faktury.
try {
    val result : kotlin.String = apiInstance.apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet(referenceNumber, invoiceReferenceNumber)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberInvoicesInvoiceReferenceNumberUpoGet")
    e.printStackTrace()
}
```

### Parameters
| **referenceNumber** | **kotlin.String**| Numer referencyjny sesji. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoiceReferenceNumber** | **kotlin.String**| Numer referencyjny faktury. | |

### Return type

**kotlin.String**

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet"></a>
# **apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet**
> kotlin.String apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet(referenceNumber, ksefNumber)

Pobranie UPO faktury z sesji na podstawie numeru KSeF

Zwraca UPO faktury przesłanego w sesji na podstawie jego numeru KSeF.  Wymagane uprawnienia: &#x60;InvoiceWrite&#x60;, &#x60;Introspection&#x60;, &#x60;PefInvoiceWrite&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = StatusWysykiIUPOKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny sesji.
val ksefNumber : kotlin.String = ksefNumber_example // kotlin.String | Numer KSeF faktury.
try {
    val result : kotlin.String = apiInstance.apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet(referenceNumber, ksefNumber)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberInvoicesKsefKsefNumberUpoGet")
    e.printStackTrace()
}
```

### Parameters
| **referenceNumber** | **kotlin.String**| Numer referencyjny sesji. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ksefNumber** | **kotlin.String**| Numer KSeF faktury. | |

### Return type

**kotlin.String**

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet"></a>
# **apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet**
> kotlin.String apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet(referenceNumber, upoReferenceNumber)

Pobranie UPO dla sesji

Zwraca XML zawierający zbiorcze UPO dla sesji.  Wymagane uprawnienia: &#x60;InvoiceWrite&#x60;, &#x60;Introspection&#x60;, &#x60;PefInvoiceWrite&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = StatusWysykiIUPOKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny sesji.
val upoReferenceNumber : kotlin.String = upoReferenceNumber_example // kotlin.String | Numer referencyjny UPO.
try {
    val result : kotlin.String = apiInstance.apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet(referenceNumber, upoReferenceNumber)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling StatusWysykiIUPOKsefApi#apiV2SessionsReferenceNumberUpoUpoReferenceNumberGet")
    e.printStackTrace()
}
```

### Parameters
| **referenceNumber** | **kotlin.String**| Numer referencyjny sesji. | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **upoReferenceNumber** | **kotlin.String**| Numer referencyjny UPO. | |

### Return type

**kotlin.String**

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

