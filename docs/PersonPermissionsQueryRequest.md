
# PersonPermissionsQueryRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **queryType** | [**PersonPermissionsQueryType**](PersonPermissionsQueryType.md) | Typ zapytania. | Type | Value | | --- | --- | | PermissionsInCurrentContext | Uprawnienia posiadane w aktualnym kontekście | | PermissionsGrantedInCurrentContext | Uprawnienia nadane w aktualnym kontekście | |  |
| **authorIdentifier** | [**PersonPermissionsAuthorIdentifier**](PersonPermissionsAuthorIdentifier.md) | Identyfikator osoby lub podmiotu nadającego uprawnienie. | Type | Value | | --- | --- | | Nip | 10 cyfrowy numer NIP | | Pesel | 11 cyfrowy numer PESEL | | Fingerprint | Odcisk palca certyfikatu | | System | Identyfikator systemowy KSeF | |  [optional] |
| **authorizedIdentifier** | [**PersonPermissionsAuthorizedIdentifier**](PersonPermissionsAuthorizedIdentifier.md) | Identyfikator osoby lub podmiotu uprawnionego. | Type | Value | | --- | --- | | Nip | 10 cyfrowy numer NIP | | Pesel | 11 cyfrowy numer PESEL | | Fingerprint | Odcisk palca certyfikatu | |  [optional] |
| **targetIdentifier** | [**PersonPermissionsTargetIdentifier**](PersonPermissionsTargetIdentifier.md) | Identyfikator podmiotu docelowego (dla uprawnień pośrednich). | Type | Value | | --- | --- | | Nip | 10 cyfrowy numer NIP | | AllPartners | Identyfikator oznaczający, że uprawnienie nadane w sposób pośredni jest typu generalnego | |  [optional] |
| **permissionTypes** | [**kotlin.collections.List&lt;PersonPermissionType&gt;**](PersonPermissionType.md) | Możliwe uprawnienia do filtrowania. |  [optional] |
| **permissionState** | [**PermissionState**](PermissionState.md) | Stan uprawnienia.  | Type | Value | | --- | --- | | Active | Uprawnienia aktywne | | Inactive | Uprawnienia nieaktywne, nadane w sposób poœredni | |  [optional] |



