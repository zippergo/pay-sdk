

# SubscriptionPlanResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  [optional] |
|**code** | **String** |  |  [optional] |
|**displayName** | **String** |  |  [optional] |
|**description** | **String** |  |  [optional] |
|**amountCents** | **Long** |  |  [optional] |
|**currency** | **String** |  |  [optional] |
|**interval** | [**IntervalEnum**](#IntervalEnum) |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |



## Enum: IntervalEnum

| Name | Value |
|---- | -----|
| MONTHLY | &quot;MONTHLY&quot; |
| YEARLY | &quot;YEARLY&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;ACTIVE&quot; |
| ARCHIVED | &quot;ARCHIVED&quot; |



