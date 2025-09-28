
# InvoicePackagePart

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **ordinalNumber** | **kotlin.Int** | Numer sekwencyjny pliku części paczki. |  |
| **partName** | **kotlin.String** | Nazwa pliku części paczki. |  |
| **method** | **kotlin.String** | Metoda HTTP, której należy użyć przy pobieraniu pliku. |  |
| **url** | [**java.net.URI**](java.net.URI.md) | Adres URL, pod który należy wysłać żądanie pobrania. |  |
| **partSize** | **kotlin.Long** | Rozmiar części paczki w bajtach. Maksymalny rozmiar części to 50MiB (52 428 800 bajtów). |  |
| **partHash** | **kotlin.String** | Skrót SHA256 pliku części paczki, zakodowany w formacie Base64. |  |
| **encryptedPartSize** | **kotlin.Long** | Rozmiar zaszyfrowanej części paczki w bajtach. |  |
| **encryptedPartHash** | **kotlin.String** | Skrót SHA256 zaszyfrowanej części paczki, zakodowany w formacie Base64. |  |
| **expirationDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Moment wygaśnięcia linku do pobrania części. |  |



