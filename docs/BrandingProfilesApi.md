# InvoicePDFs.Api.BrandingProfilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateBrandingProfile**](BrandingProfilesApi.md#createbrandingprofile) | **POST** /api/v1/branding-profiles | Create Branding Profile |
| [**DeleteBrandingLogo**](BrandingProfilesApi.md#deletebrandinglogo) | **DELETE** /api/v1/branding-profiles/{profile_id}/logo | Delete Branding Logo |
| [**DeleteBrandingProfile**](BrandingProfilesApi.md#deletebrandingprofile) | **DELETE** /api/v1/branding-profiles/{profile_id} | Delete Branding Profile |
| [**GetBrandingProfile**](BrandingProfilesApi.md#getbrandingprofile) | **GET** /api/v1/branding-profiles/{profile_id} | Get Branding Profile |
| [**ListBrandingProfiles**](BrandingProfilesApi.md#listbrandingprofiles) | **GET** /api/v1/branding-profiles | List Branding Profiles |
| [**SetDefaultBrandingProfile**](BrandingProfilesApi.md#setdefaultbrandingprofile) | **POST** /api/v1/branding-profiles/{profile_id}/default | Set Default Branding Profile |
| [**UpdateBrandingProfile**](BrandingProfilesApi.md#updatebrandingprofile) | **PATCH** /api/v1/branding-profiles/{profile_id} | Update Branding Profile |
| [**UploadBrandingLogo**](BrandingProfilesApi.md#uploadbrandinglogo) | **POST** /api/v1/branding-profiles/{profile_id}/logo | Upload Branding Logo |

<a id="createbrandingprofile"></a>
# **CreateBrandingProfile**
> BrandingProfileResponse CreateBrandingProfile (BrandingProfileCreateRequest brandingProfileCreateRequest)

Create Branding Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateBrandingProfileExample
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
                // Create Branding Profile
                BrandingProfileResponse result = apiInstance.CreateBrandingProfile(brandingProfileCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.CreateBrandingProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBrandingProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Branding Profile
    ApiResponse<BrandingProfileResponse> response = apiInstance.CreateBrandingProfileWithHttpInfo(brandingProfileCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.CreateBrandingProfileWithHttpInfo: " + e.Message);
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

<a id="deletebrandinglogo"></a>
# **DeleteBrandingLogo**
> SimpleBoolResponse DeleteBrandingLogo (string profileId)

Delete Branding Logo

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteBrandingLogoExample
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
                // Delete Branding Logo
                SimpleBoolResponse result = apiInstance.DeleteBrandingLogo(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.DeleteBrandingLogo: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBrandingLogoWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Branding Logo
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteBrandingLogoWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.DeleteBrandingLogoWithHttpInfo: " + e.Message);
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

<a id="deletebrandingprofile"></a>
# **DeleteBrandingProfile**
> SimpleBoolResponse DeleteBrandingProfile (string profileId)

Delete Branding Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteBrandingProfileExample
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
                // Delete Branding Profile
                SimpleBoolResponse result = apiInstance.DeleteBrandingProfile(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.DeleteBrandingProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteBrandingProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Branding Profile
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteBrandingProfileWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.DeleteBrandingProfileWithHttpInfo: " + e.Message);
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

<a id="getbrandingprofile"></a>
# **GetBrandingProfile**
> BrandingProfileResponse GetBrandingProfile (string profileId)

Get Branding Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetBrandingProfileExample
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
                // Get Branding Profile
                BrandingProfileResponse result = apiInstance.GetBrandingProfile(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.GetBrandingProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBrandingProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Branding Profile
    ApiResponse<BrandingProfileResponse> response = apiInstance.GetBrandingProfileWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.GetBrandingProfileWithHttpInfo: " + e.Message);
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

<a id="listbrandingprofiles"></a>
# **ListBrandingProfiles**
> BrandingProfilesListResponse ListBrandingProfiles ()

List Branding Profiles

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListBrandingProfilesExample
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
                // List Branding Profiles
                BrandingProfilesListResponse result = apiInstance.ListBrandingProfiles();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.ListBrandingProfiles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBrandingProfilesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Branding Profiles
    ApiResponse<BrandingProfilesListResponse> response = apiInstance.ListBrandingProfilesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.ListBrandingProfilesWithHttpInfo: " + e.Message);
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

<a id="setdefaultbrandingprofile"></a>
# **SetDefaultBrandingProfile**
> BrandingProfileResponse SetDefaultBrandingProfile (string profileId)

Set Default Branding Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class SetDefaultBrandingProfileExample
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
                // Set Default Branding Profile
                BrandingProfileResponse result = apiInstance.SetDefaultBrandingProfile(profileId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.SetDefaultBrandingProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetDefaultBrandingProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Set Default Branding Profile
    ApiResponse<BrandingProfileResponse> response = apiInstance.SetDefaultBrandingProfileWithHttpInfo(profileId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.SetDefaultBrandingProfileWithHttpInfo: " + e.Message);
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

<a id="updatebrandingprofile"></a>
# **UpdateBrandingProfile**
> BrandingProfileResponse UpdateBrandingProfile (string profileId, BrandingProfilePatchRequest brandingProfilePatchRequest)

Update Branding Profile

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UpdateBrandingProfileExample
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
                // Update Branding Profile
                BrandingProfileResponse result = apiInstance.UpdateBrandingProfile(profileId, brandingProfilePatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.UpdateBrandingProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateBrandingProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Branding Profile
    ApiResponse<BrandingProfileResponse> response = apiInstance.UpdateBrandingProfileWithHttpInfo(profileId, brandingProfilePatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.UpdateBrandingProfileWithHttpInfo: " + e.Message);
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

<a id="uploadbrandinglogo"></a>
# **UploadBrandingLogo**
> BrandingProfileResponse UploadBrandingLogo (string profileId, System.IO.Stream file)

Upload Branding Logo

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UploadBrandingLogoExample
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
                // Upload Branding Logo
                BrandingProfileResponse result = apiInstance.UploadBrandingLogo(profileId, file);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BrandingProfilesApi.UploadBrandingLogo: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadBrandingLogoWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload Branding Logo
    ApiResponse<BrandingProfileResponse> response = apiInstance.UploadBrandingLogoWithHttpInfo(profileId, file);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BrandingProfilesApi.UploadBrandingLogoWithHttpInfo: " + e.Message);
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

