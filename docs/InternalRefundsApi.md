# InternalRefundsApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**refundPaymentIntent**](InternalRefundsApi.md#refundPaymentIntent) | **POST** /api/v1/internal/payment-intents/{intentId}/refunds |  |
| [**refundWalletCharge**](InternalRefundsApi.md#refundWalletCharge) | **POST** /api/v1/internal/wallet/charges/{chargeId}/refunds |  |


<a id="refundPaymentIntent"></a>
# **refundPaymentIntent**
> RefundResponseDto refundPaymentIntent(intentId, idempotencyKey, principal, refundRequestDto)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.InternalRefundsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InternalRefundsApi apiInstance = new InternalRefundsApi(defaultClient);
    UUID intentId = UUID.randomUUID(); // UUID | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    AuthenticatedPrincipal principal = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    RefundRequestDto refundRequestDto = new RefundRequestDto(); // RefundRequestDto | 
    try {
      RefundResponseDto result = apiInstance.refundPaymentIntent(intentId, idempotencyKey, principal, refundRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InternalRefundsApi#refundPaymentIntent");
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
| **intentId** | **UUID**|  | |
| **idempotencyKey** | **String**|  | |
| **principal** | [**AuthenticatedPrincipal**](.md)|  | |
| **refundRequestDto** | [**RefundRequestDto**](RefundRequestDto.md)|  | |

### Return type

[**RefundResponseDto**](RefundResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="refundWalletCharge"></a>
# **refundWalletCharge**
> RefundResponseDto refundWalletCharge(chargeId, idempotencyKey, principal, refundRequestDto)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.InternalRefundsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InternalRefundsApi apiInstance = new InternalRefundsApi(defaultClient);
    UUID chargeId = UUID.randomUUID(); // UUID | 
    String idempotencyKey = "idempotencyKey_example"; // String | 
    AuthenticatedPrincipal principal = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    RefundRequestDto refundRequestDto = new RefundRequestDto(); // RefundRequestDto | 
    try {
      RefundResponseDto result = apiInstance.refundWalletCharge(chargeId, idempotencyKey, principal, refundRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InternalRefundsApi#refundWalletCharge");
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
| **chargeId** | **UUID**|  | |
| **idempotencyKey** | **String**|  | |
| **principal** | [**AuthenticatedPrincipal**](.md)|  | |
| **refundRequestDto** | [**RefundRequestDto**](RefundRequestDto.md)|  | |

### Return type

[**RefundResponseDto**](RefundResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

