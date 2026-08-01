# InvoicePDFs.Api.DocumentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CalculateDocumentApiV1DocumentsCalculatePost**](DocumentsApi.md#calculatedocumentapiv1documentscalculatepost) | **POST** /api/v1/documents/calculate | Calculate Document |
| [**RenderDocumentApiV1DocumentsRenderPost**](DocumentsApi.md#renderdocumentapiv1documentsrenderpost) | **POST** /api/v1/documents/render | Render Document |
| [**ValidateDocumentApiV1DocumentsValidatePost**](DocumentsApi.md#validatedocumentapiv1documentsvalidatepost) | **POST** /api/v1/documents/validate | Validate Document |

<a id="calculatedocumentapiv1documentscalculatepost"></a>
# **CalculateDocumentApiV1DocumentsCalculatePost**
> DocumentCalculateResponse CalculateDocumentApiV1DocumentsCalculatePost (DocumentCalculateRequest documentCalculateRequest)

Calculate Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CalculateDocumentApiV1DocumentsCalculatePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentCalculateRequest = new DocumentCalculateRequest(); // DocumentCalculateRequest | 

            try
            {
                // Calculate Document
                DocumentCalculateResponse result = apiInstance.CalculateDocumentApiV1DocumentsCalculatePost(documentCalculateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.CalculateDocumentApiV1DocumentsCalculatePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CalculateDocumentApiV1DocumentsCalculatePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Calculate Document
    ApiResponse<DocumentCalculateResponse> response = apiInstance.CalculateDocumentApiV1DocumentsCalculatePostWithHttpInfo(documentCalculateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.CalculateDocumentApiV1DocumentsCalculatePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentCalculateRequest** | [**DocumentCalculateRequest**](DocumentCalculateRequest.md) |  |  |

### Return type

[**DocumentCalculateResponse**](DocumentCalculateResponse.md)

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

<a id="renderdocumentapiv1documentsrenderpost"></a>
# **RenderDocumentApiV1DocumentsRenderPost**
> Object RenderDocumentApiV1DocumentsRenderPost (DocumentRenderRequest documentRenderRequest, string? idempotencyKey = null)

Render Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RenderDocumentApiV1DocumentsRenderPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentRenderRequest = new DocumentRenderRequest(); // DocumentRenderRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Render Document
                Object result = apiInstance.RenderDocumentApiV1DocumentsRenderPost(documentRenderRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.RenderDocumentApiV1DocumentsRenderPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RenderDocumentApiV1DocumentsRenderPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Render Document
    ApiResponse<Object> response = apiInstance.RenderDocumentApiV1DocumentsRenderPostWithHttpInfo(documentRenderRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.RenderDocumentApiV1DocumentsRenderPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentRenderRequest** | [**DocumentRenderRequest**](DocumentRenderRequest.md) |  |  |
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

<a id="validatedocumentapiv1documentsvalidatepost"></a>
# **ValidateDocumentApiV1DocumentsValidatePost**
> DocumentValidateResponse ValidateDocumentApiV1DocumentsValidatePost (DocumentValidateRequest documentValidateRequest)

Validate Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ValidateDocumentApiV1DocumentsValidatePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentValidateRequest = new DocumentValidateRequest(); // DocumentValidateRequest | 

            try
            {
                // Validate Document
                DocumentValidateResponse result = apiInstance.ValidateDocumentApiV1DocumentsValidatePost(documentValidateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.ValidateDocumentApiV1DocumentsValidatePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ValidateDocumentApiV1DocumentsValidatePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Validate Document
    ApiResponse<DocumentValidateResponse> response = apiInstance.ValidateDocumentApiV1DocumentsValidatePostWithHttpInfo(documentValidateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.ValidateDocumentApiV1DocumentsValidatePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentValidateRequest** | [**DocumentValidateRequest**](DocumentValidateRequest.md) |  |  |

### Return type

[**DocumentValidateResponse**](DocumentValidateResponse.md)

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

