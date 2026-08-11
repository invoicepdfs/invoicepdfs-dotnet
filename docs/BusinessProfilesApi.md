# InvoicePDFs.Api.BusinessProfilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateBusinessProfile**](BusinessProfilesApi.md#createbusinessprofile) | **POST** /api/v1/business-profiles | Create Business Profile |
| [**DeleteBusinessProfile**](BusinessProfilesApi.md#deletebusinessprofile) | **DELETE** /api/v1/business-profiles/{business_profile_id} | Delete Business Profile |
| [**GetBusinessProfile**](BusinessProfilesApi.md#getbusinessprofile) | **GET** /api/v1/business-profiles/{business_profile_id} | Get Business Profile |
| [**ListBusinessProfiles**](BusinessProfilesApi.md#listbusinessprofiles) | **GET** /api/v1/business-profiles | List Business Profiles |
| [**UpdateBusinessProfile**](BusinessProfilesApi.md#updatebusinessprofile) | **PATCH** /api/v1/business-profiles/{business_profile_id} | Update Business Profile |

<a id="createbusinessprofile"></a>
# **CreateBusinessProfile**
> BusinessProfileResponse CreateBusinessProfile (BusinessProfileCreate businessProfileCreate, string? idempotencyKey = null)

Create Business Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateBusinessProfileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BusinessProfilesApi(config);
            var businessProfileCreate = new BusinessProfileCreate(); // BusinessProfileCreate | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Create Business Profile
                BusinessProfileResponse result = apiInstance.CreateBusinessProfile(businessProfileCreate, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessProfilesApi.CreateBusinessProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBusinessProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Business Profile
    ApiResponse<BusinessProfileResponse> response = apiInstance.CreateBusinessProfileWithHttpInfo(businessProfileCreate, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessProfilesApi.CreateBusinessProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **businessProfileCreate** | [**BusinessProfileCreate**](BusinessProfileCreate.md) |  |  |
| **idempotencyKey** | **string?** |  | [optional]  |

### Return type

[**BusinessProfileResponse**](BusinessProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletebusinessprofile"></a>
# **DeleteBusinessProfile**
> SimpleBoolResponse DeleteBusinessProfile (string businessProfileId)

Delete Business Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteBusinessProfileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BusinessProfilesApi(config);
            var businessProfileId = "businessProfileId_example";  // string | 

            try
            {
                // Delete Business Profile
                SimpleBoolResponse result = apiInstance.DeleteBusinessProfile(businessProfileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessProfilesApi.DeleteBusinessProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBusinessProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Business Profile
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteBusinessProfileWithHttpInfo(businessProfileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessProfilesApi.DeleteBusinessProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **businessProfileId** | **string** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbusinessprofile"></a>
# **GetBusinessProfile**
> BusinessProfileResponse GetBusinessProfile (string businessProfileId)

Get Business Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetBusinessProfileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BusinessProfilesApi(config);
            var businessProfileId = "businessProfileId_example";  // string | 

            try
            {
                // Get Business Profile
                BusinessProfileResponse result = apiInstance.GetBusinessProfile(businessProfileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessProfilesApi.GetBusinessProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Business Profile
    ApiResponse<BusinessProfileResponse> response = apiInstance.GetBusinessProfileWithHttpInfo(businessProfileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessProfilesApi.GetBusinessProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **businessProfileId** | **string** |  |  |

### Return type

[**BusinessProfileResponse**](BusinessProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listbusinessprofiles"></a>
# **ListBusinessProfiles**
> BusinessProfilesListResponse ListBusinessProfiles (int? limit = null, string? cursor = null)

List Business Profiles

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListBusinessProfilesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BusinessProfilesApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Business Profiles
                BusinessProfilesListResponse result = apiInstance.ListBusinessProfiles(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessProfilesApi.ListBusinessProfiles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBusinessProfilesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Business Profiles
    ApiResponse<BusinessProfilesListResponse> response = apiInstance.ListBusinessProfilesWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessProfilesApi.ListBusinessProfilesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** |  | [optional]  |

### Return type

[**BusinessProfilesListResponse**](BusinessProfilesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatebusinessprofile"></a>
# **UpdateBusinessProfile**
> BusinessProfileResponse UpdateBusinessProfile (string businessProfileId, BusinessProfilePatch businessProfilePatch, string? idempotencyKey = null)

Update Business Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UpdateBusinessProfileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BusinessProfilesApi(config);
            var businessProfileId = "businessProfileId_example";  // string | 
            var businessProfilePatch = new BusinessProfilePatch(); // BusinessProfilePatch | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Update Business Profile
                BusinessProfileResponse result = apiInstance.UpdateBusinessProfile(businessProfileId, businessProfilePatch, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessProfilesApi.UpdateBusinessProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBusinessProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Business Profile
    ApiResponse<BusinessProfileResponse> response = apiInstance.UpdateBusinessProfileWithHttpInfo(businessProfileId, businessProfilePatch, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessProfilesApi.UpdateBusinessProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **businessProfileId** | **string** |  |  |
| **businessProfilePatch** | [**BusinessProfilePatch**](BusinessProfilePatch.md) |  |  |
| **idempotencyKey** | **string?** |  | [optional]  |

### Return type

[**BusinessProfileResponse**](BusinessProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

