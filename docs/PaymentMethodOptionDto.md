

# PaymentMethodOptionDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**method** | [**MethodEnum**](#MethodEnum) |  |  [optional] |
|**displayName** | **String** |  |  [optional] |
|**iframe** | **Boolean** |  |  [optional] |
|**supportedCards** | [**Set&lt;SupportedCardsEnum&gt;**](#Set&lt;SupportedCardsEnum&gt;) |  |  [optional] |
|**discountType** | [**DiscountTypeEnum**](#DiscountTypeEnum) |  |  [optional] |
|**discountValue** | **BigDecimal** |  |  [optional] |
|**discountAmount** | **BigDecimal** |  |  [optional] |
|**amountAfterDiscount** | **BigDecimal** |  |  [optional] |



## Enum: MethodEnum

| Name | Value |
|---- | -----|
| WALLET | &quot;WALLET&quot; |
| PAYME | &quot;PAYME&quot; |
| APPLE_PAY | &quot;APPLE_PAY&quot; |
| GOOGLE_PAY | &quot;GOOGLE_PAY&quot; |
| ONPAY | &quot;ONPAY&quot; |



## Enum: Set&lt;SupportedCardsEnum&gt;

| Name | Value |
|---- | -----|
| VISA | &quot;VISA&quot; |
| MASTERCARD | &quot;MASTERCARD&quot; |



## Enum: DiscountTypeEnum

| Name | Value |
|---- | -----|
| PERCENT | &quot;PERCENT&quot; |
| FIXED | &quot;FIXED&quot; |



