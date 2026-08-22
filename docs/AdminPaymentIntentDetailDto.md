

# AdminPaymentIntentDetailDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  [optional] |
|**consumerService** | **String** |  |  [optional] |
|**userId** | **String** |  |  [optional] |
|**idempotencyKey** | **String** |  |  [optional] |
|**parentIntentId** | **UUID** |  |  [optional] |
|**paymentMethods** | [**Set&lt;PaymentMethodsEnum&gt;**](#Set&lt;PaymentMethodsEnum&gt;) |  |  [optional] |
|**selectedPaymentMethod** | [**SelectedPaymentMethodEnum**](#SelectedPaymentMethodEnum) |  |  [optional] |
|**purpose** | [**PurposeEnum**](#PurposeEnum) |  |  [optional] |
|**amount** | **BigDecimal** |  |  [optional] |
|**baseAmount** | **BigDecimal** |  |  [optional] |
|**methodDiscountAmount** | **BigDecimal** |  |  [optional] |
|**currency** | **String** |  |  [optional] |
|**subtotalAmount** | **BigDecimal** |  |  [optional] |
|**taxAmount** | **BigDecimal** |  |  [optional] |
|**discountAmount** | **BigDecimal** |  |  [optional] |
|**feeAmount** | **BigDecimal** |  |  [optional] |
|**conversionRateId** | **Long** |  |  [optional] |
|**appliedRate** | **BigDecimal** |  |  [optional] |
|**providerRef** | **String** |  |  [optional] |
|**paymentUrl** | **String** |  |  [optional] |
|**successUrl** | **String** |  |  [optional] |
|**cancelUrl** | **String** |  |  [optional] |
|**failureUrl** | **String** |  |  [optional] |
|**callbackUrl** | **String** |  |  [optional] |
|**purposeRefType** | **String** |  |  [optional] |
|**purposeRefId** | **String** |  |  [optional] |
|**purposeDescription** | **String** |  |  [optional] |
|**language** | **String** |  |  [optional] |
|**metadata** | **Map&lt;String, Object&gt;** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**failureCode** | **String** |  |  [optional] |
|**failureMessage** | **String** |  |  [optional] |
|**journalEntryId** | **Long** |  |  [optional] |
|**completedAt** | **OffsetDateTime** |  |  [optional] |
|**callbackDispatchedAt** | **OffsetDateTime** |  |  [optional] |
|**expiresAt** | **OffsetDateTime** |  |  [optional] |
|**subscriptionId** | **UUID** |  |  [optional] |
|**merchantName** | **String** |  |  [optional] |
|**merchantBrand** | [**MerchantBrandEnum**](#MerchantBrandEnum) |  |  [optional] |
|**merchantLogoUrl** | **String** |  |  [optional] |
|**buyerName** | **String** |  |  [optional] |
|**buyerEmail** | **String** |  |  [optional] |
|**buyerPhone** | **String** |  |  [optional] |
|**embedded** | **Boolean** |  |  [optional] |
|**lineItems** | [**List&lt;AdminPaymentIntentLineItemDto&gt;**](AdminPaymentIntentLineItemDto.md) |  |  [optional] |
|**chain** | [**List&lt;AdminPaymentIntentChainNodeDto&gt;**](AdminPaymentIntentChainNodeDto.md) |  |  [optional] |
|**refundedAmount** | **BigDecimal** |  |  [optional] |
|**remainingRefundable** | **BigDecimal** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**createdBy** | **String** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |
|**updatedBy** | **String** |  |  [optional] |



## Enum: Set&lt;PaymentMethodsEnum&gt;

| Name | Value |
|---- | -----|
| WALLET | &quot;WALLET&quot; |
| PAYME | &quot;PAYME&quot; |
| APPLE_PAY | &quot;APPLE_PAY&quot; |
| GOOGLE_PAY | &quot;GOOGLE_PAY&quot; |
| ONPAY | &quot;ONPAY&quot; |



## Enum: SelectedPaymentMethodEnum

| Name | Value |
|---- | -----|
| WALLET | &quot;WALLET&quot; |
| PAYME | &quot;PAYME&quot; |
| APPLE_PAY | &quot;APPLE_PAY&quot; |
| GOOGLE_PAY | &quot;GOOGLE_PAY&quot; |
| ONPAY | &quot;ONPAY&quot; |



## Enum: PurposeEnum

| Name | Value |
|---- | -----|
| WALLET_TOPUP | &quot;WALLET_TOPUP&quot; |
| PRODUCT_PURCHASE | &quot;PRODUCT_PURCHASE&quot; |
| SUBSCRIPTION_RENEWAL | &quot;SUBSCRIPTION_RENEWAL&quot; |
| REFUND_WALLET_TOPUP | &quot;REFUND_WALLET_TOPUP&quot; |
| REFUND_PRODUCT_PURCHASE | &quot;REFUND_PRODUCT_PURCHASE&quot; |
| REFUND_SUBSCRIPTION_RENEWAL | &quot;REFUND_SUBSCRIPTION_RENEWAL&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;PENDING&quot; |
| AWAITING_METHOD_SELECTION | &quot;AWAITING_METHOD_SELECTION&quot; |
| AWAITING_PAYMENT | &quot;AWAITING_PAYMENT&quot; |
| COMPLETED | &quot;COMPLETED&quot; |
| FAILED | &quot;FAILED&quot; |
| EXPIRED | &quot;EXPIRED&quot; |
| REFUNDED | &quot;REFUNDED&quot; |
| PARTIALLY_REFUNDED | &quot;PARTIALLY_REFUNDED&quot; |



## Enum: MerchantBrandEnum

| Name | Value |
|---- | -----|
| ZIPPER | &quot;ZIPPER&quot; |
| GENERIC | &quot;GENERIC&quot; |
| CUSTOM | &quot;CUSTOM&quot; |



