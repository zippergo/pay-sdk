# InternalWalletChargesApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**charge**](InternalWalletChargesApi.md#charge) | **POST** /api/v1/internal/wallet/charges | Spend credits from a user&#39;s wallet (synchronous) |


<a id="charge"></a>
# **charge**
> WalletChargeResponseDto charge(idempotencyKey, caller, walletChargeRequestDto)

Spend credits from a user&#39;s wallet (synchronous)

### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.InternalWalletChargesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InternalWalletChargesApi apiInstance = new InternalWalletChargesApi(defaultClient);
    String idempotencyKey = "idempotencyKey_example"; // String | 
    AuthenticatedPrincipal caller = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    WalletChargeRequestDto walletChargeRequestDto = new WalletChargeRequestDto(); // WalletChargeRequestDto | 
    try {
      WalletChargeResponseDto result = apiInstance.charge(idempotencyKey, caller, walletChargeRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InternalWalletChargesApi#charge");
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
| **walletChargeRequestDto** | [**WalletChargeRequestDto**](WalletChargeRequestDto.md)|  | |

### Return type

[**WalletChargeResponseDto**](WalletChargeResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

