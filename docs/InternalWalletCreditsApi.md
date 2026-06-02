# InternalWalletCreditsApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**credit**](InternalWalletCreditsApi.md#credit) | **POST** /api/v1/internal/wallet/credits | Add credits to a user&#39;s wallet (idempotent) |


<a id="credit"></a>
# **credit**
> WalletCreditResponseDto credit(idempotencyKey, caller, walletCreditRequestDto)

Add credits to a user&#39;s wallet (idempotent)

### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.InternalWalletCreditsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InternalWalletCreditsApi apiInstance = new InternalWalletCreditsApi(defaultClient);
    String idempotencyKey = "idempotencyKey_example"; // String | 
    AuthenticatedPrincipal caller = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    WalletCreditRequestDto walletCreditRequestDto = new WalletCreditRequestDto(); // WalletCreditRequestDto | 
    try {
      WalletCreditResponseDto result = apiInstance.credit(idempotencyKey, caller, walletCreditRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InternalWalletCreditsApi#credit");
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
| **idempotencyKey** | **String**|  | |
| **caller** | [**AuthenticatedPrincipal**](.md)|  | |
| **walletCreditRequestDto** | [**WalletCreditRequestDto**](WalletCreditRequestDto.md)|  | |

### Return type

[**WalletCreditResponseDto**](WalletCreditResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

