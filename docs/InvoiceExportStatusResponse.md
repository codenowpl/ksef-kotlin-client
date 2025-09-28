
# InvoiceExportStatusResponse

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **status** | [**StatusInfo**](StatusInfo.md) | Status eksportu.  | Code | Description | Details | | --- | --- | --- | | 100 | Eksport faktur w toku | - | | 200 | Eksport faktur zakończony sukcesem | - | | 415 | Błąd odszyfrowania dostarczonego klucza  | - | | 500 | Nieznany błąd ({statusCode}) | - | |  |
| **completedDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data zakończenia przetwarzania żądania. |  [optional] |
| **&#x60;package&#x60;** | [**InvoicePackage**](InvoicePackage.md) | Dane paczki faktur przygotowanej do pobrania. |  [optional] |



