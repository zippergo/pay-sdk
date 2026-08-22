

# AdminInvoiceRowDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **Long** |  |  [optional] |
|**paymentIntentId** | **UUID** |  |  [optional] |
|**docType** | [**DocTypeEnum**](#DocTypeEnum) |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**provider** | **String** |  |  [optional] |
|**retryCount** | **Integer** |  |  [optional] |
|**providerDocId** | **String** |  |  [optional] |
|**issuedAt** | **OffsetDateTime** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |



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



