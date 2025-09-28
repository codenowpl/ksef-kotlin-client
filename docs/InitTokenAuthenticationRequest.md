
# InitTokenAuthenticationRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **challenge** | **kotlin.String** | Wygenerowany wcześniej challenge. |  |
| **contextIdentifier** | [**ContextIdentifier**](ContextIdentifier.md) | Indentyfikator kontekstu do którego następuje uwierzytelnienie. |  |
| **encryptedToken** | **kotlin.String** | Zaszyfrowany token wraz z timestampem z challenge&#39;a, w formacie &#x60;token|timestamp&#x60;. |  |
| **authorizationPolicy** | [**AuthorizationPolicy**](AuthorizationPolicy.md) | Polityka autoryzacji żądań przy każdym użyciu tokena dostępu. |  [optional] |



