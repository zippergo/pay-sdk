# AdminWalletsApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**credit**](AdminWalletsApi.md#credit) | **POST** /api/v1/admin/wallets/{userId}/{currency}/credit |  |
| [**debit**](AdminWalletsApi.md#debit) | **POST** /api/v1/admin/wallets/{userId}/{currency}/debit |  |
| [**listWallets**](AdminWalletsApi.md#listWallets) | **GET** /api/v1/admin/wallets/{userId} |  |


<a id="credit"></a>
# **credit**
> AdminAdjustmentResponseDto credit(userId, currency, principal, adminCreditRequestDto)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminWalletsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminWalletsApi apiInstance = new AdminWalletsApi(defaultClient);
    String userId = "userId_example"; // String | 
    String currency = "currency_example"; // String | 
    AuthenticatedPrincipal principal = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    AdminCreditRequestDto adminCreditRequestDto = new AdminCreditRequestDto(); // AdminCreditRequestDto | 
    try {
      AdminAdjustmentResponseDto result = apiInstance.credit(userId, currency, principal, adminCreditRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminWalletsApi#credit");
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
| **userId** | **String**|  | |
| **currency** | **String**|  | |
| **principal** | [**AuthenticatedPrincipal**](.md)|  | |
| **adminCreditRequestDto** | [**AdminCreditRequestDto**](AdminCreditRequestDto.md)|  | |

### Return type

[**AdminAdjustmentResponseDto**](AdminAdjustmentResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="debit"></a>
# **debit**
> AdminAdjustmentResponseDto debit(userId, currency, principal, adminDebitRequestDto)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminWalletsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminWalletsApi apiInstance = new AdminWalletsApi(defaultClient);
    String userId = "userId_example"; // String | 
    String currency = "currency_example"; // String | 
    AuthenticatedPrincipal principal = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    AdminDebitRequestDto adminDebitRequestDto = new AdminDebitRequestDto(); // AdminDebitRequestDto | 
    try {
      AdminAdjustmentResponseDto result = apiInstance.debit(userId, currency, principal, adminDebitRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminWalletsApi#debit");
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
| **userId** | **String**|  | |
| **currency** | **String**|  | |
| **principal** | [**AuthenticatedPrincipal**](.md)|  | |
| **adminDebitRequestDto** | [**AdminDebitRequestDto**](AdminDebitRequestDto.md)|  | |

### Return type

[**AdminAdjustmentResponseDto**](AdminAdjustmentResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="listWallets"></a>
# **listWallets**
> List&lt;WalletDto&gt; listWallets(userId)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminWalletsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminWalletsApi apiInstance = new AdminWalletsApi(defaultClient);
    String userId = "userId_example"; // String | 
    try {
      List<WalletDto> result = apiInstance.listWallets(userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminWalletsApi#listWallets");
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
| **userId** | **String**|  | |

### Return type

[**List&lt;WalletDto&gt;**](WalletDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

