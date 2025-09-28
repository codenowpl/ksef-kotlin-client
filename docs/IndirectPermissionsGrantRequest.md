
# IndirectPermissionsGrantRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **subjectIdentifier** | [**IndirectPermissionsSubjectIdentifier**](IndirectPermissionsSubjectIdentifier.md) | Identyfikator osoby fizycznej. | Type | Value | | --- | --- | | Nip | 10 cyfrowy numer NIP | | Pesel | 11 cyfrowy numer PESEL | | Fingerprint | Odcisk palca certyfikatu | |  |
| **permissions** | [**kotlin.collections.List&lt;IndirectPermissionType&gt;**](IndirectPermissionType.md) | Lista nadawanych uprawnień. Każda wartość może wystąpić tylko raz. |  |
| **description** | **kotlin.String** | Opis nadawanych uprawnień. |  |
| **targetIdentifier** | [**IndirectPermissionsTargetIdentifier**](IndirectPermissionsTargetIdentifier.md) | Identyfikator podmiotu, w którego kontekście chcemy pośrednio nadać uprawnienia. W przypadku nadawania uprawnienia generalnego, pole to powinno mieć wartość null. | Type | Value | | --- | --- | | Nip | 10 cyfrowy numer NIP | | AllPartners | Identyfikator oznaczający, że uprawnienie nadane w sposób pośredni jest typu generalnego | |  [optional] |



