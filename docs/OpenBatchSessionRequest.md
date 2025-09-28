
# OpenBatchSessionRequest

## Properties
| Name | Type | Description | Notes |
| ------------ | ------------- | ------------- | ------------- |
| **formCode** | [**FormCode**](FormCode.md) | Schemat faktur wysyłanych w ramach sesji.  Obsługiwane schematy: | SystemCode | SchemaVersion | Value | | --- | --- | --- | | FA (2) | 1-0E | FA | | FA (3) | 1-0E | FA |  |  |
| **batchFile** | [**BatchFileInfo**](BatchFileInfo.md) | Informacje o przesyłanej paczce faktur. |  |
| **encryption** | [**EncryptionInfo**](EncryptionInfo.md) | Symetryczny klucz szyfrujący plik paczki, zaszyfrowany kluczem publicznym Ministerstwa Finansów. |  |
| **offlineMode** | **kotlin.Boolean** | Określa, czy podatnik deklaruje tryb fakurowania \&quot;offline\&quot; dla dokumentów przesyłanych w sesji wsadowej. |  [optional] |



