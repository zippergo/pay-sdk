

# RefundResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**refundIntentId** | **UUID** |  |  [optional] |
|**parentIntentId** | **UUID** |  |  [optional] |
|**refundStatus** | [**RefundStatusEnum**](#RefundStatusEnum) |  |  [optional] |
|**parentStatus** | [**ParentStatusEnum**](#ParentStatusEnum) |  |  [optional] |
|**refundedAmount** | **BigDecimal** |  |  [optional] |
|**cumulativeRefunded** | **BigDecimal** |  |  [optional] |
|**journalEntryId** | **Long** |  |  [optional] |
|**completedAt** | **OffsetDateTime** |  |  [optional] |
|**providerRefundRef** | **String** |  |  [optional] |



## Enum: RefundStatusEnum

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



## Enum: ParentStatusEnum

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



