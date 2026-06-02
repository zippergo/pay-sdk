

# WalletCreditRequestDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**userId** | **String** |  |  |
|**currency** | **String** |  |  |
|**amount** | **BigDecimal** |  |  |
|**reasonCode** | [**ReasonCodeEnum**](#ReasonCodeEnum) |  |  |
|**note** | **String** |  |  [optional] |
|**issueInvoice** | **Boolean** |  |  [optional] |



## Enum: ReasonCodeEnum

| Name | Value |
|---- | -----|
| GOODWILL | &quot;GOODWILL&quot; |
| PROMOTION | &quot;PROMOTION&quot; |
| MANUAL_TOPUP | &quot;MANUAL_TOPUP&quot; |
| MIGRATION_FIX | &quot;MIGRATION_FIX&quot; |
| OTHER | &quot;OTHER&quot; |



