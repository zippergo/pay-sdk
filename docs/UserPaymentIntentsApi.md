# UserPaymentIntentsApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**get1**](UserPaymentIntentsApi.md#get1) | **GET** /api/v1/user/payment-intents/{id} |  |


<a id="get1"></a>
# **get1**
> PaymentIntentResponseDto get1(id, principal)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.UserPaymentIntentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserPaymentIntentsApi apiInstance = new UserPaymentIntentsApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    AuthenticatedPrincipal principal = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    try {
      PaymentIntentResponseDto result = apiInstance.get1(id, principal);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserPaymentIntentsApi#get1");
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
| **id** | **UUID**|  | |
| **principal** | [**AuthenticatedPrincipal**](.md)|  | |

### Return type

[**PaymentIntentResponseDto**](PaymentIntentResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

