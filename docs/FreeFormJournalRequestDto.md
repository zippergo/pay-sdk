

# FreeFormJournalRequestDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**eventType** | [**EventTypeEnum**](#EventTypeEnum) |  |  |
|**currency** | **String** |  |  |
|**refType** | **String** |  |  [optional] |
|**refId** | **String** |  |  [optional] |
|**description** | **String** |  |  [optional] |
|**postings** | [**List&lt;PostingLineDto&gt;**](PostingLineDto.md) |  |  |



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



