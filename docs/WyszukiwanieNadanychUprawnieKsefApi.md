# WyszukiwanieNadanychUprawnieKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2PermissionsQueryAuthorizationsGrantsPost**](WyszukiwanieNadanychUprawnieKsefApi.md#apiV2PermissionsQueryAuthorizationsGrantsPost) | **POST** /api/v2/permissions/query/authorizations/grants | Pobranie listy uprawnień podmiotowych do obsługi faktur |
| [**apiV2PermissionsQueryEntitiesRolesGet**](WyszukiwanieNadanychUprawnieKsefApi.md#apiV2PermissionsQueryEntitiesRolesGet) | **GET** /api/v2/permissions/query/entities/roles | Pobranie listy ról podmiotu |
| [**apiV2PermissionsQueryEuEntitiesGrantsPost**](WyszukiwanieNadanychUprawnieKsefApi.md#apiV2PermissionsQueryEuEntitiesGrantsPost) | **POST** /api/v2/permissions/query/eu-entities/grants | Pobranie listy uprawnień administratorów lub reprezentantów podmiotów unijnych uprawnionych do samofakturowania |
| [**apiV2PermissionsQueryPersonalGrantsPost**](WyszukiwanieNadanychUprawnieKsefApi.md#apiV2PermissionsQueryPersonalGrantsPost) | **POST** /api/v2/permissions/query/personal/grants | Pobranie listy własnych uprawnień |
| [**apiV2PermissionsQueryPersonsGrantsPost**](WyszukiwanieNadanychUprawnieKsefApi.md#apiV2PermissionsQueryPersonsGrantsPost) | **POST** /api/v2/permissions/query/persons/grants | Pobranie listy uprawnień do pracy w KSeF nadanych osobom fizycznym lub podmiotom |
| [**apiV2PermissionsQuerySubordinateEntitiesRolesPost**](WyszukiwanieNadanychUprawnieKsefApi.md#apiV2PermissionsQuerySubordinateEntitiesRolesPost) | **POST** /api/v2/permissions/query/subordinate-entities/roles | Pobranie listy podmiotów podrzędnych |
| [**apiV2PermissionsQuerySubunitsGrantsPost**](WyszukiwanieNadanychUprawnieKsefApi.md#apiV2PermissionsQuerySubunitsGrantsPost) | **POST** /api/v2/permissions/query/subunits/grants | Pobranie listy uprawnień administratorów jednostek i podmiotów podrzędnych |


<a id="apiV2PermissionsQueryAuthorizationsGrantsPost"></a>
# **apiV2PermissionsQueryAuthorizationsGrantsPost**
> QueryEntityAuthorizationPermissionsResponse apiV2PermissionsQueryAuthorizationsGrantsPost(pageOffset, pageSize, entityAuthorizationPermissionsQueryRequest)

Pobranie listy uprawnień podmiotowych do obsługi faktur

Zwraca listę uprawnień podmiotowych do obsługi faktur.  &gt; Więcej informacji: &gt; - [Pobieranie listy uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-uprawnie%C5%84-podmiotowych-do-obs%C5%82ugi-faktur)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;, &#x60;CredentialsRead&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = WyszukiwanieNadanychUprawnieKsefApi()
val pageOffset : kotlin.Int = 56 // kotlin.Int | Numer strony wyników.
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników.
val entityAuthorizationPermissionsQueryRequest : EntityAuthorizationPermissionsQueryRequest = {"authorizedIdentifier":{"type":"Nip","value":"7762811692"},"queryType":"Granted","permissionTypes":["SelfInvoicing","TaxRepresentative","RRInvoicing"]} // EntityAuthorizationPermissionsQueryRequest | 
try {
    val result : QueryEntityAuthorizationPermissionsResponse = apiInstance.apiV2PermissionsQueryAuthorizationsGrantsPost(pageOffset, pageSize, entityAuthorizationPermissionsQueryRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQueryAuthorizationsGrantsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQueryAuthorizationsGrantsPost")
    e.printStackTrace()
}
```

### Parameters
| **pageOffset** | **kotlin.Int**| Numer strony wyników. | [optional] |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **entityAuthorizationPermissionsQueryRequest** | [**EntityAuthorizationPermissionsQueryRequest**](EntityAuthorizationPermissionsQueryRequest.md)|  | [optional] |

### Return type

[**QueryEntityAuthorizationPermissionsResponse**](QueryEntityAuthorizationPermissionsResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2PermissionsQueryEntitiesRolesGet"></a>
# **apiV2PermissionsQueryEntitiesRolesGet**
> QueryEntityRolesResponse apiV2PermissionsQueryEntitiesRolesGet(pageOffset, pageSize)

Pobranie listy ról podmiotu

Zwraca listę ról podmiotu.  &gt; Więcej informacji: &gt; - [Pobieranie listy ról](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-r%C3%B3l-podmiotu)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;, &#x60;CredentialsRead&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = WyszukiwanieNadanychUprawnieKsefApi()
val pageOffset : kotlin.Int = 56 // kotlin.Int | Numer strony wyników.
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników.
try {
    val result : QueryEntityRolesResponse = apiInstance.apiV2PermissionsQueryEntitiesRolesGet(pageOffset, pageSize)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQueryEntitiesRolesGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQueryEntitiesRolesGet")
    e.printStackTrace()
}
```

### Parameters
| **pageOffset** | **kotlin.Int**| Numer strony wyników. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. | [optional] |

### Return type

[**QueryEntityRolesResponse**](QueryEntityRolesResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2PermissionsQueryEuEntitiesGrantsPost"></a>
# **apiV2PermissionsQueryEuEntitiesGrantsPost**
> QueryEuEntityPermissionsResponse apiV2PermissionsQueryEuEntitiesGrantsPost(pageOffset, pageSize, euEntityPermissionsQueryRequest)

Pobranie listy uprawnień administratorów lub reprezentantów podmiotów unijnych uprawnionych do samofakturowania

Zwraca listę uprawnień administratorów lub reprezentantów podmiotów unijnych uprawnionych do samofakturowania.  &gt; Więcej informacji: &gt; - [Pobieranie listy uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-uprawnie%C5%84-administrator%C3%B3w-lub-reprezentant%C3%B3w-podmiot%C3%B3w-unijnych-uprawnionych-do-samofakturowania)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;, &#x60;CredentialsRead&#x60;, &#x60;VatUeManage&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = WyszukiwanieNadanychUprawnieKsefApi()
val pageOffset : kotlin.Int = 56 // kotlin.Int | Numer strony wyników.
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników.
val euEntityPermissionsQueryRequest : EuEntityPermissionsQueryRequest = {"vatUeIdentifier":"DE123456789012","permissionTypes":["VatUeManage","Introspection"]} // EuEntityPermissionsQueryRequest | 
try {
    val result : QueryEuEntityPermissionsResponse = apiInstance.apiV2PermissionsQueryEuEntitiesGrantsPost(pageOffset, pageSize, euEntityPermissionsQueryRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQueryEuEntitiesGrantsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQueryEuEntitiesGrantsPost")
    e.printStackTrace()
}
```

### Parameters
| **pageOffset** | **kotlin.Int**| Numer strony wyników. | [optional] |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **euEntityPermissionsQueryRequest** | [**EuEntityPermissionsQueryRequest**](EuEntityPermissionsQueryRequest.md)|  | [optional] |

### Return type

[**QueryEuEntityPermissionsResponse**](QueryEuEntityPermissionsResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2PermissionsQueryPersonalGrantsPost"></a>
# **apiV2PermissionsQueryPersonalGrantsPost**
> QueryPersonalPermissionsResponse apiV2PermissionsQueryPersonalGrantsPost(pageOffset, pageSize, personalPermissionsQueryRequest)

Pobranie listy własnych uprawnień

Zwraca listę uprawnień przysługujących uwierzytelnionemu podmiotowi.  &gt; Więcej informacji: &gt; - [Pobieranie listy uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-w%C5%82asnych-uprawnie%C5%84)

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = WyszukiwanieNadanychUprawnieKsefApi()
val pageOffset : kotlin.Int = 56 // kotlin.Int | Numer strony wyników.
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników.
val personalPermissionsQueryRequest : PersonalPermissionsQueryRequest =  // PersonalPermissionsQueryRequest | 
try {
    val result : QueryPersonalPermissionsResponse = apiInstance.apiV2PermissionsQueryPersonalGrantsPost(pageOffset, pageSize, personalPermissionsQueryRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQueryPersonalGrantsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQueryPersonalGrantsPost")
    e.printStackTrace()
}
```

### Parameters
| **pageOffset** | **kotlin.Int**| Numer strony wyników. | [optional] |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **personalPermissionsQueryRequest** | [**PersonalPermissionsQueryRequest**](PersonalPermissionsQueryRequest.md)|  | [optional] |

### Return type

[**QueryPersonalPermissionsResponse**](QueryPersonalPermissionsResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2PermissionsQueryPersonsGrantsPost"></a>
# **apiV2PermissionsQueryPersonsGrantsPost**
> QueryPersonPermissionsResponse apiV2PermissionsQueryPersonsGrantsPost(pageOffset, pageSize, personPermissionsQueryRequest)

Pobranie listy uprawnień do pracy w KSeF nadanych osobom fizycznym lub podmiotom

Zwraca listę uprawnień do pracy w KSeF nadanych osobom fizycznym lub podmiotom.  &gt; Więcej informacji: &gt; - [Pobieranie listy uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-uprawnie%C5%84-do-pracy-w-ksef-nadanych-osobom-fizycznym-lub-podmiotom)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;, &#x60;CredentialsRead&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = WyszukiwanieNadanychUprawnieKsefApi()
val pageOffset : kotlin.Int = 56 // kotlin.Int | Numer strony wyników.
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników.
val personPermissionsQueryRequest : PersonPermissionsQueryRequest = {"authorIdentifier":{"type":"Nip","value":"7762811692"},"permissionTypes":["CredentialsManage","CredentialsRead","InvoiceWrite"],"permissionState":"Active","queryType":"PermissionsInCurrentContext"} // PersonPermissionsQueryRequest | 
try {
    val result : QueryPersonPermissionsResponse = apiInstance.apiV2PermissionsQueryPersonsGrantsPost(pageOffset, pageSize, personPermissionsQueryRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQueryPersonsGrantsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQueryPersonsGrantsPost")
    e.printStackTrace()
}
```

### Parameters
| **pageOffset** | **kotlin.Int**| Numer strony wyników. | [optional] |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **personPermissionsQueryRequest** | [**PersonPermissionsQueryRequest**](PersonPermissionsQueryRequest.md)|  | [optional] |

### Return type

[**QueryPersonPermissionsResponse**](QueryPersonPermissionsResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2PermissionsQuerySubordinateEntitiesRolesPost"></a>
# **apiV2PermissionsQuerySubordinateEntitiesRolesPost**
> QuerySubordinateEntityRolesResponse apiV2PermissionsQuerySubordinateEntitiesRolesPost(pageOffset, pageSize, subordinateEntityRolesQueryRequest)

Pobranie listy podmiotów podrzędnych

Zwraca liste podmiotów podrzędnych.  &gt; Więcej informacji: &gt; - [Pobieranie listy podmiotów podrzędnych](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-podmiot%C3%B3w-podrz%C4%99dnych)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;, &#x60;CredentialsRead&#x60;, &#x60;SubunitManage&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = WyszukiwanieNadanychUprawnieKsefApi()
val pageOffset : kotlin.Int = 56 // kotlin.Int | Numer strony wyników.
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników.
val subordinateEntityRolesQueryRequest : SubordinateEntityRolesQueryRequest = {"subordinateEntityIdentifier":{"type":"Nip","value":"7762811692"}} // SubordinateEntityRolesQueryRequest | 
try {
    val result : QuerySubordinateEntityRolesResponse = apiInstance.apiV2PermissionsQuerySubordinateEntitiesRolesPost(pageOffset, pageSize, subordinateEntityRolesQueryRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQuerySubordinateEntitiesRolesPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQuerySubordinateEntitiesRolesPost")
    e.printStackTrace()
}
```

### Parameters
| **pageOffset** | **kotlin.Int**| Numer strony wyników. | [optional] |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subordinateEntityRolesQueryRequest** | [**SubordinateEntityRolesQueryRequest**](SubordinateEntityRolesQueryRequest.md)|  | [optional] |

### Return type

[**QuerySubordinateEntityRolesResponse**](QuerySubordinateEntityRolesResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2PermissionsQuerySubunitsGrantsPost"></a>
# **apiV2PermissionsQuerySubunitsGrantsPost**
> QuerySubunitPermissionsResponse apiV2PermissionsQuerySubunitsGrantsPost(pageOffset, pageSize, subunitPermissionsQueryRequest)

Pobranie listy uprawnień administratorów jednostek i podmiotów podrzędnych

Zwraca listę uprawnień administratorów jednostek i podmiotów podrzędnych.  &gt; Więcej informacji: &gt; - [Pobieranie listy uprawnień](https://github.com/CIRFMF/ksef-docs/blob/main/uprawnienia.md#pobranie-listy-uprawnie%C5%84-administrator%C3%B3w-jednostek-i-podmiot%C3%B3w-podrz%C4%99dnych)  Wymagane uprawnienia: &#x60;CredentialsManage&#x60;, &#x60;CredentialsRead&#x60;, &#x60;SubunitManage&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = WyszukiwanieNadanychUprawnieKsefApi()
val pageOffset : kotlin.Int = 56 // kotlin.Int | Numer strony wyników.
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników.
val subunitPermissionsQueryRequest : SubunitPermissionsQueryRequest = {"subunitIdentifier":{"type":"InternalId","value":"7762811692-12345"}} // SubunitPermissionsQueryRequest | 
try {
    val result : QuerySubunitPermissionsResponse = apiInstance.apiV2PermissionsQuerySubunitsGrantsPost(pageOffset, pageSize, subunitPermissionsQueryRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQuerySubunitsGrantsPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WyszukiwanieNadanychUprawnieKsefApi#apiV2PermissionsQuerySubunitsGrantsPost")
    e.printStackTrace()
}
```

### Parameters
| **pageOffset** | **kotlin.Int**| Numer strony wyników. | [optional] |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subunitPermissionsQueryRequest** | [**SubunitPermissionsQueryRequest**](SubunitPermissionsQueryRequest.md)|  | [optional] |

### Return type

[**QuerySubunitPermissionsResponse**](QuerySubunitPermissionsResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

