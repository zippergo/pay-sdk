

# AdminPaymentIntentRowDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  [optional] |
|**userId** | **String** |  |  [optional] |
|**buyerName** | **String** |  |  [optional] |
|**buyerEmail** | **String** |  |  [optional] |
|**purpose** | [**PurposeEnum**](#PurposeEnum) |  |  [optional] |
|**amount** | **BigDecimal** |  |  [optional] |
|**currency** | **String** |  |  [optional] |
|**selectedPaymentMethod** | [**SelectedPaymentMethodEnum**](#SelectedPaymentMethodEnum) |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**consumerService** | **String** |  |  [optional] |
|**parentIntentId** | **UUID** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |



## Enum: PurposeEnum

| Name | Value |
|---- | -----|
| WALLET_TOPUP | &quot;WALLET_TOPUP&quot; |
| PRODUCT_PURCHASE | &quot;PRODUCT_PURCHASE&quot; |
| SUBSCRIPTION_RENEWAL | &quot;SUBSCRIPTION_RENEWAL&quot; |
| REFUND_WALLET_TOPUP | &quot;REFUND_WALLET_TOPUP&quot; |
| REFUND_PRODUCT_PURCHASE | &quot;REFUND_PRODUCT_PURCHASE&quot; |
| REFUND_SUBSCRIPTION_RENEWAL | &quot;REFUND_SUBSCRIPTION_RENEWAL&quot; |



## Enum: SelectedPaymentMethodEnum

| Name | Value |
|---- | -----|
| WALLET | &quot;WALLET&quot; |
| PAYME | &quot;PAYME&quot; |
| APPLE_PAY | &quot;APPLE_PAY&quot; |
| GOOGLE_PAY | &quot;GOOGLE_PAY&quot; |
| ONPAY | &quot;ONPAY&quot; |



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



