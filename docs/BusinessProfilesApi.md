# InvoicePDFs.Api.BusinessProfilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateBusinessProfileApiV1BusinessProfilesPost**](BusinessProfilesApi.md#createbusinessprofileapiv1businessprofilespost) | **POST** /api/v1/business-profiles | Create Business Profile |
| [**DeleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete**](BusinessProfilesApi.md#deletebusinessprofileapiv1businessprofilesbusinessprofileiddelete) | **DELETE** /api/v1/business-profiles/{business_profile_id} | Delete Business Profile |
| [**GetBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet**](BusinessProfilesApi.md#getbusinessprofileapiv1businessprofilesbusinessprofileidget) | **GET** /api/v1/business-profiles/{business_profile_id} | Get Business Profile |
| [**ListBusinessProfilesApiV1BusinessProfilesGet**](BusinessProfilesApi.md#listbusinessprofilesapiv1businessprofilesget) | **GET** /api/v1/business-profiles | List Business Profiles |
| [**PatchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch**](BusinessProfilesApi.md#patchbusinessprofileapiv1businessprofilesbusinessprofileidpatch) | **PATCH** /api/v1/business-profiles/{business_profile_id} | Patch Business Profile |

<a id="createbusinessprofileapiv1businessprofilespost"></a>
# **CreateBusinessProfileApiV1BusinessProfilesPost**
> BusinessProfileResponse CreateBusinessProfileApiV1BusinessProfilesPost (BusinessProfileCreate businessProfileCreate, string? idempotencyKey = null)

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
    public class CreateBusinessProfileApiV1BusinessProfilesPostExample
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
                BusinessProfileResponse result = apiInstance.CreateBusinessProfileApiV1BusinessProfilesPost(businessProfileCreate, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessProfilesApi.CreateBusinessProfileApiV1BusinessProfilesPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBusinessProfileApiV1BusinessProfilesPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Business Profile
    ApiResponse<BusinessProfileResponse> response = apiInstance.CreateBusinessProfileApiV1BusinessProfilesPostWithHttpInfo(businessProfileCreate, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessProfilesApi.CreateBusinessProfileApiV1BusinessProfilesPostWithHttpInfo: " + e.Message);
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

<a id="deletebusinessprofileapiv1businessprofilesbusinessprofileiddelete"></a>
# **DeleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete**
> SimpleBoolResponse DeleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete (string businessProfileId)

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
    public class DeleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDeleteExample
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
                SimpleBoolResponse result = apiInstance.DeleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete(businessProfileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessProfilesApi.DeleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Business Profile
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDeleteWithHttpInfo(businessProfileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessProfilesApi.DeleteBusinessProfileApiV1BusinessProfilesBusinessProfileIdDeleteWithHttpInfo: " + e.Message);
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

<a id="getbusinessprofileapiv1businessprofilesbusinessprofileidget"></a>
# **GetBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet**
> BusinessProfileResponse GetBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet (string businessProfileId)

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
    public class GetBusinessProfileApiV1BusinessProfilesBusinessProfileIdGetExample
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
                BusinessProfileResponse result = apiInstance.GetBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet(businessProfileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessProfilesApi.GetBusinessProfileApiV1BusinessProfilesBusinessProfileIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBusinessProfileApiV1BusinessProfilesBusinessProfileIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Business Profile
    ApiResponse<BusinessProfileResponse> response = apiInstance.GetBusinessProfileApiV1BusinessProfilesBusinessProfileIdGetWithHttpInfo(businessProfileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessProfilesApi.GetBusinessProfileApiV1BusinessProfilesBusinessProfileIdGetWithHttpInfo: " + e.Message);
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

<a id="listbusinessprofilesapiv1businessprofilesget"></a>
# **ListBusinessProfilesApiV1BusinessProfilesGet**
> BusinessProfilesListResponse ListBusinessProfilesApiV1BusinessProfilesGet (int? limit = null, string? cursor = null)

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
    public class ListBusinessProfilesApiV1BusinessProfilesGetExample
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
                BusinessProfilesListResponse result = apiInstance.ListBusinessProfilesApiV1BusinessProfilesGet(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessProfilesApi.ListBusinessProfilesApiV1BusinessProfilesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBusinessProfilesApiV1BusinessProfilesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Business Profiles
    ApiResponse<BusinessProfilesListResponse> response = apiInstance.ListBusinessProfilesApiV1BusinessProfilesGetWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessProfilesApi.ListBusinessProfilesApiV1BusinessProfilesGetWithHttpInfo: " + e.Message);
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

<a id="patchbusinessprofileapiv1businessprofilesbusinessprofileidpatch"></a>
# **PatchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch**
> BusinessProfileResponse PatchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch (string businessProfileId, BusinessProfilePatch businessProfilePatch, string? idempotencyKey = null)

Patch Business Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PatchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatchExample
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
                // Patch Business Profile
                BusinessProfileResponse result = apiInstance.PatchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch(businessProfileId, businessProfilePatch, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BusinessProfilesApi.PatchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PatchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Patch Business Profile
    ApiResponse<BusinessProfileResponse> response = apiInstance.PatchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatchWithHttpInfo(businessProfileId, businessProfilePatch, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BusinessProfilesApi.PatchBusinessProfileApiV1BusinessProfilesBusinessProfileIdPatchWithHttpInfo: " + e.Message);
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

