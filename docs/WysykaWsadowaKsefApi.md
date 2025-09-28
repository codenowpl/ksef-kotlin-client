# WysykaWsadowaKsefApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**apiV2SessionsBatchReferenceNumberClosePost**](WysykaWsadowaKsefApi.md#apiV2SessionsBatchReferenceNumberClosePost) | **POST** /api/v2/sessions/batch/{referenceNumber}/close | Zamknięcie sesji wsadowej |
| [**batchOpen**](WysykaWsadowaKsefApi.md#batchOpen) | **POST** /api/v2/sessions/batch | Otwarcie sesji wsadowej |


<a id="apiV2SessionsBatchReferenceNumberClosePost"></a>
# **apiV2SessionsBatchReferenceNumberClosePost**
> apiV2SessionsBatchReferenceNumberClosePost(referenceNumber)

Zamknięcie sesji wsadowej

Zamyka sesję wsadową, rozpoczyna procesowanie paczki faktur i generowanie UPO dla prawidłowych faktur oraz zbiorczego UPO dla sesji.  Wymagane uprawnienia: &#x60;InvoiceWrite&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = WysykaWsadowaKsefApi()
val referenceNumber : kotlin.String = referenceNumber_example // kotlin.String | Numer referencyjny sesji
try {
    apiInstance.apiV2SessionsBatchReferenceNumberClosePost(referenceNumber)
} catch (e: ClientException) {
    println("4xx response calling WysykaWsadowaKsefApi#apiV2SessionsBatchReferenceNumberClosePost")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WysykaWsadowaKsefApi#apiV2SessionsBatchReferenceNumberClosePost")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **referenceNumber** | **kotlin.String**| Numer referencyjny sesji | |

### Return type

null (empty response body)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a id="batchOpen"></a>
# **batchOpen**
> OpenBatchSessionResponse batchOpen(openBatchSessionRequest)

Otwarcie sesji wsadowej

Otwiera sesję do wysyłki wsadowej faktur. Należy przekazać schemat wysyłanych faktur, informacje o paczce faktur oraz informacje o kluczu używanym do szyfrowania.  &gt; Więcej informacji: &gt; - [Przygotwanie paczki faktur](https://github.com/CIRFMF/ksef-docs/blob/main/sesja-wsadowa.md) &gt; - [Klucz publiczny Ministersta Finansów](/docs/v2/index.html#tag/Certyfikaty-klucza-publicznego)  Wymagane uprawnienia: &#x60;InvoiceWrite&#x60;.

### Example
```kotlin
// Import classes:
//import pl.com.codenow.ksefclient.infrastructure.*
//import pl.com.codenow.ksefclient.models.*

val apiInstance = WysykaWsadowaKsefApi()
val openBatchSessionRequest : OpenBatchSessionRequest = {"formCode":{"systemCode":"FA (2)","schemaVersion":"1-0E","value":"FA"},"batchFile":{"fileSize":16037,"fileHash":"WO86CC+1Lef11wEosItld/NPwxGN8tobOMLqk9PQjgs=","fileParts":[{"ordinalNumber":1,"fileName":"92cca5be-7f37-4d36-98bb-1f5369841038.zip.aes","fileSize":16048,"fileHash":"23ZyDAN0H/+yhC/En2xbNfF0tajAWSfejDaXD7fc2AE="}]},"encryption":{"encryptedSymmetricKey":"bYqmPAglF01AxZim4oNa+1NerhZYfFgLMnvksBprUur1aesQ0Y5jsmOIfCrozfMkF2tjdO+uOsBg4FPlDgjChwN2/tz2Hqwtxq3RkTr1SjY4x8jxJFpPedcS7EI+XO8C+i9mLj7TFx9p/bg07yM9vHtMAk5b88Ay9Qc3+T5Ch1DM2ClR3sVu2DqdlKzmbINY+rhfGtXn58Qo0XRyESGgc6M0iTZVBRPuPXLnD8a1KpOneCpNzLwxgT6Ei3ivLOpPWT53PxkRTaQ8puj6CIiCKo4FHQzHuI/NmrAhYU7TkNm2kymP/OxBgWdg3XB74tqNFfT8RZN1bZXuPhBidDOqa+xsqY3E871FSDmQwZf58HmoNl31XNvpnryiRGfnAISt+m+ELqgksAresVu6E9poUL1yiff+IOHSZABoYpNiqwnbT8qyW1uk8lKLyFVFu+kOsbzBk1OWWHqSkNFDaznDa2MKjHonOXI0uyKaKWvoBFC4dWN1PVumfpSSFAeYgNpAyVrZdcVOuiliEWepTDjGzJoOafTvwr5za2S6B5bPECDpX7JXazV7Olkq7ezG0w8y3olx+0C+NHoCk8B5/cm4gtVHTgKjiLSGpKJVOJABLXFkOyIOjbQsVe4ryX0Qy+SfL7JIQvTWvM5xkCoOMbzLdMo9tNo5qE34sguFI+lIevY=","initializationVector":"jWpJLNBHJ5pQEGCBglmIAw=="},"offlineMode":false} // OpenBatchSessionRequest | 
try {
    val result : OpenBatchSessionResponse = apiInstance.batchOpen(openBatchSessionRequest)
    println(result)
} catch (e: ClientException) {
    println("4xx response calling WysykaWsadowaKsefApi#batchOpen")
    e.printStackTrace()
} catch (e: ServerException) {
    println("5xx response calling WysykaWsadowaKsefApi#batchOpen")
    e.printStackTrace()
}
```

### Parameters
| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **openBatchSessionRequest** | [**OpenBatchSessionRequest**](OpenBatchSessionRequest.md)|  | [optional] |

### Return type

[**OpenBatchSessionResponse**](OpenBatchSessionResponse.md)

### Authorization


Configure Bearer:
    ApiClient.accessToken = ""

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

