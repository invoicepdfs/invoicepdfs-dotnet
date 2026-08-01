# InvoicePDFs.Api.TemplateVersionsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTemplateVersionApiV1TemplatesTemplateIdVersionsPost**](TemplateVersionsApi.md#createtemplateversionapiv1templatestemplateidversionspost) | **POST** /api/v1/templates/{template_id}/versions | Create Template Version |
| [**GetTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet**](TemplateVersionsApi.md#gettemplateversionapiv1templatestemplateidversionsversionget) | **GET** /api/v1/templates/{template_id}/versions/{version} | Get Template Version |
| [**ListTemplateVersionsApiV1TemplatesTemplateIdVersionsGet**](TemplateVersionsApi.md#listtemplateversionsapiv1templatestemplateidversionsget) | **GET** /api/v1/templates/{template_id}/versions | List Template Versions |

<a id="createtemplateversionapiv1templatestemplateidversionspost"></a>
# **CreateTemplateVersionApiV1TemplatesTemplateIdVersionsPost**
> TemplateVersionResponse CreateTemplateVersionApiV1TemplatesTemplateIdVersionsPost (string templateId, TemplateVersionCreateRequest templateVersionCreateRequest)

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
    public class CreateTemplateVersionApiV1TemplatesTemplateIdVersionsPostExample
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
                TemplateVersionResponse result = apiInstance.CreateTemplateVersionApiV1TemplatesTemplateIdVersionsPost(templateId, templateVersionCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplateVersionsApi.CreateTemplateVersionApiV1TemplatesTemplateIdVersionsPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTemplateVersionApiV1TemplatesTemplateIdVersionsPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Template Version
    ApiResponse<TemplateVersionResponse> response = apiInstance.CreateTemplateVersionApiV1TemplatesTemplateIdVersionsPostWithHttpInfo(templateId, templateVersionCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplateVersionsApi.CreateTemplateVersionApiV1TemplatesTemplateIdVersionsPostWithHttpInfo: " + e.Message);
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

<a id="gettemplateversionapiv1templatestemplateidversionsversionget"></a>
# **GetTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet**
> TemplateVersionResponse GetTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet (string templateId, int version)

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
    public class GetTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGetExample
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
                TemplateVersionResponse result = apiInstance.GetTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet(templateId, version);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplateVersionsApi.GetTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Template Version
    ApiResponse<TemplateVersionResponse> response = apiInstance.GetTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGetWithHttpInfo(templateId, version);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplateVersionsApi.GetTemplateVersionApiV1TemplatesTemplateIdVersionsVersionGetWithHttpInfo: " + e.Message);
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

<a id="listtemplateversionsapiv1templatestemplateidversionsget"></a>
# **ListTemplateVersionsApiV1TemplatesTemplateIdVersionsGet**
> TemplateVersionsListResponse ListTemplateVersionsApiV1TemplatesTemplateIdVersionsGet (string templateId)

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
    public class ListTemplateVersionsApiV1TemplatesTemplateIdVersionsGetExample
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
                TemplateVersionsListResponse result = apiInstance.ListTemplateVersionsApiV1TemplatesTemplateIdVersionsGet(templateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplateVersionsApi.ListTemplateVersionsApiV1TemplatesTemplateIdVersionsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTemplateVersionsApiV1TemplatesTemplateIdVersionsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Template Versions
    ApiResponse<TemplateVersionsListResponse> response = apiInstance.ListTemplateVersionsApiV1TemplatesTemplateIdVersionsGetWithHttpInfo(templateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplateVersionsApi.ListTemplateVersionsApiV1TemplatesTemplateIdVersionsGetWithHttpInfo: " + e.Message);
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

