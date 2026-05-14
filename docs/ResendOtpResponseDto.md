

# ResendOtpResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**expiresAt** | **OffsetDateTime** |  |  [optional] |



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



