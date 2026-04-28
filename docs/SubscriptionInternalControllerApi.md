# SubscriptionInternalControllerApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**create**](SubscriptionInternalControllerApi.md#create) | **POST** /api/v1/internal/subscriptions |  |
| [**get2**](SubscriptionInternalControllerApi.md#get2) | **GET** /api/v1/internal/subscriptions/{id} |  |


<a id="create"></a>
# **create**
> SubscriptionResponseDto create(idempotencyKey, principal, createSubscriptionRequestDto)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.SubscriptionInternalControllerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SubscriptionInternalControllerApi apiInstance = new SubscriptionInternalControllerApi(defaultClient);
    String idempotencyKey = "idempotencyKey_example"; // String | 
    AuthenticatedPrincipal principal = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    CreateSubscriptionRequestDto createSubscriptionRequestDto = new CreateSubscriptionRequestDto(); // CreateSubscriptionRequestDto | 
    try {
      SubscriptionResponseDto result = apiInstance.create(idempotencyKey, principal, createSubscriptionRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionInternalControllerApi#create");
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
| **createSubscriptionRequestDto** | [**CreateSubscriptionRequestDto**](CreateSubscriptionRequestDto.md)|  | |

### Return type

[**SubscriptionResponseDto**](SubscriptionResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="get2"></a>
# **get2**
> SubscriptionResponseDto get2(id)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.SubscriptionInternalControllerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SubscriptionInternalControllerApi apiInstance = new SubscriptionInternalControllerApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      SubscriptionResponseDto result = apiInstance.get2(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionInternalControllerApi#get2");
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

[**SubscriptionResponseDto**](SubscriptionResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

