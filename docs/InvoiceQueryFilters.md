
# InvoiceQueryFilters

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **subjectType** | [**InvoiceQuerySubjectType**](InvoiceQuerySubjectType.md) | Typ podmiotu, którego dotyczą kryteria filtrowania metadanych faktur. Określa kontekst, w jakim przeszukiwane są dane. | Wartość | Opis | | --- | --- | | Subject1 | Podmiot 1 | | Subject2 | Podmiot 2 | | Subject3 | Podmiot 3 | | SubjectAuthorized | Podmiot upoważniony |  |  |
| **dateRange** | [**InvoiceQueryDateRange**](InvoiceQueryDateRange.md) | Typ i zakres dat, według którego mają być filtrowane faktury. Dozwolony maksymalny okres wynosi 2 lata. |  |
| **ksefNumber** | **kotlin.String** | Numer KSeF faktury. |  [optional] |
| **invoiceNumber** | **kotlin.String** | Numer faktury nadany przez wystawcę. |  [optional] |
| **amount** | [**InvoiceQueryAmount**](InvoiceQueryAmount.md) | Filtr kwotowy – brutto, netto lub VAT (z wartością). |  [optional] |
| **seller** | [**InvoiceQuerySeller**](InvoiceQuerySeller.md) | Dane sprzedawcy. |  [optional] |
| **buyer** | [**InvoiceQueryBuyer**](InvoiceQueryBuyer.md) | Dane nabywcy. |  [optional] |
| **currencyCodes** | [**kotlin.collections.List&lt;CurrencyCode&gt;**](CurrencyCode.md) | Kody walut. |  [optional] |
| **invoicingMode** | [**InvoicingMode**](InvoicingMode.md) | Tryb wystawienia faktury: online lub offline. |  [optional] |
| **isSelfInvoicing** | **kotlin.Boolean** | Czy faktura została wystawiona w trybie samofakturowania. |  [optional] |
| **formType** | [**InvoiceQueryFormType**](InvoiceQueryFormType.md) | Typ dokumentu. | Wartość | Opis | | --- | --- | | FA | Faktura VAT | | PEF | Faktura PEF | | RR | Faktura RR |  |  [optional] |
| **invoiceTypes** | [**kotlin.collections.List&lt;InvoiceType&gt;**](InvoiceType.md) | Rodzaje faktur. | Wartość | Opis | | --- | --- | | Vat | (FA) Podstawowa | | Zal | (FA) Zaliczkowa | | Kor | (FA) Korygująca | | Roz | (FA) Rozliczeniowa | | Upr | (FA) Uproszczona | | KorZal | (FA) Korygująca fakturę zaliczkową | | KorRoz | (FA) Korygująca fakturę rozliczeniową | | VatPef | (PEF) Podstawowowa | | VatPefSp | (PEF) Specjalizowana | | KorPef | (PEF) Korygująca | | VatRr | (RR) Podstawowa | | KorVatRr | (RR) Korygująca |  |  [optional] |
| **hasAttachment** | **kotlin.Boolean** | Czy faktura ma załącznik. |  [optional] |



