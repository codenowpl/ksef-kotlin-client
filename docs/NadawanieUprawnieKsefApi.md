# NadawanieUprawnieKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2PermissionsAuthorizationsGrantsPost**](NadawanieUprawnieKsefApi.md#apiV2PermissionsAuthorizationsGrantsPost) | **POST** /api/v2/permissions/authorizations/grants | Nadanie uprawnień podmiotowych |
| [**apiV2PermissionsEntitiesGrantsPost**](NadawanieUprawnieKsefApi.md#apiV2PermissionsEntitiesGrantsPost) | **POST** /api/v2/permissions/entities/grants | Nadanie podmiotom uprawnień do obsługi faktur |
| [**apiV2PermissionsEuEntitiesAdministrationGrantsPost**](NadawanieUprawnieKsefApi.md#apiV2PermissionsEuEntitiesAdministrationGrantsPost) | **POST** /api/v2/permissions/eu-entities/administration/grants | Nadanie uprawnień administratora podmiotu unijnego |
| [**apiV2PermissionsEuEntitiesGrantsPost**](NadawanieUprawnieKsefApi.md#apiV2PermissionsEuEntitiesGrantsPost) | **POST** /api/v2/permissions/eu-entities/grants | Nadanie uprawnień reprezentanta podmiotu unijnego |
| [**apiV2PermissionsIndirectGrantsPost**](NadawanieUprawnieKsefApi.md#apiV2PermissionsIndirectGrantsPost) | **POST** /api/v2/permissions/indirect/grants | Nadanie uprawnień w sposób pośredni |
| [**apiV2PermissionsPersonsGrantsPost**](NadawanieUprawnieKsefApi.md#apiV2PermissionsPersonsGrantsPost) | **POST** /api/v2/permissions/persons/grants | Nadanie osobom fizycznym uprawnień do pracy w KSeF |
| [**apiV2PermissionsSubunitsGrantsPost**](NadawanieUprawnieKsefApi.md#apiV2PermissionsSubunitsGrantsPost) | **POST** /api/v2/permissions/subunits/grants | Nadanie uprawnień administratora podmiotu podrzędnego |


<a id="apiV2PermissionsAuthorizationsGrantsPost"></a>
# **apiV2PermissionsAuthorizationsGrantsPost**
> PermissionsOperationResponse apiV2PermissionsAuthorizationsGrantsPost(entityAuthorizationPermissionsGrantRequest)

Nadanie uprawnień podmiotowych

Rozpoczyna asynchroniczną operację nadawania uprawnień podmiotowych.  &gt; Więcej informacji: &gt; - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadanie-uprawnie%C5%84-podmiotowych)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = NadawanieUprawnieKsefApi()
val entityAuthorizationPermissionsGrantRequest : EntityAuthorizationPermissionsGrantRequest = {"subjectIdentifier":{"type":"Nip","value":"7762811692"},"permission":"SelfInvoicing","description":"Uprawnienia do samofakturowania"} // EntityAuthorizationPermissionsGrantRequest | 
try {
    val result : PermissionsOperationResponse = apiInstance.apiV2PermissionsAuthorizationsGrantsPost(entityAuthorizationPermissionsGrantRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsAuthorizationsGrantsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsAuthorizationsGrantsPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **entityAuthorizationPermissionsGrantRequest** | [**EntityAuthorizationPermissionsGrantRequest**](EntityAuthorizationPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**PermissionsOperationResponse**](PermissionsOperationResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2PermissionsEntitiesGrantsPost"></a>
# **apiV2PermissionsEntitiesGrantsPost**
> PermissionsOperationResponse apiV2PermissionsEntitiesGrantsPost(entityPermissionsGrantRequest)

Nadanie podmiotom uprawnień do obsługi faktur

Rozpoczyna asynchroniczną operację nadawania podmiotom uprawnień do obsługi faktur.  &gt; Więcej informacji: &gt; - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadanie-podmiotom-uprawnie%C5%84-do-obs%C5%82ugi-faktur)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = NadawanieUprawnieKsefApi()
val entityPermissionsGrantRequest : EntityPermissionsGrantRequest = {"subjectIdentifier":{"type":"Nip","value":"7762811692"},"permissions":[{"type":"InvoiceRead","canDelegate":true},{"type":"InvoiceWrite","canDelegate":true}],"description":"Uprawnienia do odczytu i wysyłania faktur z możliwością nadania ich pośrednio"} // EntityPermissionsGrantRequest | 
try {
    val result : PermissionsOperationResponse = apiInstance.apiV2PermissionsEntitiesGrantsPost(entityPermissionsGrantRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsEntitiesGrantsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsEntitiesGrantsPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **entityPermissionsGrantRequest** | [**EntityPermissionsGrantRequest**](EntityPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**PermissionsOperationResponse**](PermissionsOperationResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2PermissionsEuEntitiesAdministrationGrantsPost"></a>
# **apiV2PermissionsEuEntitiesAdministrationGrantsPost**
> PermissionsOperationResponse apiV2PermissionsEuEntitiesAdministrationGrantsPost(euEntityAdministrationPermissionsGrantRequest)

Nadanie uprawnień administratora podmiotu unijnego

Rozpoczyna asynchroniczną operację nadawania uprawnień administratora podmiotu unijnego.  &gt; Więcej informacji: &gt; - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadanie-uprawnie%C5%84-administratora-podmiotu-unijnego)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = NadawanieUprawnieKsefApi()
val euEntityAdministrationPermissionsGrantRequest : EuEntityAdministrationPermissionsGrantRequest = {"subjectIdentifier":{"type":"Fingerprint","value":"CEB3643BAC2C111ADDE971BDA5A80163441867D65389FC0BC0DFF8B4C1CD4E59"},"contextIdentifier":{"type":"NipVatUe","value":"7762811692-DE123456789012"},"description":"Administrator podmiotu unijnego DE123456789012"} // EuEntityAdministrationPermissionsGrantRequest | 
try {
    val result : PermissionsOperationResponse = apiInstance.apiV2PermissionsEuEntitiesAdministrationGrantsPost(euEntityAdministrationPermissionsGrantRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsEuEntitiesAdministrationGrantsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsEuEntitiesAdministrationGrantsPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **euEntityAdministrationPermissionsGrantRequest** | [**EuEntityAdministrationPermissionsGrantRequest**](EuEntityAdministrationPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**PermissionsOperationResponse**](PermissionsOperationResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2PermissionsEuEntitiesGrantsPost"></a>
# **apiV2PermissionsEuEntitiesGrantsPost**
> PermissionsOperationResponse apiV2PermissionsEuEntitiesGrantsPost(euEntityPermissionsGrantRequest)

Nadanie uprawnień reprezentanta podmiotu unijnego

Rozpoczyna asynchroniczną operację nadawania uprawnień reprezentanta podmiotu unijnego.  &gt; Więcej informacji: &gt; - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadanie-uprawnie%C5%84-reprezentanta-podmiotu-unijnego)  Wymagane uprawnienia: &#x60;VatUeManage&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = NadawanieUprawnieKsefApi()
val euEntityPermissionsGrantRequest : EuEntityPermissionsGrantRequest = {"subjectIdentifier":{"type":"Fingerprint","value":"CEB3643BAC2C111ADDE971BDA5A80163441867D65389FC0BC0DFF8B4C1CD4E59"},"permissions":["InvoiceRead","InvoiceWrite"],"description":"Reprezentant podmiotu unijnego"} // EuEntityPermissionsGrantRequest | 
try {
    val result : PermissionsOperationResponse = apiInstance.apiV2PermissionsEuEntitiesGrantsPost(euEntityPermissionsGrantRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsEuEntitiesGrantsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsEuEntitiesGrantsPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **euEntityPermissionsGrantRequest** | [**EuEntityPermissionsGrantRequest**](EuEntityPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**PermissionsOperationResponse**](PermissionsOperationResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2PermissionsIndirectGrantsPost"></a>
# **apiV2PermissionsIndirectGrantsPost**
> PermissionsOperationResponse apiV2PermissionsIndirectGrantsPost(indirectPermissionsGrantRequest)

Nadanie uprawnień w sposób pośredni

Rozpoczyna asynchroniczną operację nadawania uprawnień w sposób pośredni.  &gt; Więcej informacji: &gt; - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadanie-uprawnie%C5%84-w-spos%C3%B3b-po%C5%9Bredni)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = NadawanieUprawnieKsefApi()
val indirectPermissionsGrantRequest : IndirectPermissionsGrantRequest = {"subjectIdentifier":{"type":"Pesel","value":"15062788702"},"permissions":["InvoiceWrite","InvoiceRead"],"description":"Uprawnienia generalne do odczytu i wysyłania faktur, nadane w sposób pośredni"} // IndirectPermissionsGrantRequest | 
try {
    val result : PermissionsOperationResponse = apiInstance.apiV2PermissionsIndirectGrantsPost(indirectPermissionsGrantRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsIndirectGrantsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsIndirectGrantsPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **indirectPermissionsGrantRequest** | [**IndirectPermissionsGrantRequest**](IndirectPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**PermissionsOperationResponse**](PermissionsOperationResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2PermissionsPersonsGrantsPost"></a>
# **apiV2PermissionsPersonsGrantsPost**
> PermissionsOperationResponse apiV2PermissionsPersonsGrantsPost(personPermissionsGrantRequest)

Nadanie osobom fizycznym uprawnień do pracy w KSeF

Rozpoczyna asynchroniczną operację nadawania osobom fizycznym uprawnień do pracy w KSeF.  &gt; Więcej informacji: &gt; - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadawanie-uprawnie%C5%84-osobom-fizycznym-do-pracy-w-ksef)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = NadawanieUprawnieKsefApi()
val personPermissionsGrantRequest : PersonPermissionsGrantRequest = {"subjectIdentifier":{"type":"Pesel","value":"15062788702"},"permissions":["InvoiceRead","InvoiceWrite"],"description":"Uprawnienia do odczytu i wysyłania faktur"} // PersonPermissionsGrantRequest | 
try {
    val result : PermissionsOperationResponse = apiInstance.apiV2PermissionsPersonsGrantsPost(personPermissionsGrantRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsPersonsGrantsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsPersonsGrantsPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **personPermissionsGrantRequest** | [**PersonPermissionsGrantRequest**](PersonPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**PermissionsOperationResponse**](PermissionsOperationResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2PermissionsSubunitsGrantsPost"></a>
# **apiV2PermissionsSubunitsGrantsPost**
> PermissionsOperationResponse apiV2PermissionsSubunitsGrantsPost(subunitPermissionsGrantRequest)

Nadanie uprawnień administratora podmiotu podrzędnego

Rozpoczyna asynchroniczną operację nadawania uprawnień administratora podmiotu podrzędnego.  &gt; Więcej informacji: &gt; - [Nadawanie uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#nadanie-uprawnie%C5%84-administratora-podmiotu-podrz%C4%99dnego)  Wymagane uprawnienia: &#x60;SubunitManage&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = NadawanieUprawnieKsefApi()
val subunitPermissionsGrantRequest : SubunitPermissionsGrantRequest = {"subjectIdentifier":{"type":"Pesel","value":"15062788702"},"contextIdentifier":{"type":"InternalId","value":"7762811692-11111"},"description":"Administrator jednostki podrzędnej"} // SubunitPermissionsGrantRequest | 
try {
    val result : PermissionsOperationResponse = apiInstance.apiV2PermissionsSubunitsGrantsPost(subunitPermissionsGrantRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsSubunitsGrantsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling NadawanieUprawnieKsefApi#apiV2PermissionsSubunitsGrantsPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subunitPermissionsGrantRequest** | [**SubunitPermissionsGrantRequest**](SubunitPermissionsGrantRequest.md)|  | [optional] |

### Return type

[**PermissionsOperationResponse**](PermissionsOperationResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

