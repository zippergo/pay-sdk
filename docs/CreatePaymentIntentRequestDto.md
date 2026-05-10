

# CreatePaymentIntentRequestDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**userId** | **String** |  |  |
|**paymentMethods** | [**Set&lt;PaymentMethodsEnum&gt;**](#Set&lt;PaymentMethodsEnum&gt;) |  |  |
|**purpose** | [**PurposeEnum**](#PurposeEnum) |  |  |
|**moneyAmount** | **BigDecimal** |  |  |
|**moneyCurrency** | **String** |  |  |
|**creditCurrency** | **String** |  |  |
|**purposeRefType** | **String** |  |  [optional] |
|**purposeRefId** | **String** |  |  [optional] |
|**purposeDescription** | **String** |  |  [optional] |
|**callbackUrl** | **String** |  |  [optional] |
|**successUrl** | **String** |  |  [optional] |
|**cancelUrl** | **String** |  |  [optional] |
|**language** | **String** |  |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** |  |  [optional] |
|**buyerName** | **String** |  |  [optional] |
|**buyerEmail** | **String** |  |  [optional] |
|**buyerPhone** | **String** |  |  [optional] |
|**merchantName** | **String** |  |  [optional] |
|**merchantBrand** | [**MerchantBrandEnum**](#MerchantBrandEnum) |  |  [optional] |
|**merchantLogoUrl** | **String** |  |  [optional] |
|**subtotalAmount** | **BigDecimal** |  |  [optional] |
|**taxAmount** | **BigDecimal** |  |  [optional] |
|**discountAmount** | **BigDecimal** |  |  [optional] |
|**lineItems** | [**List&lt;LineItemRequestDto&gt;**](LineItemRequestDto.md) |  |  [optional] |



## Enum: Set&lt;PaymentMethodsEnum&gt;

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



## Enum: MerchantBrandEnum

| Name | Value |
|---- | -----|
| ZIPPER | &quot;ZIPPER&quot; |
| GENERIC | &quot;GENERIC&quot; |
| CUSTOM | &quot;CUSTOM&quot; |



