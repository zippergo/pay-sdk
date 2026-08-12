# InternalExchangeRatesApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**list3**](InternalExchangeRatesApi.md#list3) | **GET** /api/v1/internal/exchange-rates |  |


<a id="list3"></a>
# **list3**
> List3200Response list3(from, to)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.InternalExchangeRatesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InternalExchangeRatesApi apiInstance = new InternalExchangeRatesApi(defaultClient);
    String from = "from_example"; // String | 
    String to = "to_example"; // String | 
    try {
      List3200Response result = apiInstance.list3(from, to);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InternalExchangeRatesApi#list3");
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
| **from** | **String**|  | |
| **to** | **String**|  | |

### Return type

[**List3200Response**](List3200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

