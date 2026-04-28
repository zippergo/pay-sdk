# AdminConsumerServicesApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**register**](AdminConsumerServicesApi.md#register) | **POST** /api/v1/admin/consumer-services |  |
| [**rotate**](AdminConsumerServicesApi.md#rotate) | **POST** /api/v1/admin/consumer-services/{clientId}/rotate-secret |  |


<a id="register"></a>
# **register**
> RegisterConsumerResponseDto register(registerConsumerRequestDto)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminConsumerServicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminConsumerServicesApi apiInstance = new AdminConsumerServicesApi(defaultClient);
    RegisterConsumerRequestDto registerConsumerRequestDto = new RegisterConsumerRequestDto(); // RegisterConsumerRequestDto | 
    try {
      RegisterConsumerResponseDto result = apiInstance.register(registerConsumerRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminConsumerServicesApi#register");
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
| **registerConsumerRequestDto** | [**RegisterConsumerRequestDto**](RegisterConsumerRequestDto.md)|  | |

### Return type

[**RegisterConsumerResponseDto**](RegisterConsumerResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="rotate"></a>
# **rotate**
> RotateSecretResponseDto rotate(clientId)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminConsumerServicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminConsumerServicesApi apiInstance = new AdminConsumerServicesApi(defaultClient);
    String clientId = "clientId_example"; // String | 
    try {
      RotateSecretResponseDto result = apiInstance.rotate(clientId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminConsumerServicesApi#rotate");
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
| **clientId** | **String**|  | |

### Return type

[**RotateSecretResponseDto**](RotateSecretResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

