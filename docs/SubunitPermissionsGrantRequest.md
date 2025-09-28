
# SubunitPermissionsGrantRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **subjectIdentifier** | [**SubunitPermissionsSubjectIdentifier**](SubunitPermissionsSubjectIdentifier.md) | Identyfikator podmiotu lub osoby fizycznej. | Type | Value | | --- | --- | | Nip | 10 cyfrowy numer NIP | | Pesel | 11 cyfrowy numer PESEL | | Fingerprint | Odcisk palca certyfikatu | |  |
| **contextIdentifier** | [**SubunitPermissionsContextIdentifier**](SubunitPermissionsContextIdentifier.md) | Identyfikator podmiotu podrzędnego. | Type | Value | | --- | --- | | Nip | 10 cyfrowy numer NIP | | InternalId | Dwuczłonowy identyfikator składający się z numeru NIP i 5 cyfr: &#x60;{nip}-{5_cyfr}&#x60; | |  |
| **description** | **kotlin.String** | Opis nadawanych uprawnień. |  |



