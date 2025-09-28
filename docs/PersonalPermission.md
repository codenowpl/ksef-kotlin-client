
# PersonalPermission

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** | Identyfikator uprawnienia. |  |
| **permissionScope** | [**PersonalPermissionScope**](PersonalPermissionScope.md) | Uprawnienie. |  |
| **description** | **kotlin.String** | Opis uprawnienia. |  |
| **permissionState** | [**PermissionState**](PermissionState.md) | Stan uprawnienia. |  |
| **startDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data rozpoczęcia obowiązywania uprawnienia. |  |
| **canDelegate** | **kotlin.Boolean** | Informacja o możliwości dalszego nadawania uprawnienia w sposób pośredni. |  |
| **contextIdentifier** | **kotlin.String** | Identyfikator kontekstu uprawnienia, jeśli inny niż kontekst uwierzytelnienia. |  [optional] |
| **contextIdentifierType** | [**PersonalPermissionsContextIdentifierType**](PersonalPermissionsContextIdentifierType.md) | Typ identyfikatora kontekstu uprawnienia. |  [optional] |
| **authorizedIdentifier** | **kotlin.String** | Identyfikator podmiotu uprawnionego, jeśli inny niż podmiot uwierzytelnienia. |  [optional] |
| **authorizedIdentifierType** | [**PersonalPermissionsAuthorizedIdentifierType**](PersonalPermissionsAuthorizedIdentifierType.md) | Typ identyfikatora podmiotu uprawnionego. |  [optional] |
| **targetIdentifier** | **kotlin.String** | Identyfikator podmiotu docelowego. |  [optional] |
| **targetIdentifierType** | [**PersonalPermissionsTargetIdentifierType**](PersonalPermissionsTargetIdentifierType.md) | Typ identyfikatora podmiotu docelowego. |  [optional] |



