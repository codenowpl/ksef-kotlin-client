
# AuthenticationToken

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **referenceNumber** | **kotlin.String** | Numer referencyjny tokena. |  [optional] |
| **authorIdentifier** | [**SubjectIdentifier**](SubjectIdentifier.md) | Identyfikator osoby która wygenerowała token. |  [optional] |
| **contextIdentifier** | [**ContextIdentifier**](ContextIdentifier.md) | Identyfikator kontekstu, w którym został wygenerowany token i do którego daje dostęp. |  [optional] |
| **description** | **kotlin.String** | Opis tokena. |  [optional] |
| **requestedPermissions** | [**kotlin.collections.List&lt;TokenPermissionType&gt;**](TokenPermissionType.md) | Uprawnienia przypisane tokenowi. |  [optional] |
| **dateCreated** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data i czas utworzenia tokena. |  [optional] |
| **lastUseDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data ostatniego użycia tokena. |  [optional] |
| **status** | [**AuthenticationTokenStatus**](AuthenticationTokenStatus.md) | Status tokena. | Wartość | Opis | | --- | --- | | Pending | Token został utworzony ale jest jeszcze w trakcie aktywacji i nadawania uprawnień. Nie może być jeszcze wykorzystywany do uwierzytelniania. | | Active | Token jest aktywny i może być wykorzystywany do uwierzytelniania. | | Revoking | Token jest w trakcie unieważniania. Nie może już być wykorzystywany do uwierzytelniania. | | Revoked | Token został unieważniony i nie może być wykorzystywany do uwierzytelniania. | | Failed | Nie udało się aktywować tokena. Należy wygenerować nowy token, obecny nie może być wykorzystywany do uwierzytelniania. |  |  [optional] |
| **statusDetails** | **kotlin.collections.List&lt;kotlin.String&gt;** | Dodatkowe informacje na temat statusu, zwracane w przypadku błędów. |  [optional] |



