# UserInvoicesApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**redirectToInvoice**](UserInvoicesApi.md#redirectToInvoice) | **GET** /api/v1/user/invoices/{paymentIntentId} |  |


<a id="redirectToInvoice"></a>
# **redirectToInvoice**
> redirectToInvoice(paymentIntentId, principal)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.UserInvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    UserInvoicesApi apiInstance = new UserInvoicesApi(defaultClient);
    UUID paymentIntentId = UUID.randomUUID(); // UUID | 
    AuthenticatedPrincipal principal = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    try {
      apiInstance.redirectToInvoice(paymentIntentId, principal);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserInvoicesApi#redirectToInvoice");
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
| **paymentIntentId** | **UUID**|  | |
| **principal** | [**AuthenticatedPrincipal**](.md)|  | |

### Return type

null (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

