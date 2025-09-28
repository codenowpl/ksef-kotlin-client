# UzyskiwanieDostpuKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2AuthChallengePost**](UzyskiwanieDostpuKsefApi.md#apiV2AuthChallengePost) | **POST** /api/v2/auth/challenge | Inicjalizacja uwierzytelnienia |
| [**apiV2AuthKsefTokenPost**](UzyskiwanieDostpuKsefApi.md#apiV2AuthKsefTokenPost) | **POST** /api/v2/auth/ksef-token | Uwierzytelnienie z wykorzystaniem tokena KSeF |
| [**apiV2AuthReferenceNumberGet**](UzyskiwanieDostpuKsefApi.md#apiV2AuthReferenceNumberGet) | **GET** /api/v2/auth/{referenceNumber} | Pobranie statusu uwierzytelniania |
| [**apiV2AuthTokenRedeemPost**](UzyskiwanieDostpuKsefApi.md#apiV2AuthTokenRedeemPost) | **POST** /api/v2/auth/token/redeem | Pobranie tokenów dostępowych |
| [**apiV2AuthTokenRefreshPost**](UzyskiwanieDostpuKsefApi.md#apiV2AuthTokenRefreshPost) | **POST** /api/v2/auth/token/refresh | Odświeżenie tokena dostępowego |
| [**apiV2AuthXadesSignaturePost**](UzyskiwanieDostpuKsefApi.md#apiV2AuthXadesSignaturePost) | **POST** /api/v2/auth/xades-signature | Uwierzytelnienie z wykorzystaniem podpisu XAdES |


<a id="apiV2AuthChallengePost"></a>
# **apiV2AuthChallengePost**
> AuthenticationChallengeResponse apiV2AuthChallengePost()

Inicjalizacja uwierzytelnienia

Generuje unikalny challenge wymagany w kolejnym kroku operacji uwierzytelnienia.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = UzyskiwanieDostpuKsefApi()
try {
    val result : AuthenticationChallengeResponse = apiInstance.apiV2AuthChallengePost()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling UzyskiwanieDostpuKsefApi#apiV2AuthChallengePost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling UzyskiwanieDostpuKsefApi#apiV2AuthChallengePost")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AuthenticationChallengeResponse**](AuthenticationChallengeResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2AuthKsefTokenPost"></a>
# **apiV2AuthKsefTokenPost**
> AuthenticationInitResponse apiV2AuthKsefTokenPost(initTokenAuthenticationRequest)

Uwierzytelnienie z wykorzystaniem tokena KSeF

Rozpoczyna operację uwierzytelniania z wykorzystaniem wcześniej wygenerowanego tokena KSeF.  Token KSeF wraz z timestampem ze wcześniej wygenerowanego challenge&#39;a (w formacie &#x60;&#x60;&#x60;token|timestamp&#x60;&#x60;&#x60;) powinien zostać zaszyfrowany dedykowanym do tego celu kluczem publicznym. - Timestamp powinien zostać przekazany jako **liczba milisekund od 1 stycznia 1970 roku (Unix timestamp)**. - Algorytm szyfrowania: **RSA-OAEP (z użyciem SHA-256 jako funkcji skrótu)**.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = UzyskiwanieDostpuKsefApi()
val initTokenAuthenticationRequest : InitTokenAuthenticationRequest = {"challenge":"20250625-CR-2FDC223000-C2BFC98A9C-4E","contextIdentifier":{"type":"Nip","value":"5265877635"},"encryptedToken":"..."} // InitTokenAuthenticationRequest | 
try {
    val result : AuthenticationInitResponse = apiInstance.apiV2AuthKsefTokenPost(initTokenAuthenticationRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling UzyskiwanieDostpuKsefApi#apiV2AuthKsefTokenPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling UzyskiwanieDostpuKsefApi#apiV2AuthKsefTokenPost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **initTokenAuthenticationRequest** | [**InitTokenAuthenticationRequest**](InitTokenAuthenticationRequest.md)|  | [optional] |

### Return type

[**AuthenticationInitResponse**](AuthenticationInitResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a id="apiV2AuthReferenceNumberGet"></a>
# **apiV2AuthReferenceNumberGet**
> AuthenticationOperationStatusResponse apiV2AuthReferenceNumberGet(referenceNumber)

Pobranie statusu uwierzytelniania

Sprawdza bieżący status operacji uwierzytelniania dla podanego tokena.  Sposób uwierzytelnienia: &#x60;AuthenticationToken&#x60; otrzymany przy rozpoczęciu operacji uwierzytelniania.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = UzyskiwanieDostpuKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny tokena otrzymanego przy inicjalizacji operacji uwierzytelniania.
try {
    val result : AuthenticationOperationStatusResponse = apiInstance.apiV2AuthReferenceNumberGet(referenceNumber)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling UzyskiwanieDostpuKsefApi#apiV2AuthReferenceNumberGet")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling UzyskiwanieDostpuKsefApi#apiV2AuthReferenceNumberGet")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **referenceNumber** | **kotlin.String**| Numer referencyjny tokena otrzymanego przy inicjalizacji operacji uwierzytelniania. | |

### Return type

[**AuthenticationOperationStatusResponse**](AuthenticationOperationStatusResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2AuthTokenRedeemPost"></a>
# **apiV2AuthTokenRedeemPost**
> AuthenticationTokensResponse apiV2AuthTokenRedeemPost()

Pobranie tokenów dostępowych

Pobiera parę tokenów (access token i refresh token) wygenerowanych w ramach pozytywnie zakończonego procesu uwierzytelniania. **Tokeny można pobrać tylko raz.**  Sposób uwierzytelnienia: &#x60;AuthenticationToken&#x60; otrzymany przy rozpoczęciu operacji uwierzytelniania.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = UzyskiwanieDostpuKsefApi()
try {
    val result : AuthenticationTokensResponse = apiInstance.apiV2AuthTokenRedeemPost()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling UzyskiwanieDostpuKsefApi#apiV2AuthTokenRedeemPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling UzyskiwanieDostpuKsefApi#apiV2AuthTokenRedeemPost")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AuthenticationTokensResponse**](AuthenticationTokensResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2AuthTokenRefreshPost"></a>
# **apiV2AuthTokenRefreshPost**
> AuthenticationTokenRefreshResponse apiV2AuthTokenRefreshPost()

Odświeżenie tokena dostępowego

Generuje nowy token dostępu na podstawie ważnego refresh tokena.  Sposób uwierzytelnienia: &#x60;RefreshToken&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = UzyskiwanieDostpuKsefApi()
try {
    val result : AuthenticationTokenRefreshResponse = apiInstance.apiV2AuthTokenRefreshPost()
    println(result)
} catch (e: ClientException) {
    println("4xx response calling UzyskiwanieDostpuKsefApi#apiV2AuthTokenRefreshPost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling UzyskiwanieDostpuKsefApi#apiV2AuthTokenRefreshPost")
    e.printStackTrace()
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AuthenticationTokenRefreshResponse**](AuthenticationTokenRefreshResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="apiV2AuthXadesSignaturePost"></a>
# **apiV2AuthXadesSignaturePost**
> AuthenticationInitResponse apiV2AuthXadesSignaturePost(body, verifyCertificateChain)

Uwierzytelnienie z wykorzystaniem podpisu XAdES

Rozpoczyna operację uwierzytelniania za pomocą dokumentu XML podpisanego podpisem elektronicznym XAdES.  &gt; Więcej informacji: &gt; - [Przygotowanie dokumentu XML](https://github.com/CIRFMF/ksef-docs/blob/main/uwierzytelnianie.md#1-przygotowanie-dokumentu-xml-authtokenrequest) &gt; - [Podpis dokumentu XML](https://github.com/CIRFMF/ksef-docs/blob/main/uwierzytelnianie.md#2-podpisanie-dokumentu-xades) &gt; - [Schemat XSD](/docs/v2/schemas/authv2.xsd)

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = UzyskiwanieDostpuKsefApi()
val body : kotlin.String = <?xml version="1.0" encoding="utf-8"?>
<AuthTokenRequest xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns="http://ksef.mf.gov.pl/auth/token/2.0">
    <Challenge>20250625-CR-20F5EE4000-DA48AE4124-46</Challenge>
    <ContextIdentifier>
        <Nip>5265877635</Nip>
    </ContextIdentifier>
    <SubjectIdentifierType>certificateSubject</SubjectIdentifierType>
    <ds:Signature xmlns:ds="http://www.w3.org/2000/09/xmldsig#" Id="Signature-9707709">
        <!-- Tu powinien być podpis XAdES -->
    </ds:Signature>
</AuthTokenRequest> // kotlin.String | 
val verifyCertificateChain : kotlin.Boolean = true // kotlin.Boolean | Wymuszenie weryfikacji zaufania łańcucha certyfikatu wraz ze sprawdzeniem statusu certyfikatu (OCSP/CRL) na środowiskach które umożliwiają wykorzystanie samodzielnie wygenerowanych certyfikatów.
try {
    val result : AuthenticationInitResponse = apiInstance.apiV2AuthXadesSignaturePost(body, verifyCertificateChain)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling UzyskiwanieDostpuKsefApi#apiV2AuthXadesSignaturePost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling UzyskiwanieDostpuKsefApi#apiV2AuthXadesSignaturePost")
    e.printStackTrace()
}
```

### Parameters
| **body** | **kotlin.String**|  | |
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **verifyCertificateChain** | **kotlin.Boolean**| Wymuszenie weryfikacji zaufania łańcucha certyfikatu wraz ze sprawdzeniem statusu certyfikatu (OCSP/CRL) na środowiskach które umożliwiają wykorzystanie samodzielnie wygenerowanych certyfikatów. | [optional] |

### Return type

[**AuthenticationInitResponse**](AuthenticationInitResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

