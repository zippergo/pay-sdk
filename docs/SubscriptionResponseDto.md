

# SubscriptionResponseDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  [optional] |
|**planId** | **UUID** |  |  [optional] |
|**userId** | **String** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**provider** | [**ProviderEnum**](#ProviderEnum) |  |  [optional] |
|**providerSubscriptionId** | **String** |  |  [optional] |
|**providerAuthorizationUrl** | **String** |  |  [optional] |
|**amountCents** | **Long** |  |  [optional] |
|**currency** | **String** |  |  [optional] |
|**interval** | [**IntervalEnum**](#IntervalEnum) |  |  [optional] |
|**currentPeriodStart** | **OffsetDateTime** |  |  [optional] |
|**currentPeriodEnd** | **OffsetDateTime** |  |  [optional] |
|**nextBillingAt** | **OffsetDateTime** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING_AUTHORIZATION | &quot;PENDING_AUTHORIZATION&quot; |
| ACTIVE | &quot;ACTIVE&quot; |
| PAST_DUE | &quot;PAST_DUE&quot; |
| PAUSED | &quot;PAUSED&quot; |
| CANCEL_AT_PERIOD_END | &quot;CANCEL_AT_PERIOD_END&quot; |
| CANCELED | &quot;CANCELED&quot; |
| EXPIRED | &quot;EXPIRED&quot; |



## Enum: ProviderEnum

| Name | Value |
|---- | -----|
| PAYME | &quot;PAYME&quot; |



## Enum: IntervalEnum

| Name | Value |
|---- | -----|
| MONTHLY | &quot;MONTHLY&quot; |
| YEARLY | &quot;YEARLY&quot; |



