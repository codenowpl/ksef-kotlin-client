
# EntityAuthorizationGrant

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **id** | **kotlin.String** | Identyfikator uprawnienia. |  |
| **authorizedEntityIdentifier** | **kotlin.String** | Identyfikator podmiotu uprawnionego. |  |
| **authorizedEntityIdentifierType** | [**EntityAuthorizationsAuthorizedEntityIdentifierType**](EntityAuthorizationsAuthorizedEntityIdentifierType.md) | Typ identyfikatora podmiotu uprawnionego. |  |
| **authorizingEntityIdentifier** | **kotlin.String** | Identyfikator podmiotu uprawniającego. |  |
| **authorizingEntityIdentifierType** | [**EntityAuthorizationsAuthorizingEntityIdentifierType**](EntityAuthorizationsAuthorizingEntityIdentifierType.md) | Typ identyfikatora podmiotu uprawniającego. |  |
| **authorizationScope** | [**InvoicePermissionType**](InvoicePermissionType.md) | Uprawnienie. |  |
| **description** | **kotlin.String** | Opis uprawnienia. |  |
| **startDate** | [**java.time.LocalDateTime**](java.time.LocalDateTime.md) | Data rozpoczęcia obowiązywania uprawnienia. |  |
| **authorIdentifier** | **kotlin.String** | Identyfikator osoby nadającej uprawnienie. |  [optional] |
| **authorIdentifierType** | [**EntityAuthorizationsAuthorIdentifierType**](EntityAuthorizationsAuthorIdentifierType.md) | Typ identyfikatora osoby nadającej uprawnienie. |  [optional] |



