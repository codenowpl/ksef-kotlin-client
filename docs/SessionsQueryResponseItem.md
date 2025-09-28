
# SessionsQueryResponseItem

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **referenceNumber** | **kotlin.String** | Numer referencyjny sesji. |  |
| **status** | [**StatusInfo**](StatusInfo.md) | Status sesji. |  |
| **dateCreated** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data utowrzenia sesji. |  |
| **dateUpdated** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data ostatniej aktywności w ramach sesji. |  |
| **totalInvoiceCount** | **kotlin.Int** | Łączna liczba faktur (uwzględnia również te w trakcie przetwarzania). |  |
| **successfulInvoiceCount** | **kotlin.Int** | Liczba poprawnie przetworzonych faktur. |  |
| **failedInvoiceCount** | **kotlin.Int** | Liczba błędnie przetworzonych faktur. |  |
| **validUntil** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Termin ważności sesji. Po jego upływie sesja interaktywna zostanie automatycznie zamknięta. |  [optional] |



