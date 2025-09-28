
# PersonalPermissionsQueryRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **contextIdentifier** | [**PersonalPermissionsContextIdentifier**](PersonalPermissionsContextIdentifier.md) | Identyfikator kontekstu uprawnienia (dla uprawnień nadanych podmiotom do obsługi faktur). | Type | Value | | --- | --- | | Nip | 10 cyfrowy numer NIP | |  [optional] |
| **targetIdentifier** | [**PersonalPermissionsTargetIdentifier**](PersonalPermissionsTargetIdentifier.md) | Identyfikator podmiotu docelowego (dla uprawnień pośrednich). | Type | Value | | --- | --- | | Nip | 10 cyfrowy numer NIP | | AllPartners | Identyfikator oznaczający, że uprawnienie nadane w sposób pośredni jest typu generalnego | |  [optional] |
| **permissionTypes** | [**kotlin.collections.List&lt;PersonalPermissionType&gt;**](PersonalPermissionType.md) | Możliwe uprawnienia do filtrowania. |  [optional] |
| **permissionState** | [**PermissionState**](PermissionState.md) | Stan uprawnienia.  | Type | Value | | --- | --- | | Active | Uprawnienia aktywne | | Inactive | Uprawnienia nieaktywne, nadane w sposób pośredni | |  [optional] |



