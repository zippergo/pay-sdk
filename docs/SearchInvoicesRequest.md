

# SearchInvoicesRequest

Search request for issued invoices, with filtering, sorting, and pagination. **Query Fields** (full-text search): invoice id, payment intent id, `providerDocId` — the ids are cast to text so a fragment copied off a truncated column still matches. **Available Filter/Sort Fields:** - `id` (Long, sortable) - `status` (PENDING | ISSUED | FAILED, sortable) - `docType` (RECEIPT | INVOICE | INVRECEIPT | CREDIT_INVOICE, sortable) - `provider` (String) - `language` (String) - `retryCount` (sortable; EQ/IN filters also work — the framework has no concept of a   sort-only field — but no filter UI is wired to it) - `issuedAt` (Instant, sortable) - `createdAt` (Instant, sortable) - `nextRetryAt` (Instant) - `paymentIntentId` (UUID, joined — filterable but not sortable) 

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**query** | **String** | Full-text search query string. Matches against predefined query fields using case-insensitive LIKE. |  [optional] |
|**filters** | **Map&lt;String, List&lt;Filter&gt;&gt;** | Filter groups with AND/OR logic. Each group contains a list of filter criteria that are combined using the specified operator. |  [optional] |
|**sort** | [**List&lt;SortField&gt;**](SortField.md) | Sort criteria applied in order. Only sortable fields are accepted. |  [optional] |
|**pagination** | [**Pagination**](Pagination.md) | Pagination parameters. Page numbers are 1-based. |  [optional] |



