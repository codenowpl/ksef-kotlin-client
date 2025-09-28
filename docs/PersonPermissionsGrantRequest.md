
# PersonPermissionsGrantRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **subjectIdentifier** | [**PersonPermissionsSubjectIdentifier**](PersonPermissionsSubjectIdentifier.md) | Identyfikator osoby fizycznej. | Type | Value | | --- | --- | | Nip | 10 cyfrowy numer NIP | | Pesel | 11 cyfrowy numer PESEL | | Fingerprint | Odcisk palca certyfikatu | |  |
| **permissions** | [**kotlin.collections.List&lt;PersonPermissionType&gt;**](PersonPermissionType.md) | Lista nadawanych uprawnień. Każda wartość może wystąpić tylko raz. |  |
| **description** | **kotlin.String** | Opis nadawanych uprawnień. |  |



