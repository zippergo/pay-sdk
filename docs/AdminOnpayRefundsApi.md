# AdminOnpayRefundsApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**adminSettleOnPayRefund**](AdminOnpayRefundsApi.md#adminSettleOnPayRefund) | **POST** /api/v1/admin/onpay-refunds/{refundIntentId}/settle | Settle an ON refund |


<a id="adminSettleOnPayRefund"></a>
# **adminSettleOnPayRefund**
> adminSettleOnPayRefund(refundIntentId)

Settle an ON refund

Confirms BTB moved the money out of band: flips the refund intent to COMPLETED and the parent to REFUNDED/PARTIALLY_REFUNDED. Admin only.

### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminOnpayRefundsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminOnpayRefundsApi apiInstance = new AdminOnpayRefundsApi(defaultClient);
    UUID refundIntentId = UUID.randomUUID(); // UUID | 
    try {
      apiInstance.adminSettleOnPayRefund(refundIntentId);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminOnpayRefundsApi#adminSettleOnPayRefund");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **refundIntentId** | **UUID**|  | |

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

