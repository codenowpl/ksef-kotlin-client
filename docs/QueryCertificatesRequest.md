
# QueryCertificatesRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **certificateSerialNumber** | **kotlin.String** | Numer seryjny certyfikatu. Wyszukiwanie odbywa się na zasadzie dokładnego dopasowania (exact match). |  [optional] |
| **name** | **kotlin.String** | Nazwa własna certyfikatu. Wyszukiwanie jest częściowe, czyli zwracane są certyfikaty, których nazwa zawiera podany ciąg znaków (contains). |  [optional] |
| **type** | [**KsefCertificateType**](KsefCertificateType.md) | Typ certyfikatu KSeF. | Wartość | Opis | | --- | --- | | Authentication | Certyfikat używany do uwierzytelnienia w systemie. | | Offline | Certyfikat używany wyłącznie do potwierdzania autentyczności wystawcy i integralności faktury w trybie offline |  |  [optional] |
| **status** | [**CertificateListItemStatus**](CertificateListItemStatus.md) | Status certyfikatu. | Wartość | Opis | | --- | --- | | Active | Certyfikat jest aktywny i może zostać użyty do uwierzytelnienia lub realizacji operacji w trybie offline (w zależności od typu certyfikatu). | | Blocked | Certyfikat został zablokowany i nie może zostać użyty do uwierzytelnienia i realizacji operacji w trybie offline.            Status przejściowy do czasu zakończenia procesu unieważniania. | | Revoked | Certyfikat został unieważniony i nie może zostać użyty do uwierzytelnienia i realizacji operacji w trybie offline. | | Expired | Certyfikat wygasł i nie może zostać użyty do uwierzytelnienia i realizacji operacji w trybie offline. |  |  [optional] |
| **expiresAfter** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Filtruje certyfikaty, które wygasają po podanej dacie. |  [optional] |



