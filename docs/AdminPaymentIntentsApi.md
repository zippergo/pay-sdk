# AdminPaymentIntentsApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**adminGetPaymentIntent**](AdminPaymentIntentsApi.md#adminGetPaymentIntent) | **GET** /api/v1/admin/payment-intents/{id} | Get one payment intent |
| [**adminSearchPaymentIntents**](AdminPaymentIntentsApi.md#adminSearchPaymentIntents) | **POST** /api/v1/admin/payment-intents/search | Search payment intents |


<a id="adminGetPaymentIntent"></a>
# **adminGetPaymentIntent**
> AdminPaymentIntentDetailDto adminGetPaymentIntent(id)

Get one payment intent

The full record, its line items and its refund chain.

### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminPaymentIntentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminPaymentIntentsApi apiInstance = new AdminPaymentIntentsApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      AdminPaymentIntentDetailDto result = apiInstance.adminGetPaymentIntent(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminPaymentIntentsApi#adminGetPaymentIntent");
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

[**AdminPaymentIntentDetailDto**](AdminPaymentIntentDetailDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="adminSearchPaymentIntents"></a>
# **adminSearchPaymentIntents**
> PageResponseListAdminPaymentIntentRowDto adminSearchPaymentIntents(searchPaymentIntentsRequest)

Search payment intents

Search, filter, sort and page payment intents. Admin only.

### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminPaymentIntentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminPaymentIntentsApi apiInstance = new AdminPaymentIntentsApi(defaultClient);
    SearchPaymentIntentsRequest searchPaymentIntentsRequest = new SearchPaymentIntentsRequest(); // SearchPaymentIntentsRequest | 
    try {
      PageResponseListAdminPaymentIntentRowDto result = apiInstance.adminSearchPaymentIntents(searchPaymentIntentsRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminPaymentIntentsApi#adminSearchPaymentIntents");
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
| **searchPaymentIntentsRequest** | [**SearchPaymentIntentsRequest**](SearchPaymentIntentsRequest.md)|  | |

### Return type

[**PageResponseListAdminPaymentIntentRowDto**](PageResponseListAdminPaymentIntentRowDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

