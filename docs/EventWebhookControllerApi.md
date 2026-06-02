# EventWebhookControllerApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**receive**](EventWebhookControllerApi.md#receive) | **POST** /api/v1/open/webhooks/events |  |


<a id="receive"></a>
# **receive**
> receive(body, xHmacSha256)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.EventWebhookControllerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    EventWebhookControllerApi apiInstance = new EventWebhookControllerApi(defaultClient);
    String body = "body_example"; // String | 
    String xHmacSha256 = "xHmacSha256_example"; // String | 
    try {
      apiInstance.receive(body, xHmacSha256);
    } catch (ApiException e) {
      System.err.println("Exception when calling EventWebhookControllerApi#receive");
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
| **body** | **String**|  | |
| **xHmacSha256** | **String**|  | [optional] |

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

