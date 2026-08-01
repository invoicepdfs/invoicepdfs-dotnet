# InvoicePDFs.Api.DocumentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveDocumentApiV1DocumentsDocumentIdArchivePost**](DocumentsApi.md#archivedocumentapiv1documentsdocumentidarchivepost) | **POST** /api/v1/documents/{document_id}/archive | Archive Document |
| [**CalculateDocumentApiV1DocumentsCalculatePost**](DocumentsApi.md#calculatedocumentapiv1documentscalculatepost) | **POST** /api/v1/documents/calculate | Calculate Document |
| [**CreateDocumentApiV1DocumentsPost**](DocumentsApi.md#createdocumentapiv1documentspost) | **POST** /api/v1/documents | Create Document |
| [**DeleteDocumentApiV1DocumentsDocumentIdDelete**](DocumentsApi.md#deletedocumentapiv1documentsdocumentiddelete) | **DELETE** /api/v1/documents/{document_id} | Delete Document |
| [**DuplicateDocumentApiV1DocumentsDocumentIdDuplicatePost**](DocumentsApi.md#duplicatedocumentapiv1documentsdocumentidduplicatepost) | **POST** /api/v1/documents/{document_id}/duplicate | Duplicate Document |
| [**FinalizeDocumentApiV1DocumentsDocumentIdFinalizePost**](DocumentsApi.md#finalizedocumentapiv1documentsdocumentidfinalizepost) | **POST** /api/v1/documents/{document_id}/finalize | Finalize Document |
| [**GetDocumentApiV1DocumentsDocumentIdGet**](DocumentsApi.md#getdocumentapiv1documentsdocumentidget) | **GET** /api/v1/documents/{document_id} | Get Document |
| [**ListDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet**](DocumentsApi.md#listdocumentdeliveriesapiv1documentsdocumentiddeliveriesget) | **GET** /api/v1/documents/{document_id}/deliveries | List Document Deliveries |
| [**ListDocumentsApiV1DocumentsGet**](DocumentsApi.md#listdocumentsapiv1documentsget) | **GET** /api/v1/documents | List Documents |
| [**MarkPaidApiV1DocumentsDocumentIdMarkPaidPost**](DocumentsApi.md#markpaidapiv1documentsdocumentidmarkpaidpost) | **POST** /api/v1/documents/{document_id}/mark-paid | Mark Paid |
| [**MarkSentApiV1DocumentsDocumentIdMarkSentPost**](DocumentsApi.md#marksentapiv1documentsdocumentidmarksentpost) | **POST** /api/v1/documents/{document_id}/mark-sent | Mark Sent |
| [**MarkUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost**](DocumentsApi.md#markunpaidapiv1documentsdocumentidmarkunpaidpost) | **POST** /api/v1/documents/{document_id}/mark-unpaid | Mark Unpaid |
| [**PatchDocumentApiV1DocumentsDocumentIdPatch**](DocumentsApi.md#patchdocumentapiv1documentsdocumentidpatch) | **PATCH** /api/v1/documents/{document_id} | Patch Document |
| [**RenderDocumentApiV1DocumentsDocumentIdRendersPost**](DocumentsApi.md#renderdocumentapiv1documentsdocumentidrenderspost) | **POST** /api/v1/documents/{document_id}/renders | Render Document |
| [**RenderDocumentApiV1DocumentsRenderPost**](DocumentsApi.md#renderdocumentapiv1documentsrenderpost) | **POST** /api/v1/documents/render | Render Document |
| [**RestoreDocumentApiV1DocumentsDocumentIdRestorePost**](DocumentsApi.md#restoredocumentapiv1documentsdocumentidrestorepost) | **POST** /api/v1/documents/{document_id}/restore | Restore Document |
| [**SendDocumentApiV1DocumentsDocumentIdSendPost**](DocumentsApi.md#senddocumentapiv1documentsdocumentidsendpost) | **POST** /api/v1/documents/{document_id}/send | Send Document |
| [**ValidateDocumentApiV1DocumentsValidatePost**](DocumentsApi.md#validatedocumentapiv1documentsvalidatepost) | **POST** /api/v1/documents/validate | Validate Document |
| [**VoidDocumentApiV1DocumentsDocumentIdVoidPost**](DocumentsApi.md#voiddocumentapiv1documentsdocumentidvoidpost) | **POST** /api/v1/documents/{document_id}/void | Void Document |

<a id="archivedocumentapiv1documentsdocumentidarchivepost"></a>
# **ArchiveDocumentApiV1DocumentsDocumentIdArchivePost**
> DocumentResponse ArchiveDocumentApiV1DocumentsDocumentIdArchivePost (string documentId)

Archive Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ArchiveDocumentApiV1DocumentsDocumentIdArchivePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 

            try
            {
                // Archive Document
                DocumentResponse result = apiInstance.ArchiveDocumentApiV1DocumentsDocumentIdArchivePost(documentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.ArchiveDocumentApiV1DocumentsDocumentIdArchivePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveDocumentApiV1DocumentsDocumentIdArchivePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive Document
    ApiResponse<DocumentResponse> response = apiInstance.ArchiveDocumentApiV1DocumentsDocumentIdArchivePostWithHttpInfo(documentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.ArchiveDocumentApiV1DocumentsDocumentIdArchivePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="createdocumentapiv1documentspost"></a>
# **CreateDocumentApiV1DocumentsPost**
> DocumentResponse CreateDocumentApiV1DocumentsPost (DocumentCreateRequest documentCreateRequest, string? idempotencyKey = null)

Create Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateDocumentApiV1DocumentsPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentCreateRequest = new DocumentCreateRequest(); // DocumentCreateRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Create Document
                DocumentResponse result = apiInstance.CreateDocumentApiV1DocumentsPost(documentCreateRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.CreateDocumentApiV1DocumentsPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateDocumentApiV1DocumentsPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Document
    ApiResponse<DocumentResponse> response = apiInstance.CreateDocumentApiV1DocumentsPostWithHttpInfo(documentCreateRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.CreateDocumentApiV1DocumentsPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentCreateRequest** | [**DocumentCreateRequest**](DocumentCreateRequest.md) |  |  |
| **idempotencyKey** | **string?** |  | [optional]  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="deletedocumentapiv1documentsdocumentiddelete"></a>
# **DeleteDocumentApiV1DocumentsDocumentIdDelete**
> SimpleBoolResponse DeleteDocumentApiV1DocumentsDocumentIdDelete (string documentId)

Delete Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteDocumentApiV1DocumentsDocumentIdDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 

            try
            {
                // Delete Document
                SimpleBoolResponse result = apiInstance.DeleteDocumentApiV1DocumentsDocumentIdDelete(documentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.DeleteDocumentApiV1DocumentsDocumentIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteDocumentApiV1DocumentsDocumentIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Document
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteDocumentApiV1DocumentsDocumentIdDeleteWithHttpInfo(documentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.DeleteDocumentApiV1DocumentsDocumentIdDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |

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

<a id="duplicatedocumentapiv1documentsdocumentidduplicatepost"></a>
# **DuplicateDocumentApiV1DocumentsDocumentIdDuplicatePost**
> DocumentResponse DuplicateDocumentApiV1DocumentsDocumentIdDuplicatePost (string documentId)

Duplicate Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DuplicateDocumentApiV1DocumentsDocumentIdDuplicatePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 

            try
            {
                // Duplicate Document
                DocumentResponse result = apiInstance.DuplicateDocumentApiV1DocumentsDocumentIdDuplicatePost(documentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.DuplicateDocumentApiV1DocumentsDocumentIdDuplicatePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuplicateDocumentApiV1DocumentsDocumentIdDuplicatePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Duplicate Document
    ApiResponse<DocumentResponse> response = apiInstance.DuplicateDocumentApiV1DocumentsDocumentIdDuplicatePostWithHttpInfo(documentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.DuplicateDocumentApiV1DocumentsDocumentIdDuplicatePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="finalizedocumentapiv1documentsdocumentidfinalizepost"></a>
# **FinalizeDocumentApiV1DocumentsDocumentIdFinalizePost**
> DocumentResponse FinalizeDocumentApiV1DocumentsDocumentIdFinalizePost (string documentId)

Finalize Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class FinalizeDocumentApiV1DocumentsDocumentIdFinalizePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 

            try
            {
                // Finalize Document
                DocumentResponse result = apiInstance.FinalizeDocumentApiV1DocumentsDocumentIdFinalizePost(documentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.FinalizeDocumentApiV1DocumentsDocumentIdFinalizePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FinalizeDocumentApiV1DocumentsDocumentIdFinalizePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Finalize Document
    ApiResponse<DocumentResponse> response = apiInstance.FinalizeDocumentApiV1DocumentsDocumentIdFinalizePostWithHttpInfo(documentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.FinalizeDocumentApiV1DocumentsDocumentIdFinalizePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="getdocumentapiv1documentsdocumentidget"></a>
# **GetDocumentApiV1DocumentsDocumentIdGet**
> DocumentResponse GetDocumentApiV1DocumentsDocumentIdGet (string documentId)

Get Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetDocumentApiV1DocumentsDocumentIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 

            try
            {
                // Get Document
                DocumentResponse result = apiInstance.GetDocumentApiV1DocumentsDocumentIdGet(documentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.GetDocumentApiV1DocumentsDocumentIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDocumentApiV1DocumentsDocumentIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Document
    ApiResponse<DocumentResponse> response = apiInstance.GetDocumentApiV1DocumentsDocumentIdGetWithHttpInfo(documentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.GetDocumentApiV1DocumentsDocumentIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="listdocumentdeliveriesapiv1documentsdocumentiddeliveriesget"></a>
# **ListDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet**
> DeliveriesListResponse ListDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet (string documentId, int? limit = null, string? cursor = null)

List Document Deliveries

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Document Deliveries
                DeliveriesListResponse result = apiInstance.ListDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet(documentId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.ListDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Document Deliveries
    ApiResponse<DeliveriesListResponse> response = apiInstance.ListDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGetWithHttpInfo(documentId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.ListDocumentDeliveriesApiV1DocumentsDocumentIdDeliveriesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** |  | [optional]  |

### Return type

[**DeliveriesListResponse**](DeliveriesListResponse.md)

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

<a id="listdocumentsapiv1documentsget"></a>
# **ListDocumentsApiV1DocumentsGet**
> DocumentsListResponse ListDocumentsApiV1DocumentsGet (int? limit = null, string? cursor = null, string? documentType = null, string? status = null)

List Documents

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListDocumentsApiV1DocumentsGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 
            var documentType = "documentType_example";  // string? |  (optional) 
            var status = "status_example";  // string? |  (optional) 

            try
            {
                // List Documents
                DocumentsListResponse result = apiInstance.ListDocumentsApiV1DocumentsGet(limit, cursor, documentType, status);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.ListDocumentsApiV1DocumentsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListDocumentsApiV1DocumentsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Documents
    ApiResponse<DocumentsListResponse> response = apiInstance.ListDocumentsApiV1DocumentsGetWithHttpInfo(limit, cursor, documentType, status);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.ListDocumentsApiV1DocumentsGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** |  | [optional]  |
| **documentType** | **string?** |  | [optional]  |
| **status** | **string?** |  | [optional]  |

### Return type

[**DocumentsListResponse**](DocumentsListResponse.md)

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

<a id="markpaidapiv1documentsdocumentidmarkpaidpost"></a>
# **MarkPaidApiV1DocumentsDocumentIdMarkPaidPost**
> DocumentResponse MarkPaidApiV1DocumentsDocumentIdMarkPaidPost (string documentId)

Mark Paid

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class MarkPaidApiV1DocumentsDocumentIdMarkPaidPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 

            try
            {
                // Mark Paid
                DocumentResponse result = apiInstance.MarkPaidApiV1DocumentsDocumentIdMarkPaidPost(documentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.MarkPaidApiV1DocumentsDocumentIdMarkPaidPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MarkPaidApiV1DocumentsDocumentIdMarkPaidPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mark Paid
    ApiResponse<DocumentResponse> response = apiInstance.MarkPaidApiV1DocumentsDocumentIdMarkPaidPostWithHttpInfo(documentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.MarkPaidApiV1DocumentsDocumentIdMarkPaidPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="marksentapiv1documentsdocumentidmarksentpost"></a>
# **MarkSentApiV1DocumentsDocumentIdMarkSentPost**
> DocumentResponse MarkSentApiV1DocumentsDocumentIdMarkSentPost (string documentId)

Mark Sent

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class MarkSentApiV1DocumentsDocumentIdMarkSentPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 

            try
            {
                // Mark Sent
                DocumentResponse result = apiInstance.MarkSentApiV1DocumentsDocumentIdMarkSentPost(documentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.MarkSentApiV1DocumentsDocumentIdMarkSentPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MarkSentApiV1DocumentsDocumentIdMarkSentPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mark Sent
    ApiResponse<DocumentResponse> response = apiInstance.MarkSentApiV1DocumentsDocumentIdMarkSentPostWithHttpInfo(documentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.MarkSentApiV1DocumentsDocumentIdMarkSentPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="markunpaidapiv1documentsdocumentidmarkunpaidpost"></a>
# **MarkUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost**
> DocumentResponse MarkUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost (string documentId)

Mark Unpaid

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class MarkUnpaidApiV1DocumentsDocumentIdMarkUnpaidPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 

            try
            {
                // Mark Unpaid
                DocumentResponse result = apiInstance.MarkUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost(documentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.MarkUnpaidApiV1DocumentsDocumentIdMarkUnpaidPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MarkUnpaidApiV1DocumentsDocumentIdMarkUnpaidPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mark Unpaid
    ApiResponse<DocumentResponse> response = apiInstance.MarkUnpaidApiV1DocumentsDocumentIdMarkUnpaidPostWithHttpInfo(documentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.MarkUnpaidApiV1DocumentsDocumentIdMarkUnpaidPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="patchdocumentapiv1documentsdocumentidpatch"></a>
# **PatchDocumentApiV1DocumentsDocumentIdPatch**
> DocumentResponse PatchDocumentApiV1DocumentsDocumentIdPatch (string documentId, DocumentPatchRequest documentPatchRequest)

Patch Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PatchDocumentApiV1DocumentsDocumentIdPatchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 
            var documentPatchRequest = new DocumentPatchRequest(); // DocumentPatchRequest | 

            try
            {
                // Patch Document
                DocumentResponse result = apiInstance.PatchDocumentApiV1DocumentsDocumentIdPatch(documentId, documentPatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.PatchDocumentApiV1DocumentsDocumentIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PatchDocumentApiV1DocumentsDocumentIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Patch Document
    ApiResponse<DocumentResponse> response = apiInstance.PatchDocumentApiV1DocumentsDocumentIdPatchWithHttpInfo(documentId, documentPatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.PatchDocumentApiV1DocumentsDocumentIdPatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |
| **documentPatchRequest** | [**DocumentPatchRequest**](DocumentPatchRequest.md) |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="renderdocumentapiv1documentsdocumentidrenderspost"></a>
# **RenderDocumentApiV1DocumentsDocumentIdRendersPost**
> Object RenderDocumentApiV1DocumentsDocumentIdRendersPost (string documentId, AppDocumentsSchemasDocumentRenderRequest appDocumentsSchemasDocumentRenderRequest, string? idempotencyKey = null)

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
    public class RenderDocumentApiV1DocumentsDocumentIdRendersPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 
            var appDocumentsSchemasDocumentRenderRequest = new AppDocumentsSchemasDocumentRenderRequest(); // AppDocumentsSchemasDocumentRenderRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Render Document
                Object result = apiInstance.RenderDocumentApiV1DocumentsDocumentIdRendersPost(documentId, appDocumentsSchemasDocumentRenderRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.RenderDocumentApiV1DocumentsDocumentIdRendersPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RenderDocumentApiV1DocumentsDocumentIdRendersPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Render Document
    ApiResponse<Object> response = apiInstance.RenderDocumentApiV1DocumentsDocumentIdRendersPostWithHttpInfo(documentId, appDocumentsSchemasDocumentRenderRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.RenderDocumentApiV1DocumentsDocumentIdRendersPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |
| **appDocumentsSchemasDocumentRenderRequest** | [**AppDocumentsSchemasDocumentRenderRequest**](AppDocumentsSchemasDocumentRenderRequest.md) |  |  |
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

<a id="renderdocumentapiv1documentsrenderpost"></a>
# **RenderDocumentApiV1DocumentsRenderPost**
> Object RenderDocumentApiV1DocumentsRenderPost (AppSchemasV1DocumentRenderRequest appSchemasV1DocumentRenderRequest, string? idempotencyKey = null)

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
            var appSchemasV1DocumentRenderRequest = new AppSchemasV1DocumentRenderRequest(); // AppSchemasV1DocumentRenderRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Render Document
                Object result = apiInstance.RenderDocumentApiV1DocumentsRenderPost(appSchemasV1DocumentRenderRequest, idempotencyKey);
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
    ApiResponse<Object> response = apiInstance.RenderDocumentApiV1DocumentsRenderPostWithHttpInfo(appSchemasV1DocumentRenderRequest, idempotencyKey);
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

<a id="restoredocumentapiv1documentsdocumentidrestorepost"></a>
# **RestoreDocumentApiV1DocumentsDocumentIdRestorePost**
> DocumentResponse RestoreDocumentApiV1DocumentsDocumentIdRestorePost (string documentId)

Restore Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RestoreDocumentApiV1DocumentsDocumentIdRestorePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 

            try
            {
                // Restore Document
                DocumentResponse result = apiInstance.RestoreDocumentApiV1DocumentsDocumentIdRestorePost(documentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.RestoreDocumentApiV1DocumentsDocumentIdRestorePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreDocumentApiV1DocumentsDocumentIdRestorePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore Document
    ApiResponse<DocumentResponse> response = apiInstance.RestoreDocumentApiV1DocumentsDocumentIdRestorePostWithHttpInfo(documentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.RestoreDocumentApiV1DocumentsDocumentIdRestorePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

<a id="senddocumentapiv1documentsdocumentidsendpost"></a>
# **SendDocumentApiV1DocumentsDocumentIdSendPost**
> DeliveryResponse SendDocumentApiV1DocumentsDocumentIdSendPost (string documentId, DeliverySendRequest deliverySendRequest)

Send Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class SendDocumentApiV1DocumentsDocumentIdSendPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 
            var deliverySendRequest = new DeliverySendRequest(); // DeliverySendRequest | 

            try
            {
                // Send Document
                DeliveryResponse result = apiInstance.SendDocumentApiV1DocumentsDocumentIdSendPost(documentId, deliverySendRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.SendDocumentApiV1DocumentsDocumentIdSendPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendDocumentApiV1DocumentsDocumentIdSendPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send Document
    ApiResponse<DeliveryResponse> response = apiInstance.SendDocumentApiV1DocumentsDocumentIdSendPostWithHttpInfo(documentId, deliverySendRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.SendDocumentApiV1DocumentsDocumentIdSendPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |
| **deliverySendRequest** | [**DeliverySendRequest**](DeliverySendRequest.md) |  |  |

### Return type

[**DeliveryResponse**](DeliveryResponse.md)

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

<a id="voiddocumentapiv1documentsdocumentidvoidpost"></a>
# **VoidDocumentApiV1DocumentsDocumentIdVoidPost**
> DocumentResponse VoidDocumentApiV1DocumentsDocumentIdVoidPost (string documentId)

Void Document

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class VoidDocumentApiV1DocumentsDocumentIdVoidPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentsApi(config);
            var documentId = "documentId_example";  // string | 

            try
            {
                // Void Document
                DocumentResponse result = apiInstance.VoidDocumentApiV1DocumentsDocumentIdVoidPost(documentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentsApi.VoidDocumentApiV1DocumentsDocumentIdVoidPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VoidDocumentApiV1DocumentsDocumentIdVoidPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Void Document
    ApiResponse<DocumentResponse> response = apiInstance.VoidDocumentApiV1DocumentsDocumentIdVoidPostWithHttpInfo(documentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentsApi.VoidDocumentApiV1DocumentsDocumentIdVoidPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

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

