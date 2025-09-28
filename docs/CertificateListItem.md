
# CertificateListItem

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **certificateSerialNumber** | **kotlin.String** | Numer seryjny certyfikatu (w formacie szesnastkowym). |  |
| **name** | **kotlin.String** | Nazwa własna certyfikatu. |  |
| **type** | [**KsefCertificateType**](KsefCertificateType.md) | Typ certyfikatu. | Wartość | Opis | | --- | --- | | Authentication | Certyfikat używany do uwierzytelnienia w systemie. | | Offline | Certyfikat używany wyłącznie do potwierdzania autentyczności wystawcy i integralności faktury w trybie offline |  |  |
| **commonName** | **kotlin.String** | Nazwa powszechna (CN) podmiotu, dla którego wystawiono certyfikat. |  |
| **status** | [**CertificateListItemStatus**](CertificateListItemStatus.md) | Status certyfikatu. | Wartość | Opis | | --- | --- | | Active | Certyfikat jest aktywny i może zostać użyty do uwierzytelnienia lub realizacji operacji w trybie offline (w zależności od typu certyfikatu). | | Blocked | Certyfikat został zablokowany i nie może zostać użyty do uwierzytelnienia i realizacji operacji w trybie offline.            Status przejściowy do czasu zakończenia procesu unieważniania. | | Revoked | Certyfikat został unieważniony i nie może zostać użyty do uwierzytelnienia i realizacji operacji w trybie offline. | | Expired | Certyfikat wygasł i nie może zostać użyty do uwierzytelnienia i realizacji operacji w trybie offline. |  |  |
| **subjectIdentifier** | **kotlin.String** | Identyfikator podmiotu, dla którego wystawiono certyfikat. |  |
| **subjectIdentifierType** | **kotlin.String** | Typ identyfikatora podmiotu, dla którego wystawiono certyfikat. |  |
| **validFrom** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data rozpoczęcia ważności certyfikatu. |  |
| **validTo** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data wygaśnięcia certyfikatu. |  |
| **lastUseDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data ostatniego użycia certyfikatu. |  [optional] |



