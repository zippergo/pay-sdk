# PaymentIntentInternalControllerApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**create2**](PaymentIntentInternalControllerApi.md#create2) | **POST** /api/v1/internal/payment-intents |  |
| [**get3**](PaymentIntentInternalControllerApi.md#get3) | **GET** /api/v1/internal/payment-intents/{id} |  |


<a id="create2"></a>
# **create2**
> PaymentIntentResponseDto create2(idempotencyKey, principal, createPaymentIntentRequestDto)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.PaymentIntentInternalControllerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PaymentIntentInternalControllerApi apiInstance = new PaymentIntentInternalControllerApi(defaultClient);
    String idempotencyKey = "idempotencyKey_example"; // String | 
    AuthenticatedPrincipal principal = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    CreatePaymentIntentRequestDto createPaymentIntentRequestDto = new CreatePaymentIntentRequestDto(); // CreatePaymentIntentRequestDto | 
    try {
      PaymentIntentResponseDto result = apiInstance.create2(idempotencyKey, principal, createPaymentIntentRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentIntentInternalControllerApi#create2");
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
| **principal** | [**AuthenticatedPrincipal**](.md)|  | |
| **createPaymentIntentRequestDto** | [**CreatePaymentIntentRequestDto**](CreatePaymentIntentRequestDto.md)|  | |

### Return type

[**PaymentIntentResponseDto**](PaymentIntentResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="get3"></a>
# **get3**
> PaymentIntentResponseDto get3(id)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.PaymentIntentInternalControllerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    PaymentIntentInternalControllerApi apiInstance = new PaymentIntentInternalControllerApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      PaymentIntentResponseDto result = apiInstance.get3(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentIntentInternalControllerApi#get3");
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

