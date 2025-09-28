
# InvoicePackage

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **invoiceCount** | **kotlin.Long** | Łączna liczba faktur w paczce. Maksymalna liczba faktur w paczce to 10 000. |  |
| **propertySize** | **kotlin.Long** | Rozmiar paczki w bajtach. Maksymalny rozmiar paczki to 1 GiB (1 073 741 824 bajtów). |  |
| **parts** | [**kotlin.collections.List&lt;InvoicePackagePart&gt;**](InvoicePackagePart.md) | Lista dostępnych części paczki do pobrania. Każda część jest zaszyfrowana algorytmem AES-256-CBC z dopełnieniem PKCS#7, przy użyciu klucza symetrycznego przekazanego podczas inicjowania eksportu. Wyniki sortowane są rosnąco według typu daty przekazanej w &#x60;DateRange&#x60; przy inicjalizacji. |  |
| **isTruncated** | **kotlin.Boolean** | Określa, czy wynik eksportu został ucięty z powodu przekroczenia limitu liczby faktur lub wielkości paczki. |  |
| **lastIssueDate** | [**java.time.LocalDate**](java.time.LocalDate.md) | Data wystawienia ostatniej faktury ujętej w paczce. Pole występuje wyłącznie wtedy, gdy paczka została ucięta i eksport był filtrowany po typie daty &#x60;Issue&#x60;. |  [optional] |
| **lastInvoicingDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data przyjęcia ostatniej faktury ujętej w paczce. Pole występuje wyłącznie wtedy, gdy paczka została ucięta i eksport był filtrowany po typie daty &#x60;Invoicing&#x60;. |  [optional] |
| **lastPermanentStorageDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data trwałego zapisu ostatniej faktury ujętej w paczce. Pole występuje wyłącznie wtedy, gdy paczka została ucięta i eksport był filtrowany po typie daty &#x60;PermanentStorage&#x60;. |  [optional] |



