
# PersonPermission

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** | Identyfikator uprawnienia. |  |
| **authorizedIdentifier** | **kotlin.String** | Identyfikator uprawnionego. |  |
| **authorizedIdentifierType** | [**PersonPermissionsAuthorizedIdentifierType**](PersonPermissionsAuthorizedIdentifierType.md) | Typ identyfikatora uprawnionego. |  |
| **authorIdentifier** | **kotlin.String** | Identyfikator uprawniającego. |  |
| **authorIdentifierType** | [**PersonPermissionsAuthorIdentifierType**](PersonPermissionsAuthorIdentifierType.md) | Typ identyfikatora uprawniającego. |  |
| **permissionScope** | [**PersonPermissionScope**](PersonPermissionScope.md) | Uprawnienie. |  |
| **description** | **kotlin.String** | Opis uprawnienia. |  |
| **permissionState** | [**PermissionState**](PermissionState.md) | Stan uprawnienia. |  |
| **startDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data rozpoczęcia obowiązywania uprawnienia. |  |
| **canDelegate** | **kotlin.Boolean** | Informacja o możliwości dalszego nadawania uprawnienia w sposób pośredni. |  |
| **targetIdentifier** | **kotlin.String** | Identyfikator podmiotu docelowego. |  [optional] |
| **targetIdentifierType** | [**PersonPermissionsTargetIdentifierType**](PersonPermissionsTargetIdentifierType.md) | Typ identyfikatora podmiotu docelowego. |  [optional] |



