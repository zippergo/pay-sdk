

# AdminInvoiceDetailDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Long** |  |  [optional] |
|**paymentIntentId** | **UUID** |  |  [optional] |
|**docType** | [**DocTypeEnum**](#DocTypeEnum) |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**provider** | **String** |  |  [optional] |
|**language** | **String** |  |  [optional] |
|**retryCount** | **Integer** |  |  [optional] |
|**nextRetryAt** | **OffsetDateTime** |  |  [optional] |
|**providerDocId** | **String** |  |  [optional] |
|**docUrl** | **String** |  |  [optional] |
|**docCopyUrl** | **String** |  |  [optional] |
|**requestPayload** | **Map&lt;String, Object&gt;** |  |  [optional] |
|**responsePayload** | **Map&lt;String, Object&gt;** |  |  [optional] |
|**lastError** | **String** |  |  [optional] |
|**issuedAt** | **OffsetDateTime** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**createdBy** | **String** |  |  [optional] |
|**updatedAt** | **OffsetDateTime** |  |  [optional] |
|**updatedBy** | **String** |  |  [optional] |



## Enum: DocTypeEnum

| Name | Value |
|---- | -----|
| RECEIPT | &quot;RECEIPT&quot; |
| INVOICE | &quot;INVOICE&quot; |
| INVRECEIPT | &quot;INVRECEIPT&quot; |
| CREDIT_INVOICE | &quot;CREDIT_INVOICE&quot; |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;PENDING&quot; |
| ISSUED | &quot;ISSUED&quot; |
| FAILED | &quot;FAILED&quot; |



