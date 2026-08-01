# InvoicePDFs.Api.TemplatesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTemplateApiV1TemplatesCustomPost**](TemplatesApi.md#createtemplateapiv1templatescustompost) | **POST** /api/v1/templates/custom | Create Template |
| [**DeleteTemplateApiV1TemplatesCustomTemplateIdDelete**](TemplatesApi.md#deletetemplateapiv1templatescustomtemplateiddelete) | **DELETE** /api/v1/templates/custom/{template_id} | Delete Template |
| [**DuplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost**](TemplatesApi.md#duplicatetemplateapiv1templatescustomtemplateidduplicatepost) | **POST** /api/v1/templates/custom/{template_id}/duplicate | Duplicate Template |
| [**GetBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet**](TemplatesApi.md#getbuiltintemplateapiv1templatesbuiltintemplateidget) | **GET** /api/v1/templates/builtin/{template_id} | Get Builtin Template |
| [**GetCustomTemplateApiV1TemplatesCustomTemplateIdGet**](TemplatesApi.md#getcustomtemplateapiv1templatescustomtemplateidget) | **GET** /api/v1/templates/custom/{template_id} | Get Custom Template |
| [**GetTemplateApiV1TemplatesTemplateIdGet**](TemplatesApi.md#gettemplateapiv1templatestemplateidget) | **GET** /api/v1/templates/{template_id} | Get Template |
| [**ListCustomTemplatesApiV1TemplatesCustomGet**](TemplatesApi.md#listcustomtemplatesapiv1templatescustomget) | **GET** /api/v1/templates/custom | List Custom Templates |
| [**PatchTemplateApiV1TemplatesCustomTemplateIdPatch**](TemplatesApi.md#patchtemplateapiv1templatescustomtemplateidpatch) | **PATCH** /api/v1/templates/custom/{template_id} | Patch Template |
| [**PreviewTemplateApiV1TemplatesTemplateIdPreviewPost**](TemplatesApi.md#previewtemplateapiv1templatestemplateidpreviewpost) | **POST** /api/v1/templates/{template_id}/preview | Preview Template |
| [**PublishTemplateApiV1TemplatesCustomTemplateIdPublishPost**](TemplatesApi.md#publishtemplateapiv1templatescustomtemplateidpublishpost) | **POST** /api/v1/templates/custom/{template_id}/publish | Publish Template |
| [**TemplatesApiV1TemplatesGet**](TemplatesApi.md#templatesapiv1templatesget) | **GET** /api/v1/templates | Templates |

<a id="createtemplateapiv1templatescustompost"></a>
# **CreateTemplateApiV1TemplatesCustomPost**
> CustomTemplateResponse CreateTemplateApiV1TemplatesCustomPost (TemplateCreateRequest templateCreateRequest)

Create Template

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateTemplateApiV1TemplatesCustomPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplatesApi(config);
            var templateCreateRequest = new TemplateCreateRequest(); // TemplateCreateRequest | 

            try
            {
                // Create Template
                CustomTemplateResponse result = apiInstance.CreateTemplateApiV1TemplatesCustomPost(templateCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplatesApi.CreateTemplateApiV1TemplatesCustomPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTemplateApiV1TemplatesCustomPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Template
    ApiResponse<CustomTemplateResponse> response = apiInstance.CreateTemplateApiV1TemplatesCustomPostWithHttpInfo(templateCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplatesApi.CreateTemplateApiV1TemplatesCustomPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateCreateRequest** | [**TemplateCreateRequest**](TemplateCreateRequest.md) |  |  |

### Return type

[**CustomTemplateResponse**](CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="deletetemplateapiv1templatescustomtemplateiddelete"></a>
# **DeleteTemplateApiV1TemplatesCustomTemplateIdDelete**
> void DeleteTemplateApiV1TemplatesCustomTemplateIdDelete (string templateId)

Delete Template

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteTemplateApiV1TemplatesCustomTemplateIdDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplatesApi(config);
            var templateId = "templateId_example";  // string | 

            try
            {
                // Delete Template
                apiInstance.DeleteTemplateApiV1TemplatesCustomTemplateIdDelete(templateId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplatesApi.DeleteTemplateApiV1TemplatesCustomTemplateIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTemplateApiV1TemplatesCustomTemplateIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Template
    apiInstance.DeleteTemplateApiV1TemplatesCustomTemplateIdDeleteWithHttpInfo(templateId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplatesApi.DeleteTemplateApiV1TemplatesCustomTemplateIdDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** |  |  |

### Return type

void (empty response body)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="duplicatetemplateapiv1templatescustomtemplateidduplicatepost"></a>
# **DuplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost**
> CustomTemplateResponse DuplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost (string templateId)

Duplicate Template

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DuplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplatesApi(config);
            var templateId = "templateId_example";  // string | 

            try
            {
                // Duplicate Template
                CustomTemplateResponse result = apiInstance.DuplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost(templateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplatesApi.DuplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Duplicate Template
    ApiResponse<CustomTemplateResponse> response = apiInstance.DuplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePostWithHttpInfo(templateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplatesApi.DuplicateTemplateApiV1TemplatesCustomTemplateIdDuplicatePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** |  |  |

### Return type

[**CustomTemplateResponse**](CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getbuiltintemplateapiv1templatesbuiltintemplateidget"></a>
# **GetBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet**
> TemplateDetailResponse GetBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet (string templateId)

Get Builtin Template

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplatesApi(config);
            var templateId = "templateId_example";  // string | 

            try
            {
                // Get Builtin Template
                TemplateDetailResponse result = apiInstance.GetBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet(templateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplatesApi.GetBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Builtin Template
    ApiResponse<TemplateDetailResponse> response = apiInstance.GetBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGetWithHttpInfo(templateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplatesApi.GetBuiltinTemplateApiV1TemplatesBuiltinTemplateIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** |  |  |

### Return type

[**TemplateDetailResponse**](TemplateDetailResponse.md)

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

<a id="getcustomtemplateapiv1templatescustomtemplateidget"></a>
# **GetCustomTemplateApiV1TemplatesCustomTemplateIdGet**
> CustomTemplateResponse GetCustomTemplateApiV1TemplatesCustomTemplateIdGet (string templateId)

Get Custom Template

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetCustomTemplateApiV1TemplatesCustomTemplateIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplatesApi(config);
            var templateId = "templateId_example";  // string | 

            try
            {
                // Get Custom Template
                CustomTemplateResponse result = apiInstance.GetCustomTemplateApiV1TemplatesCustomTemplateIdGet(templateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplatesApi.GetCustomTemplateApiV1TemplatesCustomTemplateIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCustomTemplateApiV1TemplatesCustomTemplateIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Custom Template
    ApiResponse<CustomTemplateResponse> response = apiInstance.GetCustomTemplateApiV1TemplatesCustomTemplateIdGetWithHttpInfo(templateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplatesApi.GetCustomTemplateApiV1TemplatesCustomTemplateIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** |  |  |

### Return type

[**CustomTemplateResponse**](CustomTemplateResponse.md)

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

<a id="gettemplateapiv1templatestemplateidget"></a>
# **GetTemplateApiV1TemplatesTemplateIdGet**
> TemplateDetailResponse GetTemplateApiV1TemplatesTemplateIdGet (string templateId)

Get Template

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetTemplateApiV1TemplatesTemplateIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplatesApi(config);
            var templateId = "templateId_example";  // string | 

            try
            {
                // Get Template
                TemplateDetailResponse result = apiInstance.GetTemplateApiV1TemplatesTemplateIdGet(templateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplatesApi.GetTemplateApiV1TemplatesTemplateIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTemplateApiV1TemplatesTemplateIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Template
    ApiResponse<TemplateDetailResponse> response = apiInstance.GetTemplateApiV1TemplatesTemplateIdGetWithHttpInfo(templateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplatesApi.GetTemplateApiV1TemplatesTemplateIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** |  |  |

### Return type

[**TemplateDetailResponse**](TemplateDetailResponse.md)

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

<a id="listcustomtemplatesapiv1templatescustomget"></a>
# **ListCustomTemplatesApiV1TemplatesCustomGet**
> CustomTemplatesListResponse ListCustomTemplatesApiV1TemplatesCustomGet (int? limit = null, string? cursor = null)

List Custom Templates

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListCustomTemplatesApiV1TemplatesCustomGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplatesApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Custom Templates
                CustomTemplatesListResponse result = apiInstance.ListCustomTemplatesApiV1TemplatesCustomGet(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplatesApi.ListCustomTemplatesApiV1TemplatesCustomGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCustomTemplatesApiV1TemplatesCustomGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Custom Templates
    ApiResponse<CustomTemplatesListResponse> response = apiInstance.ListCustomTemplatesApiV1TemplatesCustomGetWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplatesApi.ListCustomTemplatesApiV1TemplatesCustomGetWithHttpInfo: " + e.Message);
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

[**CustomTemplatesListResponse**](CustomTemplatesListResponse.md)

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

<a id="patchtemplateapiv1templatescustomtemplateidpatch"></a>
# **PatchTemplateApiV1TemplatesCustomTemplateIdPatch**
> CustomTemplateResponse PatchTemplateApiV1TemplatesCustomTemplateIdPatch (string templateId, TemplatePatchRequest templatePatchRequest)

Patch Template

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PatchTemplateApiV1TemplatesCustomTemplateIdPatchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplatesApi(config);
            var templateId = "templateId_example";  // string | 
            var templatePatchRequest = new TemplatePatchRequest(); // TemplatePatchRequest | 

            try
            {
                // Patch Template
                CustomTemplateResponse result = apiInstance.PatchTemplateApiV1TemplatesCustomTemplateIdPatch(templateId, templatePatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplatesApi.PatchTemplateApiV1TemplatesCustomTemplateIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PatchTemplateApiV1TemplatesCustomTemplateIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Patch Template
    ApiResponse<CustomTemplateResponse> response = apiInstance.PatchTemplateApiV1TemplatesCustomTemplateIdPatchWithHttpInfo(templateId, templatePatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplatesApi.PatchTemplateApiV1TemplatesCustomTemplateIdPatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** |  |  |
| **templatePatchRequest** | [**TemplatePatchRequest**](TemplatePatchRequest.md) |  |  |

### Return type

[**CustomTemplateResponse**](CustomTemplateResponse.md)

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

<a id="previewtemplateapiv1templatestemplateidpreviewpost"></a>
# **PreviewTemplateApiV1TemplatesTemplateIdPreviewPost**
> Object PreviewTemplateApiV1TemplatesTemplateIdPreviewPost (string templateId, AppSchemasV1DocumentRenderRequest appSchemasV1DocumentRenderRequest, string? idempotencyKey = null)

Preview Template

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PreviewTemplateApiV1TemplatesTemplateIdPreviewPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplatesApi(config);
            var templateId = "templateId_example";  // string | 
            var appSchemasV1DocumentRenderRequest = new AppSchemasV1DocumentRenderRequest(); // AppSchemasV1DocumentRenderRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Preview Template
                Object result = apiInstance.PreviewTemplateApiV1TemplatesTemplateIdPreviewPost(templateId, appSchemasV1DocumentRenderRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplatesApi.PreviewTemplateApiV1TemplatesTemplateIdPreviewPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PreviewTemplateApiV1TemplatesTemplateIdPreviewPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Preview Template
    ApiResponse<Object> response = apiInstance.PreviewTemplateApiV1TemplatesTemplateIdPreviewPostWithHttpInfo(templateId, appSchemasV1DocumentRenderRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplatesApi.PreviewTemplateApiV1TemplatesTemplateIdPreviewPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** |  |  |
| **appSchemasV1DocumentRenderRequest** | [**AppSchemasV1DocumentRenderRequest**](AppSchemasV1DocumentRenderRequest.md) |  |  |
| **idempotencyKey** | **string?** |  | [optional]  |

### Return type

**Object**

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

<a id="publishtemplateapiv1templatescustomtemplateidpublishpost"></a>
# **PublishTemplateApiV1TemplatesCustomTemplateIdPublishPost**
> CustomTemplateResponse PublishTemplateApiV1TemplatesCustomTemplateIdPublishPost (string templateId)

Publish Template

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PublishTemplateApiV1TemplatesCustomTemplateIdPublishPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplatesApi(config);
            var templateId = "templateId_example";  // string | 

            try
            {
                // Publish Template
                CustomTemplateResponse result = apiInstance.PublishTemplateApiV1TemplatesCustomTemplateIdPublishPost(templateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplatesApi.PublishTemplateApiV1TemplatesCustomTemplateIdPublishPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PublishTemplateApiV1TemplatesCustomTemplateIdPublishPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Publish Template
    ApiResponse<CustomTemplateResponse> response = apiInstance.PublishTemplateApiV1TemplatesCustomTemplateIdPublishPostWithHttpInfo(templateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplatesApi.PublishTemplateApiV1TemplatesCustomTemplateIdPublishPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **templateId** | **string** |  |  |

### Return type

[**CustomTemplateResponse**](CustomTemplateResponse.md)

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

<a id="templatesapiv1templatesget"></a>
# **TemplatesApiV1TemplatesGet**
> TemplatesListResponse TemplatesApiV1TemplatesGet ()

Templates

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class TemplatesApiV1TemplatesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TemplatesApi(config);

            try
            {
                // Templates
                TemplatesListResponse result = apiInstance.TemplatesApiV1TemplatesGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TemplatesApi.TemplatesApiV1TemplatesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TemplatesApiV1TemplatesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Templates
    ApiResponse<TemplatesListResponse> response = apiInstance.TemplatesApiV1TemplatesGetWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TemplatesApi.TemplatesApiV1TemplatesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**TemplatesListResponse**](TemplatesListResponse.md)

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

