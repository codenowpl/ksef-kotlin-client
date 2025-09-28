
# InvoiceQueryDateRange

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **dateType** | [**InvoiceQueryDateType**](InvoiceQueryDateType.md) | Typ daty, według której ma być zastosowany zakres. | Wartość | Opis | | --- | --- | | Issue | Data wystawienia faktury. | | Invoicing | Data przyjęcia faktury w systemie KSeF (do dalszego przetwarzania). | | PermanentStorage | Data trwałego zapisu faktury w repozytorium systemu KSeF. |  |  |
| **from** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data początkowa zakresu. |  |
| **to** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data końcowa zakresu. Jeśli nie zostanie podana, przyjmowana jest bieżąca data i czas w UTC. |  [optional] |



