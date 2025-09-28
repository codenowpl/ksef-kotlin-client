
# EntityAuthorizationPermissionsQueryRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **queryType** | [**QueryType**](QueryType.md) | Typ zapytania. | Type | Value | | --- | --- | | Granted | Uprawnienia nadane innym podmiotom | | Received | Uprawnienia otrzymane od innych podmiotów | |  |
| **authorizingIdentifier** | [**EntityAuthorizationsAuthorizingEntityIdentifier**](EntityAuthorizationsAuthorizingEntityIdentifier.md) | Identyfikator podmiotu uprawniającego. | Type | Value | | --- | --- | | Nip | 10 cyfrowy numer NIP | |  [optional] |
| **authorizedIdentifier** | [**EntityAuthorizationsAuthorizedEntityIdentifier**](EntityAuthorizationsAuthorizedEntityIdentifier.md) | Identyfikator podmiotu uprawnionego. | Type | Value | | --- | --- | | Nip | 10 cyfrowy numer NIP | | PeppolId | Identyfikator dostawcy usług Peppol | |  [optional] |
| **permissionTypes** | [**kotlin.collections.List&lt;InvoicePermissionType&gt;**](InvoicePermissionType.md) | Możliwe uprawnienia do filtrowania. |  [optional] |



