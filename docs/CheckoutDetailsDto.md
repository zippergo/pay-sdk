

# CheckoutDetailsDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**moneyAmount** | **BigDecimal** |  |  [optional] |
|**moneyCurrency** | **String** |  |  [optional] |
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



