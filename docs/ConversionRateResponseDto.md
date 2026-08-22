

# ConversionRateResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Long** |  |  [optional] |
|**paymentMethod** | [**PaymentMethodEnum**](#PaymentMethodEnum) |  |  [optional] |
|**moneyCurrency** | **String** |  |  [optional] |
|**creditCurrency** | **String** |  |  [optional] |
|**rate** | **BigDecimal** |  |  [optional] |
|**feePercent** | **BigDecimal** |  |  [optional] |
|**feeFixed** | **BigDecimal** |  |  [optional] |
|**effectiveFrom** | **OffsetDateTime** |  |  [optional] |
|**effectiveTo** | **OffsetDateTime** |  |  [optional] |
|**createdBy** | **String** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |



## Enum: PaymentMethodEnum

| Name | Value |
|---- | -----|
| WALLET | &quot;WALLET&quot; |
| PAYME | &quot;PAYME&quot; |
| APPLE_PAY | &quot;APPLE_PAY&quot; |
| GOOGLE_PAY | &quot;GOOGLE_PAY&quot; |
| ONPAY | &quot;ONPAY&quot; |



