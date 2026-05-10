# CheckoutOpenControllerApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getCheckout**](CheckoutOpenControllerApi.md#getCheckout) | **GET** /api/v1/open/checkout/{id} |  |
| [**getStatus**](CheckoutOpenControllerApi.md#getStatus) | **GET** /api/v1/open/checkout/{id}/status |  |
| [**selectMethod**](CheckoutOpenControllerApi.md#selectMethod) | **POST** /api/v1/open/checkout/{id}/select-method |  |


<a id="getCheckout"></a>
# **getCheckout**
> CheckoutDetailsDto getCheckout(id)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.CheckoutOpenControllerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CheckoutOpenControllerApi apiInstance = new CheckoutOpenControllerApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      CheckoutDetailsDto result = apiInstance.getCheckout(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutOpenControllerApi#getCheckout");
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

[**CheckoutDetailsDto**](CheckoutDetailsDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="getStatus"></a>
# **getStatus**
> CheckoutStatusDto getStatus(id)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.CheckoutOpenControllerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CheckoutOpenControllerApi apiInstance = new CheckoutOpenControllerApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      CheckoutStatusDto result = apiInstance.getStatus(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutOpenControllerApi#getStatus");
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

[**CheckoutStatusDto**](CheckoutStatusDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="selectMethod"></a>
# **selectMethod**
> SelectMethodResponseDto selectMethod(id, selectMethodRequestDto)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.CheckoutOpenControllerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    CheckoutOpenControllerApi apiInstance = new CheckoutOpenControllerApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    SelectMethodRequestDto selectMethodRequestDto = new SelectMethodRequestDto(); // SelectMethodRequestDto | 
    try {
      SelectMethodResponseDto result = apiInstance.selectMethod(id, selectMethodRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CheckoutOpenControllerApi#selectMethod");
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
| **selectMethodRequestDto** | [**SelectMethodRequestDto**](SelectMethodRequestDto.md)|  | |

### Return type

[**SelectMethodResponseDto**](SelectMethodResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

