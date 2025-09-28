
# CertificateEnrollmentStatusResponse

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **requestDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data złożenia wniosku certyfikacyjnego. |  |
| **status** | [**StatusInfo**](StatusInfo.md) | Informacje o aktualnym statusie. | Code | Description | Details | | --- | --- | --- | | 100 | Wniosek przyjęty do realizacji | - | | 200 | Wniosek obsłużony (certyfikat wygenerowany) | - | | 400 | Wniosek odrzucony | Klucz publiczny został już certyfikowany przez inny podmiot. | | 400 | Wniosek odrzucony | Osiągnięto dopuszczalny limit posiadanych certyfikatów. | | 500 | Nieznany błąd | - | |  |
| **certificateSerialNumber** | **kotlin.String** | Numer seryjny wygenerowanego certyfikatu (w formacie szesnastkowym).  Zwracany w przypadku prawidłowego przeprocesowania wniosku certyfikacyjnego. |  [optional] |



