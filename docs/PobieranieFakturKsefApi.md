# PobieranieFakturKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2InvoicesExportsOperationReferenceNumberGet**](PobieranieFakturKsefApi.md#apiV2InvoicesExportsOperationReferenceNumberGet) | **GET** /api/v2/invoices/exports/{operationReferenceNumber} | Pobranie statusu eksportu paczki faktur |
| [**apiV2InvoicesExportsPost**](PobieranieFakturKsefApi.md#apiV2InvoicesExportsPost) | **POST** /api/v2/invoices/exports | Eksport paczki faktur |
| [**apiV2InvoicesKsefKsefNumberGet**](PobieranieFakturKsefApi.md#apiV2InvoicesKsefKsefNumberGet) | **GET** /api/v2/invoices/ksef/{ksefNumber} | Pobranie faktury po numerze KSeF |
| [**apiV2InvoicesQueryMetadataPost**](PobieranieFakturKsefApi.md#apiV2InvoicesQueryMetadataPost) | **POST** /api/v2/invoices/query/metadata | Pobranie listy metadanych faktur |


<a id="apiV2InvoicesExportsOperationReferenceNumberGet"></a>
# **apiV2InvoicesExportsOperationReferenceNumberGet**
> InvoiceExportStatusResponse apiV2InvoicesExportsOperationReferenceNumberGet(operationReferenceNumber)

Pobranie statusu eksportu paczki faktur

  Wymagane uprawnienia: &#x60;InvoiceRead&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = PobieranieFakturKsefApi()
val operationReferenceNumber : kotlin.String = operationReferenceNumber_example // kotlin.String | Numer referencyjny operacji.
try {
    val result : InvoiceExportStatusResponse = apiInstance.apiV2InvoicesExportsOperationReferenceNumberGet(operationReferenceNumber)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PobieranieFakturKsefApi#apiV2InvoicesExportsOperationReferenceNumberGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PobieranieFakturKsefApi#apiV2InvoicesExportsOperationReferenceNumberGet")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **operationReferenceNumber** | **kotlin.String**| Numer referencyjny operacji. | |

### Return type

[**InvoiceExportStatusResponse**](InvoiceExportStatusResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2InvoicesExportsPost"></a>
# **apiV2InvoicesExportsPost**
> ExportInvoicesResponse apiV2InvoicesExportsPost(invoiceExportRequest)

Eksport paczki faktur

Rozpoczyna asynchroniczny proces wyszukiwania faktur w systemie KSeF na podstawie przekazanych filtrów oraz przygotowania ich w formie zaszyfrowanej paczki. Wymagane jest przekazanie informacji o szyfrowaniu w polu &#x60;Encryption&#x60;, które służą do zabezpieczenia przygotowanej paczki z fakturami.  Wymagane uprawnienia: &#x60;InvoiceRead&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = PobieranieFakturKsefApi()
val invoiceExportRequest : InvoiceExportRequest =  // InvoiceExportRequest | Dane wejściowe określające kryteria i format eksportu paczki faktur.
try {
    val result : ExportInvoicesResponse = apiInstance.apiV2InvoicesExportsPost(invoiceExportRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PobieranieFakturKsefApi#apiV2InvoicesExportsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PobieranieFakturKsefApi#apiV2InvoicesExportsPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoiceExportRequest** | [**InvoiceExportRequest**](InvoiceExportRequest.md)| Dane wejściowe określające kryteria i format eksportu paczki faktur. | [optional] |

### Return type

[**ExportInvoicesResponse**](ExportInvoicesResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2InvoicesKsefKsefNumberGet"></a>
# **apiV2InvoicesKsefKsefNumberGet**
> kotlin.String apiV2InvoicesKsefKsefNumberGet(ksefNumber)

Pobranie faktury po numerze KSeF

Zwraca fakturę o podanym numerze KSeF.  Wymagane uprawnienia: &#x60;InvoiceRead&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = PobieranieFakturKsefApi()
val ksefNumber : kotlin.String = ksefNumber_example // kotlin.String | Numer KSeF faktury.
try {
    val result : kotlin.String = apiInstance.apiV2InvoicesKsefKsefNumberGet(ksefNumber)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PobieranieFakturKsefApi#apiV2InvoicesKsefKsefNumberGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PobieranieFakturKsefApi#apiV2InvoicesKsefKsefNumberGet")
    e.printStackTrace()
}
```

### Parameters
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

<a id="apiV2InvoicesQueryMetadataPost"></a>
# **apiV2InvoicesQueryMetadataPost**
> QueryInvoicesMetadataResponse apiV2InvoicesQueryMetadataPost(pageOffset, pageSize, invoiceQueryFilters)

Pobranie listy metadanych faktur

Zwraca listę metadanych faktur spełniające podane kryteria wyszukiwania. Wyniki sortowane są rosnąco według typu daty przekazanej w &#x60;DateRange&#x60;. Do realizacji pobierania przyrostowego należy stosować typ &#x60;PermanentStorage&#x60;. Maksymalnie można pobrać faktury w zakresie do 10 000 rekordów  Wymagane uprawnienia: &#x60;InvoiceRead&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = PobieranieFakturKsefApi()
val pageOffset : kotlin.Int = 56 // kotlin.Int | Indeks pierwszej strony wyników (0 = pierwsza strona).
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników. Wartość musi zawierać się w przedziale od 10 do 250.
val invoiceQueryFilters : InvoiceQueryFilters =  // InvoiceQueryFilters | Zestaw filtrów dla wyszukiwania metadanych.
try {
    val result : QueryInvoicesMetadataResponse = apiInstance.apiV2InvoicesQueryMetadataPost(pageOffset, pageSize, invoiceQueryFilters)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling PobieranieFakturKsefApi#apiV2InvoicesQueryMetadataPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling PobieranieFakturKsefApi#apiV2InvoicesQueryMetadataPost")
    e.printStackTrace()
}
```

### Parameters
| **pageOffset** | **kotlin.Int**| Indeks pierwszej strony wyników (0 &#x3D; pierwsza strona). | [optional] [default to 0] |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. Wartość musi zawierać się w przedziale od 10 do 250. | [optional] [default to 10] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **invoiceQueryFilters** | [**InvoiceQueryFilters**](InvoiceQueryFilters.md)| Zestaw filtrów dla wyszukiwania metadanych. | [optional] |

### Return type

[**QueryInvoicesMetadataResponse**](QueryInvoicesMetadataResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

