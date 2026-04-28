# AdminJournalApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getByRef**](AdminJournalApi.md#getByRef) | **GET** /api/v1/admin/journal/{refType}/{refId} |  |
| [**postFreeForm**](AdminJournalApi.md#postFreeForm) | **POST** /api/v1/admin/journal/adjustments |  |


<a id="getByRef"></a>
# **getByRef**
> JournalEntryTreeDto getByRef(refType, refId)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminJournalApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminJournalApi apiInstance = new AdminJournalApi(defaultClient);
    String refType = "refType_example"; // String | 
    String refId = "refId_example"; // String | 
    try {
      JournalEntryTreeDto result = apiInstance.getByRef(refType, refId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminJournalApi#getByRef");
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
| **refType** | **String**|  | |
| **refId** | **String**|  | |

### Return type

[**JournalEntryTreeDto**](JournalEntryTreeDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="postFreeForm"></a>
# **postFreeForm**
> JournalEntryDto postFreeForm(principal, freeFormJournalRequestDto)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.AdminJournalApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    AdminJournalApi apiInstance = new AdminJournalApi(defaultClient);
    AuthenticatedPrincipal principal = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    FreeFormJournalRequestDto freeFormJournalRequestDto = new FreeFormJournalRequestDto(); // FreeFormJournalRequestDto | 
    try {
      JournalEntryDto result = apiInstance.postFreeForm(principal, freeFormJournalRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AdminJournalApi#postFreeForm");
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
| **principal** | [**AuthenticatedPrincipal**](.md)|  | |
| **freeFormJournalRequestDto** | [**FreeFormJournalRequestDto**](FreeFormJournalRequestDto.md)|  | |

### Return type

[**JournalEntryDto**](JournalEntryDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

