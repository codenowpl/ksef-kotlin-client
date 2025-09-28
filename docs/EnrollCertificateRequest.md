
# EnrollCertificateRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **certificateName** | **kotlin.String** | Nazwa własna certyfikatu. |  |
| **certificateType** | [**KsefCertificateType**](KsefCertificateType.md) | Typ certyfikatu. | Wartość | Opis | | --- | --- | | Authentication | Certyfikat używany do uwierzytelnienia w systemie. | | Offline | Certyfikat używany wyłącznie do potwierdzania autentyczności wystawcy i integralności faktury w trybie offline |  |  |
| **csr** | **kotlin.ByteArray** | Wniosek certyfikacyjny PKCS#10 (CSR) w formacie DER zakodowany w Base64. |  |
| **validFrom** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data rozpoczęcia ważności certyfikatu. Jeśli nie zostanie podana, certyfikat będzie ważny od momentu jego wystawienia. |  [optional] |



