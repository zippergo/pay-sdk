

# CheckoutDetailsDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**amount** | **BigDecimal** |  |  [optional] |
|**currency** | **String** |  |  [optional] |
|**language** | **String** |  |  [optional] |
|**methods** | [**List&lt;PaymentMethodOptionDto&gt;**](PaymentMethodOptionDto.md) |  |  [optional] |
|**selectedPaymentMethod** | [**SelectedPaymentMethodEnum**](#SelectedPaymentMethodEnum) |  |  [optional] |
|**paymentUrl** | **String** |  |  [optional] |
|**merchantSuccessUrl** | **String** |  |  [optional] |
|**merchantCancelUrl** | **String** |  |  [optional] |
|**expiresAt** | **OffsetDateTime** |  |  [optional] |
|**merchant** | [**MerchantInfoDto**](MerchantInfoDto.md) |  |  [optional] |
|**lineItems** | [**List&lt;LineItemDto&gt;**](LineItemDto.md) |  |  [optional] |
|**priceBreakdown** | [**PriceBreakdownDto**](PriceBreakdownDto.md) |  |  [optional] |
|**buyerEmail** | **String** |  |  [optional] |
|**purpose** | [**PurposeEnum**](#PurposeEnum) |  |  [optional] |



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



## Enum: SelectedPaymentMethodEnum

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



