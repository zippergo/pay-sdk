# SubscriptionPlanInternalControllerApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**callList**](SubscriptionPlanInternalControllerApi.md#callList) | **GET** /api/v1/internal/subscription-plans |  |
| [**create1**](SubscriptionPlanInternalControllerApi.md#create1) | **POST** /api/v1/internal/subscription-plans |  |
| [**get**](SubscriptionPlanInternalControllerApi.md#get) | **GET** /api/v1/internal/subscription-plans/{id} |  |
| [**update**](SubscriptionPlanInternalControllerApi.md#update) | **PATCH** /api/v1/internal/subscription-plans/{id} |  |


<a id="callList"></a>
# **callList**
> List&lt;SubscriptionPlanResponseDto&gt; callList(pageable, principal)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.SubscriptionPlanInternalControllerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SubscriptionPlanInternalControllerApi apiInstance = new SubscriptionPlanInternalControllerApi(defaultClient);
    Pageable pageable = new Pageable(); // Pageable | 
    AuthenticatedPrincipal principal = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    try {
      List<SubscriptionPlanResponseDto> result = apiInstance.callList(pageable, principal);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionPlanInternalControllerApi#callList");
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
| **pageable** | [**Pageable**](.md)|  | |
| **principal** | [**AuthenticatedPrincipal**](.md)|  | |

### Return type

[**List&lt;SubscriptionPlanResponseDto&gt;**](SubscriptionPlanResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="create1"></a>
# **create1**
> SubscriptionPlanResponseDto create1(principal, createSubscriptionPlanRequestDto)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.SubscriptionPlanInternalControllerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SubscriptionPlanInternalControllerApi apiInstance = new SubscriptionPlanInternalControllerApi(defaultClient);
    AuthenticatedPrincipal principal = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    CreateSubscriptionPlanRequestDto createSubscriptionPlanRequestDto = new CreateSubscriptionPlanRequestDto(); // CreateSubscriptionPlanRequestDto | 
    try {
      SubscriptionPlanResponseDto result = apiInstance.create1(principal, createSubscriptionPlanRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionPlanInternalControllerApi#create1");
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
| **createSubscriptionPlanRequestDto** | [**CreateSubscriptionPlanRequestDto**](CreateSubscriptionPlanRequestDto.md)|  | |

### Return type

[**SubscriptionPlanResponseDto**](SubscriptionPlanResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="get"></a>
# **get**
> SubscriptionPlanResponseDto get(id)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.SubscriptionPlanInternalControllerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SubscriptionPlanInternalControllerApi apiInstance = new SubscriptionPlanInternalControllerApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    try {
      SubscriptionPlanResponseDto result = apiInstance.get(id);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionPlanInternalControllerApi#get");
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

[**SubscriptionPlanResponseDto**](SubscriptionPlanResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

<a id="update"></a>
# **update**
> SubscriptionPlanResponseDto update(id, updateSubscriptionPlanRequestDto)



### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.SubscriptionPlanInternalControllerApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    SubscriptionPlanInternalControllerApi apiInstance = new SubscriptionPlanInternalControllerApi(defaultClient);
    UUID id = UUID.randomUUID(); // UUID | 
    UpdateSubscriptionPlanRequestDto updateSubscriptionPlanRequestDto = new UpdateSubscriptionPlanRequestDto(); // UpdateSubscriptionPlanRequestDto | 
    try {
      SubscriptionPlanResponseDto result = apiInstance.update(id, updateSubscriptionPlanRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling SubscriptionPlanInternalControllerApi#update");
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
| **updateSubscriptionPlanRequestDto** | [**UpdateSubscriptionPlanRequestDto**](UpdateSubscriptionPlanRequestDto.md)|  | |

### Return type

[**SubscriptionPlanResponseDto**](SubscriptionPlanResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

