# AdminInvoicesApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**adminGetInvoice**](AdminInvoicesApi.md#adminGetInvoice) | **GET** /api/v1/admin/invoices/{id} | Get one invoice |
| [**adminRetryInvoice**](AdminInvoicesApi.md#adminRetryInvoice) | **POST** /api/v1/admin/invoices/{id}/retry | Retry a failed issuance |
| [**adminSearchInvoices**](AdminInvoicesApi.md#adminSearchInvoices) | **POST** /api/v1/admin/invoices/search | Search invoices |


<a id="adminGetInvoice"></a>
# **adminGetInvoice**
> AdminInvoiceDetailDto adminGetInvoice(id)

Get one invoice

### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminInvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminInvoicesApi apiInstance = new AdminInvoicesApi(defaultClient);
    Long id = 56L; // Long | 
    try {
      AdminInvoiceDetailDto result = apiInstance.adminGetInvoice(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminInvoicesApi#adminGetInvoice");
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
| **id** | **Long**|  | |

### Return type

[**AdminInvoiceDetailDto**](AdminInvoiceDetailDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="adminRetryInvoice"></a>
# **adminRetryInvoice**
> AdminInvoiceDetailDto adminRetryInvoice(id)

Retry a failed issuance

Re-enqueues the ISSUE_INVOICE outbox message. Only FAILED invoices.

### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminInvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminInvoicesApi apiInstance = new AdminInvoicesApi(defaultClient);
    Long id = 56L; // Long | 
    try {
      AdminInvoiceDetailDto result = apiInstance.adminRetryInvoice(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminInvoicesApi#adminRetryInvoice");
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
| **id** | **Long**|  | |

### Return type

[**AdminInvoiceDetailDto**](AdminInvoiceDetailDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="adminSearchInvoices"></a>
# **adminSearchInvoices**
> PageResponseListAdminInvoiceRowDto adminSearchInvoices(searchInvoicesRequest)

Search invoices

Search, filter, sort and page issued documents. Admin only.

### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminInvoicesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminInvoicesApi apiInstance = new AdminInvoicesApi(defaultClient);
    SearchInvoicesRequest searchInvoicesRequest = new SearchInvoicesRequest(); // SearchInvoicesRequest | 
    try {
      PageResponseListAdminInvoiceRowDto result = apiInstance.adminSearchInvoices(searchInvoicesRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminInvoicesApi#adminSearchInvoices");
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
| **searchInvoicesRequest** | [**SearchInvoicesRequest**](SearchInvoicesRequest.md)|  | |

### Return type

[**PageResponseListAdminInvoiceRowDto**](PageResponseListAdminInvoiceRowDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

