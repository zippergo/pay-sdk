# InternalUsersApi

All URIs are relative to *http://localhost:8089*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**onboard**](InternalUsersApi.md#onboard) | **POST** /api/v1/internal/users/onboard | Register a user and provision wallets in all active credit currencies |


<a id="onboard"></a>
# **onboard**
> OnboardUserResponseDto onboard(caller, onboardUserRequestDto)

Register a user and provision wallets in all active credit currencies

### Example
```java
// Import classes:
import com.zipper.pay.sdk.ApiClient;
import com.zipper.pay.sdk.ApiException;
import com.zipper.pay.sdk.Configuration;
import com.zipper.pay.sdk.auth.*;
import com.zipper.pay.sdk.models.*;
import com.zipper.pay.sdk.api.InternalUsersApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost:8089");
    
    // Configure HTTP bearer authorization: bearerAuth
    HttpBearerAuth bearerAuth = (HttpBearerAuth) defaultClient.getAuthentication("bearerAuth");
    bearerAuth.setBearerToken("BEARER TOKEN");

    InternalUsersApi apiInstance = new InternalUsersApi(defaultClient);
    AuthenticatedPrincipal caller = new AuthenticatedPrincipal(); // AuthenticatedPrincipal | 
    OnboardUserRequestDto onboardUserRequestDto = new OnboardUserRequestDto(); // OnboardUserRequestDto | 
    try {
      OnboardUserResponseDto result = apiInstance.onboard(caller, onboardUserRequestDto);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InternalUsersApi#onboard");
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
| **caller** | [**AuthenticatedPrincipal**](.md)|  | |
| **onboardUserRequestDto** | [**OnboardUserRequestDto**](OnboardUserRequestDto.md)|  | |

### Return type

[**OnboardUserResponseDto**](OnboardUserResponseDto.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | OK |  -  |

