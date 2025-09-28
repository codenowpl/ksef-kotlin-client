
# PublicKeyCertificate

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **certificate** | **kotlin.String** | Certyfikat klucza publicznego w formacie DER zakodowany w Base64. |  |
| **validFrom** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data początku obowiązywania certyfikatu. |  |
| **validTo** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data końca obowiązywania certyfikatu. |  |
| **usage** | [**kotlin.collections.List&lt;PublicKeyCertificateUsage&gt;**](PublicKeyCertificateUsage.md) | Operacje do których może być używany certyfikat. | Wartość | Opis | | --- | --- | | KsefTokenEncryption | Szyfrowanie tokenów KSeF przesyłanych w trakcie procesu uwierzytelniania. | | SymmetricKeyEncryption | Szyfrowanie klucza symetrycznego wykorzystywanego do szyfrowania przesyłanych faktur. |  |  |



