
# SessionStatusResponse

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **status** | [**StatusInfo**](StatusInfo.md) | Informacje o aktualnym statusie.              Sesja wsadowa: | Code | Description | Details | | --- | --- | --- | | 100 | Sesja wsadowa rozpoczęta | - | | 150 | Trwa przetwarzanie | - | | 200 | Sesja wsadowa przetworzona pomyślnie | - | | 405 | Błąd weryfikacji poprawności dostarczonych elementów paczki | - | | 415 | Błąd odszyfrowania dostarczonego klucza | - | | 430 | Błąd dekompresji pierwotnego archiwum | - | | 435 | Błąd odszyfrowania zaszyfrowanych części archiwum | - | | 440 | Sesja anulowana, przekroczono czas wysyłki | - | | 445 | Błąd weryfikacji, brak poprawnych faktur | - | | 500 | Nieznany błąd ({statusCode}) | - |  Sesja interaktywna: | Code | Description | Details | | --- | --- | --- | | 100 | Sesja interaktywna otwarta | - | | 170 | Sesja interaktywna zamknięta | - | | 200 | Sesja interaktywna przetworzona pomyślnie | - | | 415 | Błąd odszyfrowania dostarczonego klucza | - | | 440 | Sesja anulowana, nie przesłano faktur | - | | 445 | Błąd weryfikacji, brak poprawnych faktur | - | | * | description missing | - | |  |
| **validUntil** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Termin ważności sesji. Po jego upływie sesja zostanie automatycznie zamknięta. |  [optional] [readonly] |
| **upo** | [**UpoResponse**](UpoResponse.md) | Informacja o UPO sesyjnym, zwracana gdy sesja została zamknięta i UPO zostało wygenerowane. |  [optional] |
| **invoiceCount** | **kotlin.Int** | Liczba przyjętych faktur w ramach sesji. |  [optional] |
| **successfulInvoiceCount** | **kotlin.Int** | Liczba faktur przeprocesowanych w ramach sesji z sukcesem . |  [optional] |
| **failedInvoiceCount** | **kotlin.Int** | Liczba faktur przeprocesowanych w ramach sesji z błędem. |  [optional] |



