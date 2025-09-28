
# SessionInvoiceStatusResponse

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **ordinalNumber** | **kotlin.Int** | Numer sekwencyjny faktury w ramach sesji. |  |
| **invoicingDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data przyjęcia faktury w systemie KSeF (do dalszego przetwarzania). |  |
| **status** | [**StatusInfo**](StatusInfo.md) | Status faktury.  | Code | Description | Details | | --- | --- | --- | | 100 | Faktura przyjęta do dalszego przetwarzania | - | | 150 | Trwa przetwarzanie | - | | 200 | Sukces | - | | 405 | Przetwarzanie anulowane | - | | 410 | Nieprawidłowy zakres uprawnień | - | | 415 | Brak możliwości wysyłania faktury z załącznikiem | - | | 430 | Błąd weryfikacji pliku faktury | - | | 435 | Błąd odszyfrowania pliku | - | | 440 | Duplikat faktury | - | | 450 | Błąd weryfikacji semantyki dokumentu faktury | - | | 500 | Nieznany błąd ({statusCode}) | - | |  |
| **invoiceNumber** | **kotlin.String** | Numer faktury. |  [optional] |
| **ksefNumber** | **kotlin.String** | Numer KSeF. |  [optional] |
| **referenceNumber** | **kotlin.String** | Numer referencyjny faktury. |  [optional] |
| **invoiceHash** | **kotlin.String** | Skrót SHA256 faktury, zakodowany w formacie Base64. |  [optional] |
| **invoiceFileName** | **kotlin.String** | Nazwa pliku faktury (zwracana dla faktur wysyłanych wsadowo). |  [optional] |
| **acquisitionDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data nadania numeru KSeF. |  [optional] |
| **permanentStorageDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data trwałego zapisu faktury w repozytorium systemu KSeF. Od tego momentu faktura jest dostępna do pobrania. |  [optional] |
| **upoDownloadUrl** | [**java.net.URI**](java.net.URI.md) | Adres do pobrania UPO. |  [optional] |



