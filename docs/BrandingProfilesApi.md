# InvoicePDFs.Api.BrandingProfilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateProfileApiV1BrandingProfilesPost**](BrandingProfilesApi.md#createprofileapiv1brandingprofilespost) | **POST** /api/v1/branding-profiles | Create Profile |
| [**DeleteLogoApiV1BrandingProfilesProfileIdLogoDelete**](BrandingProfilesApi.md#deletelogoapiv1brandingprofilesprofileidlogodelete) | **DELETE** /api/v1/branding-profiles/{profile_id}/logo | Delete Logo |
| [**DeleteProfileApiV1BrandingProfilesProfileIdDelete**](BrandingProfilesApi.md#deleteprofileapiv1brandingprofilesprofileiddelete) | **DELETE** /api/v1/branding-profiles/{profile_id} | Delete Profile |
| [**GetProfileApiV1BrandingProfilesProfileIdGet**](BrandingProfilesApi.md#getprofileapiv1brandingprofilesprofileidget) | **GET** /api/v1/branding-profiles/{profile_id} | Get Profile |
| [**ListProfilesApiV1BrandingProfilesGet**](BrandingProfilesApi.md#listprofilesapiv1brandingprofilesget) | **GET** /api/v1/branding-profiles | List Profiles |
| [**SetDefaultApiV1BrandingProfilesProfileIdDefaultPost**](BrandingProfilesApi.md#setdefaultapiv1brandingprofilesprofileiddefaultpost) | **POST** /api/v1/branding-profiles/{profile_id}/default | Set Default |
| [**UpdateProfileApiV1BrandingProfilesProfileIdPatch**](BrandingProfilesApi.md#updateprofileapiv1brandingprofilesprofileidpatch) | **PATCH** /api/v1/branding-profiles/{profile_id} | Update Profile |
| [**UploadLogoApiV1BrandingProfilesProfileIdLogoPost**](BrandingProfilesApi.md#uploadlogoapiv1brandingprofilesprofileidlogopost) | **POST** /api/v1/branding-profiles/{profile_id}/logo | Upload Logo |

<a id="createprofileapiv1brandingprofilespost"></a>
# **CreateProfileApiV1BrandingProfilesPost**
> BrandingProfileResponse CreateProfileApiV1BrandingProfilesPost (BrandingProfileCreateRequest brandingProfileCreateRequest)

Create Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateProfileApiV1BrandingProfilesPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BrandingProfilesApi(config);
            var brandingProfileCreateRequest = new BrandingProfileCreateRequest(); // BrandingProfileCreateRequest | 

            try
            {
                // Create Profile
                BrandingProfileResponse result = apiInstance.CreateProfileApiV1BrandingProfilesPost(brandingProfileCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.CreateProfileApiV1BrandingProfilesPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateProfileApiV1BrandingProfilesPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Profile
    ApiResponse<BrandingProfileResponse> response = apiInstance.CreateProfileApiV1BrandingProfilesPostWithHttpInfo(brandingProfileCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.CreateProfileApiV1BrandingProfilesPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **brandingProfileCreateRequest** | [**BrandingProfileCreateRequest**](BrandingProfileCreateRequest.md) |  |  |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

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

<a id="deletelogoapiv1brandingprofilesprofileidlogodelete"></a>
# **DeleteLogoApiV1BrandingProfilesProfileIdLogoDelete**
> SimpleBoolResponse DeleteLogoApiV1BrandingProfilesProfileIdLogoDelete (string profileId)

Delete Logo

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteLogoApiV1BrandingProfilesProfileIdLogoDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BrandingProfilesApi(config);
            var profileId = "profileId_example";  // string | 

            try
            {
                // Delete Logo
                SimpleBoolResponse result = apiInstance.DeleteLogoApiV1BrandingProfilesProfileIdLogoDelete(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.DeleteLogoApiV1BrandingProfilesProfileIdLogoDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteLogoApiV1BrandingProfilesProfileIdLogoDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Logo
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteLogoApiV1BrandingProfilesProfileIdLogoDeleteWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.DeleteLogoApiV1BrandingProfilesProfileIdLogoDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** |  |  |

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

<a id="deleteprofileapiv1brandingprofilesprofileiddelete"></a>
# **DeleteProfileApiV1BrandingProfilesProfileIdDelete**
> SimpleBoolResponse DeleteProfileApiV1BrandingProfilesProfileIdDelete (string profileId)

Delete Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteProfileApiV1BrandingProfilesProfileIdDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BrandingProfilesApi(config);
            var profileId = "profileId_example";  // string | 

            try
            {
                // Delete Profile
                SimpleBoolResponse result = apiInstance.DeleteProfileApiV1BrandingProfilesProfileIdDelete(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.DeleteProfileApiV1BrandingProfilesProfileIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteProfileApiV1BrandingProfilesProfileIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Profile
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteProfileApiV1BrandingProfilesProfileIdDeleteWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.DeleteProfileApiV1BrandingProfilesProfileIdDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** |  |  |

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

<a id="getprofileapiv1brandingprofilesprofileidget"></a>
# **GetProfileApiV1BrandingProfilesProfileIdGet**
> BrandingProfileResponse GetProfileApiV1BrandingProfilesProfileIdGet (string profileId)

Get Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetProfileApiV1BrandingProfilesProfileIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BrandingProfilesApi(config);
            var profileId = "profileId_example";  // string | 

            try
            {
                // Get Profile
                BrandingProfileResponse result = apiInstance.GetProfileApiV1BrandingProfilesProfileIdGet(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.GetProfileApiV1BrandingProfilesProfileIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetProfileApiV1BrandingProfilesProfileIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Profile
    ApiResponse<BrandingProfileResponse> response = apiInstance.GetProfileApiV1BrandingProfilesProfileIdGetWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.GetProfileApiV1BrandingProfilesProfileIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** |  |  |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

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

<a id="listprofilesapiv1brandingprofilesget"></a>
# **ListProfilesApiV1BrandingProfilesGet**
> BrandingProfilesListResponse ListProfilesApiV1BrandingProfilesGet ()

List Profiles

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListProfilesApiV1BrandingProfilesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BrandingProfilesApi(config);

            try
            {
                // List Profiles
                BrandingProfilesListResponse result = apiInstance.ListProfilesApiV1BrandingProfilesGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.ListProfilesApiV1BrandingProfilesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListProfilesApiV1BrandingProfilesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Profiles
    ApiResponse<BrandingProfilesListResponse> response = apiInstance.ListProfilesApiV1BrandingProfilesGetWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.ListProfilesApiV1BrandingProfilesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**BrandingProfilesListResponse**](BrandingProfilesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="setdefaultapiv1brandingprofilesprofileiddefaultpost"></a>
# **SetDefaultApiV1BrandingProfilesProfileIdDefaultPost**
> BrandingProfileResponse SetDefaultApiV1BrandingProfilesProfileIdDefaultPost (string profileId)

Set Default

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class SetDefaultApiV1BrandingProfilesProfileIdDefaultPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BrandingProfilesApi(config);
            var profileId = "profileId_example";  // string | 

            try
            {
                // Set Default
                BrandingProfileResponse result = apiInstance.SetDefaultApiV1BrandingProfilesProfileIdDefaultPost(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.SetDefaultApiV1BrandingProfilesProfileIdDefaultPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetDefaultApiV1BrandingProfilesProfileIdDefaultPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set Default
    ApiResponse<BrandingProfileResponse> response = apiInstance.SetDefaultApiV1BrandingProfilesProfileIdDefaultPostWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.SetDefaultApiV1BrandingProfilesProfileIdDefaultPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** |  |  |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

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

<a id="updateprofileapiv1brandingprofilesprofileidpatch"></a>
# **UpdateProfileApiV1BrandingProfilesProfileIdPatch**
> BrandingProfileResponse UpdateProfileApiV1BrandingProfilesProfileIdPatch (string profileId, BrandingProfilePatchRequest brandingProfilePatchRequest)

Update Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UpdateProfileApiV1BrandingProfilesProfileIdPatchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BrandingProfilesApi(config);
            var profileId = "profileId_example";  // string | 
            var brandingProfilePatchRequest = new BrandingProfilePatchRequest(); // BrandingProfilePatchRequest | 

            try
            {
                // Update Profile
                BrandingProfileResponse result = apiInstance.UpdateProfileApiV1BrandingProfilesProfileIdPatch(profileId, brandingProfilePatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.UpdateProfileApiV1BrandingProfilesProfileIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateProfileApiV1BrandingProfilesProfileIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Profile
    ApiResponse<BrandingProfileResponse> response = apiInstance.UpdateProfileApiV1BrandingProfilesProfileIdPatchWithHttpInfo(profileId, brandingProfilePatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.UpdateProfileApiV1BrandingProfilesProfileIdPatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** |  |  |
| **brandingProfilePatchRequest** | [**BrandingProfilePatchRequest**](BrandingProfilePatchRequest.md) |  |  |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

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

<a id="uploadlogoapiv1brandingprofilesprofileidlogopost"></a>
# **UploadLogoApiV1BrandingProfilesProfileIdLogoPost**
> BrandingProfileResponse UploadLogoApiV1BrandingProfilesProfileIdLogoPost (string profileId, System.IO.Stream file)

Upload Logo

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UploadLogoApiV1BrandingProfilesProfileIdLogoPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BrandingProfilesApi(config);
            var profileId = "profileId_example";  // string | 
            var file = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // System.IO.Stream | 

            try
            {
                // Upload Logo
                BrandingProfileResponse result = apiInstance.UploadLogoApiV1BrandingProfilesProfileIdLogoPost(profileId, file);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.UploadLogoApiV1BrandingProfilesProfileIdLogoPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadLogoApiV1BrandingProfilesProfileIdLogoPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload Logo
    ApiResponse<BrandingProfileResponse> response = apiInstance.UploadLogoApiV1BrandingProfilesProfileIdLogoPostWithHttpInfo(profileId, file);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.UploadLogoApiV1BrandingProfilesProfileIdLogoPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **profileId** | **string** |  |  |
| **file** | **System.IO.Stream****System.IO.Stream** |  |  |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

