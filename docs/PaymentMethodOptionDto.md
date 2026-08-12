

# PaymentMethodOptionDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**method** | [**MethodEnum**](#MethodEnum) |  |  [optional] |
|**displayName** | **String** |  |  [optional] |
|**iframe** | **Boolean** |  |  [optional] |
|**supportedCards** | [**Set&lt;SupportedCardsEnum&gt;**](#Set&lt;SupportedCardsEnum&gt;) |  |  [optional] |



## Enum: MethodEnum

| Name | Value |
|---- | -----|
| WALLET | &quot;WALLET&quot; |
| PAYME | &quot;PAYME&quot; |
| APPLE_PAY | &quot;APPLE_PAY&quot; |
| GOOGLE_PAY | &quot;GOOGLE_PAY&quot; |



## Enum: Set&lt;SupportedCardsEnum&gt;

| Name | Value |
|---- | -----|
| VISA | &quot;VISA&quot; |
| MASTERCARD | &quot;MASTERCARD&quot; |



