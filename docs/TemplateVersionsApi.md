# InvoicePDFs.Api.TemplateVersionsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTemplateVersion**](TemplateVersionsApi.md#createtemplateversion) | **POST** /api/v1/templates/{template_id}/versions | Create Template Version |
| [**GetTemplateVersion**](TemplateVersionsApi.md#gettemplateversion) | **GET** /api/v1/templates/{template_id}/versions/{version} | Get Template Version |
| [**ListTemplateVersions**](TemplateVersionsApi.md#listtemplateversions) | **GET** /api/v1/templates/{template_id}/versions | List Template Versions |

<a id="createtemplateversion"></a>
# **CreateTemplateVersion**
> TemplateVersionResponse CreateTemplateVersion (string templateId, TemplateVersionCreateRequest templateVersionCreateRequest)

Create Template Version

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateTemplateVersionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplateVersionsApi(config);
            var templateId = "templateId_example";  // string | 
            var templateVersionCreateRequest = new TemplateVersionCreateRequest(); // TemplateVersionCreateRequest | 

            try
            {
                // Create Template Version
                TemplateVersionResponse result = apiInstance.CreateTemplateVersion(templateId, templateVersionCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplateVersionsApi.CreateTemplateVersion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTemplateVersionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Template Version
    ApiResponse<TemplateVersionResponse> response = apiInstance.CreateTemplateVersionWithHttpInfo(templateId, templateVersionCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplateVersionsApi.CreateTemplateVersionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** |  |  |
| **templateVersionCreateRequest** | [**TemplateVersionCreateRequest**](TemplateVersionCreateRequest.md) |  |  |

### Return type

[**TemplateVersionResponse**](TemplateVersionResponse.md)

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

<a id="gettemplateversion"></a>
# **GetTemplateVersion**
> TemplateVersionResponse GetTemplateVersion (string templateId, int version)

Get Template Version

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetTemplateVersionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplateVersionsApi(config);
            var templateId = "templateId_example";  // string | 
            var version = 56;  // int | 

            try
            {
                // Get Template Version
                TemplateVersionResponse result = apiInstance.GetTemplateVersion(templateId, version);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplateVersionsApi.GetTemplateVersion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTemplateVersionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Template Version
    ApiResponse<TemplateVersionResponse> response = apiInstance.GetTemplateVersionWithHttpInfo(templateId, version);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplateVersionsApi.GetTemplateVersionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** |  |  |
| **version** | **int** |  |  |

### Return type

[**TemplateVersionResponse**](TemplateVersionResponse.md)

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

<a id="listtemplateversions"></a>
# **ListTemplateVersions**
> TemplateVersionsListResponse ListTemplateVersions (string templateId)

List Template Versions

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListTemplateVersionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplateVersionsApi(config);
            var templateId = "templateId_example";  // string | 

            try
            {
                // List Template Versions
                TemplateVersionsListResponse result = apiInstance.ListTemplateVersions(templateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplateVersionsApi.ListTemplateVersions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTemplateVersionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Template Versions
    ApiResponse<TemplateVersionsListResponse> response = apiInstance.ListTemplateVersionsWithHttpInfo(templateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplateVersionsApi.ListTemplateVersionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** |  |  |

### Return type

[**TemplateVersionsListResponse**](TemplateVersionsListResponse.md)

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

