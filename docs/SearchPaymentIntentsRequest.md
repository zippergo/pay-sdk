

# SearchPaymentIntentsRequest

Search request for payment intents, with filtering, sorting, and pagination. **Query Fields** (full-text search): intent id, `buyerName`, `buyerEmail`, `providerRef`, `userId` — the id is cast to text so a fragment copied off a truncated column still matches. **Available Filter/Sort Fields:** - `status` (PENDING | AWAITING_METHOD_SELECTION | AWAITING_PAYMENT | COMPLETED | FAILED |   EXPIRED | REFUNDED | PARTIALLY_REFUNDED, sortable) - `purpose` (WALLET_TOPUP | PRODUCT_PURCHASE | SUBSCRIPTION_RENEWAL | REFUND_WALLET_TOPUP |   REFUND_PRODUCT_PURCHASE | REFUND_SUBSCRIPTION_RENEWAL, sortable) - `selectedPaymentMethod` (WALLET | PAYME | APPLE_PAY | GOOGLE_PAY, sortable) - `consumerService` (String, sortable) - `userId` (String, sortable) - `buyerEmail` (String) - `currency` (String, sortable) - `amount` (BigDecimal, sortable) - `createdAt` (Instant, sortable) — the default sort is `createdAt DESC` - `completedAt` (Instant, sortable) - `expiresAt` (Instant) - `parentIntentId` (UUID) — set on refund intents; filter on it to list one intent's refunds  `id` is deliberately absent: sorting UUIDs is meaningless and free-text already finds one. 

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**query** | **String** | Full-text search query string. Matches against predefined query fields using case-insensitive LIKE. |  [optional] |
|**filters** | **Map&lt;String, List&lt;Filter&gt;&gt;** | Filter groups with AND/OR logic. Each group contains a list of filter criteria that are combined using the specified operator. |  [optional] |
|**sort** | [**List&lt;SortField&gt;**](SortField.md) | Sort criteria applied in order. Only sortable fields are accepted. |  [optional] |
|**pagination** | [**Pagination**](Pagination.md) | Pagination parameters. Page numbers are 1-based. |  [optional] |



