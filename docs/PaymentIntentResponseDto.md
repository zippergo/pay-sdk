

# PaymentIntentResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**paymentMethods** | [**Set&lt;PaymentMethodsEnum&gt;**](#Set&lt;PaymentMethodsEnum&gt;) |  |  [optional] |
|**selectedPaymentMethod** | [**SelectedPaymentMethodEnum**](#SelectedPaymentMethodEnum) |  |  [optional] |
|**paymentUrl** | **String** |  |  [optional] |
|**checkoutUrl** | **String** |  |  [optional] |
|**providerRef** | **String** |  |  [optional] |
|**amount** | **BigDecimal** |  |  [optional] |
|**currency** | **String** |  |  [optional] |
|**appliedRate** | **BigDecimal** |  |  [optional] |
|**feeAmount** | **BigDecimal** |  |  [optional] |
|**expiresAt** | **OffsetDateTime** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |



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



## Enum: Set&lt;PaymentMethodsEnum&gt;

| Name | Value |
|---- | -----|
| WALLET | &quot;WALLET&quot; |
| PAYME | &quot;PAYME&quot; |
| APPLE_PAY | &quot;APPLE_PAY&quot; |
| GOOGLE_PAY | &quot;GOOGLE_PAY&quot; |



## Enum: SelectedPaymentMethodEnum

| Name | Value |
|---- | -----|
| WALLET | &quot;WALLET&quot; |
| PAYME | &quot;PAYME&quot; |
| APPLE_PAY | &quot;APPLE_PAY&quot; |
| GOOGLE_PAY | &quot;GOOGLE_PAY&quot; |



