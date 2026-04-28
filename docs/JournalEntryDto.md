

# JournalEntryDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Long** |  |  [optional] |
|**idempotencyKey** | **String** |  |  [optional] |
|**eventType** | [**EventTypeEnum**](#EventTypeEnum) |  |  [optional] |
|**currency** | **String** |  |  [optional] |
|**refType** | **String** |  |  [optional] |
|**refId** | **String** |  |  [optional] |
|**description** | **String** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**createdBy** | **String** |  |  [optional] |
|**postings** | [**List&lt;PostingLineDto&gt;**](PostingLineDto.md) |  |  [optional] |



## Enum: EventTypeEnum

| Name | Value |
|---- | -----|
| WALLET_TOPUP | &quot;WALLET_TOPUP&quot; |
| WALLET_SPEND | &quot;WALLET_SPEND&quot; |
| REFUND_TOPUP | &quot;REFUND_TOPUP&quot; |
| REFUND_SPEND | &quot;REFUND_SPEND&quot; |
| OPENING_BALANCE_FROM_LEGACY | &quot;OPENING_BALANCE_FROM_LEGACY&quot; |
| ADJUSTMENT_CREDIT | &quot;ADJUSTMENT_CREDIT&quot; |
| ADJUSTMENT_DEBIT | &quot;ADJUSTMENT_DEBIT&quot; |



