
# InvoiceMetadata

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **ksefNumber** | **kotlin.String** | Numer KSeF faktury. |  |
| **invoiceNumber** | **kotlin.String** | Numer faktury nadany przez wystawcę. |  |
| **issueDate** | [**java.time.LocalDate**](java.time.LocalDate.md) | Data wystawienia faktury. |  |
| **invoicingDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data przyjęcia faktury w systemie KSeF (do dalszego przetwarzania). |  |
| **acquisitionDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data nadania numeru KSeF. |  |
| **permanentStorageDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data trwałego zapisu faktury w repozytorium systemu KSeF. |  |
| **seller** | [**InvoiceMetadataSeller**](InvoiceMetadataSeller.md) | Dane identyfikujące sprzedawcę. |  |
| **buyer** | [**InvoiceMetadataBuyer**](InvoiceMetadataBuyer.md) | Dane identyfikujące nabywcę. |  |
| **netAmount** | **kotlin.Double** | Łączna kwota netto. |  |
| **grossAmount** | **kotlin.Double** | Łączna kwota brutto. |  |
| **vatAmount** | **kotlin.Double** | Łączna kwota VAT. |  |
| **currency** | **kotlin.String** | Kod waluty. |  |
| **invoicingMode** | [**InvoicingMode**](InvoicingMode.md) | Tryb fakturowania (online/offline). |  |
| **invoiceType** | [**InvoiceType**](InvoiceType.md) | Rodzaj faktury. | Wartość | Opis | | --- | --- | | Vat | (FA) Podstawowa | | Zal | (FA) Zaliczkowa | | Kor | (FA) Korygująca | | Roz | (FA) Rozliczeniowa | | Upr | (FA) Uproszczona | | KorZal | (FA) Korygująca fakturę zaliczkową | | KorRoz | (FA) Korygująca fakturę rozliczeniową | | VatPef | (PEF) Podstawowowa | | VatPefSp | (PEF) Specjalizowana | | KorPef | (PEF) Korygująca | | VatRr | (RR) Podstawowa | | KorVatRr | (RR) Korygująca |  |  |
| **formCode** | [**FormCode**](FormCode.md) | Struktura dokumentu faktury.  Obsługiwane schematy: | SystemCode | SchemaVersion | Value | | --- | --- | --- | | FA (2) | 1-0E | FA | | FA (3) | 1-0E | FA | | FA_PEF (3) | 2-1 | FA_PEF | | FA_KOR_PEF (3) | 2-1 | FA_PEF |  |  |
| **isSelfInvoicing** | **kotlin.Boolean** | Czy faktura została wystawiona w trybie samofakturowania. |  |
| **hasAttachment** | **kotlin.Boolean** | Czy faktura posiada załącznik. |  |
| **invoiceHash** | **kotlin.String** | Skrót SHA256 faktury. |  |
| **hashOfCorrectedInvoice** | **kotlin.String** | Skrót SHA256 korygowanej faktury. |  [optional] |
| **thirdSubjects** | [**kotlin.collections.List&lt;InvoiceMetadataThirdSubject&gt;**](InvoiceMetadataThirdSubject.md) | Lista podmiotów trzecich. |  [optional] |
| **authorizedSubject** | [**InvoiceMetadataAuthorizedSubject**](InvoiceMetadataAuthorizedSubject.md) | Podmiot upoważniony. |  [optional] |



