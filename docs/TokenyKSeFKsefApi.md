# TokenyKSeFKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**tokenGenerate**](TokenyKSeFKsefApi.md#tokenGenerate) | **POST** /api/v2/tokens | Wygenerowanie nowego tokena |
| [**tokenQuery**](TokenyKSeFKsefApi.md#tokenQuery) | **GET** /api/v2/tokens | Pobranie listy wygenerowanych tokenów |
| [**tokenRevoke**](TokenyKSeFKsefApi.md#tokenRevoke) | **DELETE** /api/v2/tokens/{referenceNumber} | Unieważnienie tokena |
| [**tokenStatus**](TokenyKSeFKsefApi.md#tokenStatus) | **GET** /api/v2/tokens/{referenceNumber} | Pobranie statusu tokena |


<a id="tokenGenerate"></a>
# **tokenGenerate**
> GenerateTokenResponse tokenGenerate(generateTokenRequest)

Wygenerowanie nowego tokena

Zwraca token, który może być użyty do uwierzytelniania się w KSeF.  Token może być generowany tylko w kontekście NIP lub identyfikatora wewnętrznego. Jest zwracany tylko raz. Zaczyna być aktywny w momencie gdy jego status zmieni się na &#x60;Active&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = TokenyKSeFKsefApi()
val generateTokenRequest : GenerateTokenRequest =  // GenerateTokenRequest | 
try {
    val result : GenerateTokenResponse = apiInstance.tokenGenerate(generateTokenRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TokenyKSeFKsefApi#tokenGenerate")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TokenyKSeFKsefApi#tokenGenerate")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **generateTokenRequest** | [**GenerateTokenRequest**](GenerateTokenRequest.md)|  | [optional] |

### Return type

[**GenerateTokenResponse**](GenerateTokenResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="tokenQuery"></a>
# **tokenQuery**
> QueryTokensResponse tokenQuery(status, description, authorIdentifier, authorIdentifierType, pageSize, xContinuationToken)

Pobranie listy wygenerowanych tokenów

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = TokenyKSeFKsefApi()
val status : kotlin.collections.List<AuthenticationTokenStatus> =  // kotlin.collections.List<AuthenticationTokenStatus> | Status tokenów do zwrócenia. W przypadku braku parametru zwracane są wszystkie tokeny. Parametr można przekazać wielokrotnie. | Wartość | Opis | | --- | --- | | Pending | Token został utworzony ale jest jeszcze w trakcie aktywacji i nadawania uprawnień. Nie może być jeszcze wykorzystywany do uwierzytelniania. | | Active | Token jest aktywny i może być wykorzystywany do uwierzytelniania. | | Revoking | Token jest w trakcie unieważniania. Nie może już być wykorzystywany do uwierzytelniania. | | Revoked | Token został unieważniony i nie może być wykorzystywany do uwierzytelniania. | | Failed | Nie udało się aktywować tokena. Należy wygenerować nowy token, obecny nie może być wykorzystywany do uwierzytelniania. | 
val description : kotlin.String = description_example // kotlin.String | Umożliwia filtrowanie tokenów po opisie. Wartość parametru jest wyszukiwana w opisie tokena (operacja nie rozróżnia wielkości liter). Należy podać co najmniej 3 znaki.
val authorIdentifier : kotlin.String = authorIdentifier_example // kotlin.String | Umożliwia filtrowanie tokenów po ich twórcy. Wartość parametru jest wyszukiwana w identyfikatorze (operacja nie rozróżnia wielkości liter). Należy podać co najmniej 3 znaki.
val authorIdentifierType : AuthorIdentifierType =  // AuthorIdentifierType | Umożliwia filtrowanie tokenów po ich twórcy. Wartość parametru określa typ identyfikatora w którym będzie wyszukiwany ciąg znaków przekazany w parametrze `authorIdentifier`. | Wartość | Opis | | --- | --- | | Nip | NIP. | | Pesel | PESEL. | | Fingerprint | Odcisk palca certyfikatu. | 
val pageSize : kotlin.Int = 56 // kotlin.Int | Rozmiar strony wyników.
val xContinuationToken : kotlin.String = xContinuationToken_example // kotlin.String | Token służący do pobrania kolejnej strony wyników.
try {
    val result : QueryTokensResponse = apiInstance.tokenQuery(status, description, authorIdentifier, authorIdentifierType, pageSize, xContinuationToken)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TokenyKSeFKsefApi#tokenQuery")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TokenyKSeFKsefApi#tokenQuery")
    e.printStackTrace()
}
```

### Parameters
| **status** | [**kotlin.collections.List&lt;AuthenticationTokenStatus&gt;**](AuthenticationTokenStatus.md)| Status tokenów do zwrócenia. W przypadku braku parametru zwracane są wszystkie tokeny. Parametr można przekazać wielokrotnie. | Wartość | Opis | | --- | --- | | Pending | Token został utworzony ale jest jeszcze w trakcie aktywacji i nadawania uprawnień. Nie może być jeszcze wykorzystywany do uwierzytelniania. | | Active | Token jest aktywny i może być wykorzystywany do uwierzytelniania. | | Revoking | Token jest w trakcie unieważniania. Nie może już być wykorzystywany do uwierzytelniania. | | Revoked | Token został unieważniony i nie może być wykorzystywany do uwierzytelniania. | | Failed | Nie udało się aktywować tokena. Należy wygenerować nowy token, obecny nie może być wykorzystywany do uwierzytelniania. |  | [optional] |
| **description** | **kotlin.String**| Umożliwia filtrowanie tokenów po opisie. Wartość parametru jest wyszukiwana w opisie tokena (operacja nie rozróżnia wielkości liter). Należy podać co najmniej 3 znaki. | [optional] |
| **authorIdentifier** | **kotlin.String**| Umożliwia filtrowanie tokenów po ich twórcy. Wartość parametru jest wyszukiwana w identyfikatorze (operacja nie rozróżnia wielkości liter). Należy podać co najmniej 3 znaki. | [optional] |
| **authorIdentifierType** | [**AuthorIdentifierType**](.md)| Umożliwia filtrowanie tokenów po ich twórcy. Wartość parametru określa typ identyfikatora w którym będzie wyszukiwany ciąg znaków przekazany w parametrze &#x60;authorIdentifier&#x60;. | Wartość | Opis | | --- | --- | | Nip | NIP. | | Pesel | PESEL. | | Fingerprint | Odcisk palca certyfikatu. |  | [optional] [enum: Nip, Pesel, Fingerprint] |
| **pageSize** | **kotlin.Int**| Rozmiar strony wyników. | [optional] |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **xContinuationToken** | **kotlin.String**| Token służący do pobrania kolejnej strony wyników. | [optional] |

### Return type

[**QueryTokensResponse**](QueryTokensResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="tokenRevoke"></a>
# **tokenRevoke**
> tokenRevoke(referenceNumber)

Unieważnienie tokena

Unieważniony token nie pozwoli już na uwierzytelnienie się za jego pomocą. Unieważnienie nie może zostać cofnięte.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = TokenyKSeFKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny tokena do unieważeniania.
try {
    apiInstance.tokenRevoke(referenceNumber)
} catch (e: ClientException) {
    println("4xx response calling TokenyKSeFKsefApi#tokenRevoke")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TokenyKSeFKsefApi#tokenRevoke")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **referenceNumber** | **kotlin.String**| Numer referencyjny tokena do unieważeniania. | |

### Return type

null (empty response body)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="tokenStatus"></a>
# **tokenStatus**
> AuthenticationToken tokenStatus(referenceNumber)

Pobranie statusu tokena

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = TokenyKSeFKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny tokena.
try {
    val result : AuthenticationToken = apiInstance.tokenStatus(referenceNumber)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling TokenyKSeFKsefApi#tokenStatus")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling TokenyKSeFKsefApi#tokenStatus")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **referenceNumber** | **kotlin.String**| Numer referencyjny tokena. | |

### Return type

[**AuthenticationToken**](AuthenticationToken.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

