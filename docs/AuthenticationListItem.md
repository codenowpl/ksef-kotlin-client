
# AuthenticationListItem

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **startDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data rozpoczęcia operacji uwierzytelnienia. |  |
| **authenticationMethod** | [**AuthenticationMethod**](AuthenticationMethod.md) | Użyta metoda uwierzytelnienia. | Wartość | Opis | | --- | --- | | Token | Token KSeF. | | TrustedProfile | Profil Zaufany. | | InternalCertificate | Certyfikat KSeF. | | QualifiedSignature | Podpis kwalifikowany. | | QualifiedSeal | Pieczęć kwalifikowana. | | PersonalSignature | Podpis osobisty. | | PeppolSignature | Podpis dostawcy uslug Peppol. |  |  |
| **status** | [**StatusInfo**](StatusInfo.md) | Informacje o aktualnym statusie. | Code | Description | Details | | --- | --- | --- | | 100 | Uwierzytelnianie w toku | - | | 200 | Uwierzytelnianie zakończone sukcesem | - | | 415 | Uwierzytelnianie zakończone niepowodzeniem | Brak przypisanych uprawnień | | 425 | Uwierzytelnienie unieważnione  | Uwierzytelnienie i powiązane refresh tokeny zostały unieważnione przez użytkownika | | 450 | Uwierzytelnianie zakończone niepowodzeniem z powodu błędnego tokenu | Nieprawidłowy token | | 450 | Uwierzytelnianie zakończone niepowodzeniem z powodu błędnego tokenu | Nieprawidłowy czas tokena | | 450 | Uwierzytelnianie zakończone niepowodzeniem z powodu błędnego tokenu | Token unieważniony | | 450 | Uwierzytelnianie zakończone niepowodzeniem z powodu błędnego tokenu | Token nieaktywny | | 460 | Uwierzytelnianie zakończone niepowodzeniem z powodu błędu certyfikatu | Nieważny certyfikat | | 460 | Uwierzytelnianie zakończone niepowodzeniem z powodu błędu certyfikatu | Błąd weryfikacji łańcucha certyfikatów | | 460 | Uwierzytelnianie zakończone niepowodzeniem z powodu błędu certyfikatu | Niezaufany łańcuch certyfikatów | | 460 | Uwierzytelnianie zakończone niepowodzeniem z powodu błędu certyfikatu | Certyfikat odwołany | | 460 | Uwierzytelnianie zakończone niepowodzeniem z powodu błędu certyfikatu | Niepoprawny certyfikat | | 500 | Nieznany błąd | - | |  |
| **referenceNumber** | **kotlin.String** | Numer referencyjny operacji uwierzytelnienia. |  |
| **isTokenRedeemed** | **kotlin.Boolean** | Czy został już wydany refresh token powiązany z danym uwierzytelnieniem. |  [optional] |
| **lastTokenRefreshDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data ostatniego odświeżenia tokena. |  [optional] |
| **refreshTokenValidUntil** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Termin ważności refresh tokena (o ile nie zostanie wcześniej unieważniony). |  [optional] |
| **isCurrent** | **kotlin.Boolean** | Czy sesja jest powiązana z aktualnie używanym tokenem. |  [optional] [readonly] |



