
# SendInvoiceRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **invoiceHash** | **kotlin.String** | Skrót SHA256 oryginalnej faktury, zakodowany w formacie Base64. |  |
| **invoiceSize** | **kotlin.Long** | Rozmiar oryginalnej faktury w bajtach. |  |
| **encryptedInvoiceHash** | **kotlin.String** | Skrót SHA256 zaszyfrowanej faktury, zakodowany w formacie Base64. |  |
| **encryptedInvoiceSize** | **kotlin.Long** | Rozmiar zaszyfrowanej faktury w bajtach. |  |
| **encryptedInvoiceContent** | **kotlin.String** | Faktura zaszyfrowana algorytmem AES-256-CBC z dopełnianiem PKCS#7 (kluczem przekazanym przy otwarciu sesji), zakodowana w formacie Base64. |  |
| **offlineMode** | **kotlin.Boolean** | Określa, czy podatnik deklaruje tryb fakturowania \&quot;offline\&quot; dla przesyłanego dokumentu. |  [optional] |
| **hashOfCorrectedInvoice** | **kotlin.String** | Skrót SHA256 korygowanej faktury, zakodowany w formacie Base64. Wymagany przy wysyłaniu korekty technicznej faktury. |  [optional] |



