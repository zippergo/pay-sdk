# AdminConversionRatesApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**insert**](AdminConversionRatesApi.md#insert) | **POST** /api/v1/admin/conversion-rates |  |
| [**list1**](AdminConversionRatesApi.md#list1) | **GET** /api/v1/admin/conversion-rates |  |


<a id="insert"></a>
# **insert**
> ConversionRateResponseDto insert(principal, conversionRateRequestDto)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminConversionRatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminConversionRatesApi apiInstance = new AdminConversionRatesApi(defaultClient);
    AuthenticatedPrincipal principal = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    ConversionRateRequestDto conversionRateRequestDto = new ConversionRateRequestDto(); // ConversionRateRequestDto | 
    try {
      ConversionRateResponseDto result = apiInstance.insert(principal, conversionRateRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminConversionRatesApi#insert");
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
| **principal** | [**AuthenticatedPrincipal**](.md)|  | |
| **conversionRateRequestDto** | [**ConversionRateRequestDto**](ConversionRateRequestDto.md)|  | |

### Return type

[**ConversionRateResponseDto**](ConversionRateResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="list1"></a>
# **list1**
> List&lt;ConversionRateResponseDto&gt; list1(paymentMethod, moneyCurrency, creditCurrency)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminConversionRatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminConversionRatesApi apiInstance = new AdminConversionRatesApi(defaultClient);
    String paymentMethod = "WALLET"; // String | 
    String moneyCurrency = "moneyCurrency_example"; // String | 
    String creditCurrency = "creditCurrency_example"; // String | 
    try {
      List<ConversionRateResponseDto> result = apiInstance.list1(paymentMethod, moneyCurrency, creditCurrency);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminConversionRatesApi#list1");
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
| **paymentMethod** | **String**|  | [optional] [enum: WALLET, PAYME] |
| **moneyCurrency** | **String**|  | [optional] |
| **creditCurrency** | **String**|  | [optional] |

### Return type

[**List&lt;ConversionRateResponseDto&gt;**](ConversionRateResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

