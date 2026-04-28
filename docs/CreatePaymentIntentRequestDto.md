

# CreatePaymentIntentRequestDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**userId** | **String** |  |  |
|**paymentMethod** | [**PaymentMethodEnum**](#PaymentMethodEnum) |  |  |
|**purpose** | [**PurposeEnum**](#PurposeEnum) |  |  |
|**moneyAmount** | **BigDecimal** |  |  |
|**moneyCurrency** | **String** |  |  |
|**creditCurrency** | **String** |  |  |
|**purposeRefType** | **String** |  |  [optional] |
|**purposeRefId** | **String** |  |  [optional] |
|**purposeDescription** | **String** |  |  [optional] |
|**notifyUrl** | **String** |  |  [optional] |
|**returnUrl** | **String** |  |  [optional] |
|**language** | **String** |  |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** |  |  [optional] |
|**buyerName** | **String** |  |  [optional] |
|**buyerEmail** | **String** |  |  [optional] |



## Enum: PaymentMethodEnum

| Name | Value |
|---- | -----|
| WALLET | &quot;WALLET&quot; |
| PAYME | &quot;PAYME&quot; |



## Enum: PurposeEnum

| Name | Value |
|---- | -----|
| WALLET_TOPUP | &quot;WALLET_TOPUP&quot; |
| PRODUCT_PURCHASE | &quot;PRODUCT_PURCHASE&quot; |
| SUBSCRIPTION_RENEWAL | &quot;SUBSCRIPTION_RENEWAL&quot; |
| REFUND_WALLET_TOPUP | &quot;REFUND_WALLET_TOPUP&quot; |
| REFUND_PRODUCT_PURCHASE | &quot;REFUND_PRODUCT_PURCHASE&quot; |
| REFUND_SUBSCRIPTION_RENEWAL | &quot;REFUND_SUBSCRIPTION_RENEWAL&quot; |



