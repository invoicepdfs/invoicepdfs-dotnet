# InvoicePDFs.Api.DocumentAttachmentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateDocumentAttachment**](DocumentAttachmentsApi.md#createdocumentattachment) | **POST** /api/v1/documents/{document_id}/attachments | Create Document Attachment |
| [**DeleteDocumentAttachment**](DocumentAttachmentsApi.md#deletedocumentattachment) | **DELETE** /api/v1/documents/{document_id}/attachments/{attachment_id} | Delete Document Attachment |
| [**ListDocumentAttachments**](DocumentAttachmentsApi.md#listdocumentattachments) | **GET** /api/v1/documents/{document_id}/attachments | List Document Attachments |

<a id="createdocumentattachment"></a>
# **CreateDocumentAttachment**
> InvoiceAttachmentResponse CreateDocumentAttachment (string documentId, InvoiceAttachmentCreateRequest invoiceAttachmentCreateRequest)

Create Document Attachment

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateDocumentAttachmentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentAttachmentsApi(config);
            var documentId = "documentId_example";  // string | 
            var invoiceAttachmentCreateRequest = new InvoiceAttachmentCreateRequest(); // InvoiceAttachmentCreateRequest | 

            try
            {
                // Create Document Attachment
                InvoiceAttachmentResponse result = apiInstance.CreateDocumentAttachment(documentId, invoiceAttachmentCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentAttachmentsApi.CreateDocumentAttachment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateDocumentAttachmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Document Attachment
    ApiResponse<InvoiceAttachmentResponse> response = apiInstance.CreateDocumentAttachmentWithHttpInfo(documentId, invoiceAttachmentCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentAttachmentsApi.CreateDocumentAttachmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |
| **invoiceAttachmentCreateRequest** | [**InvoiceAttachmentCreateRequest**](InvoiceAttachmentCreateRequest.md) |  |  |

### Return type

[**InvoiceAttachmentResponse**](InvoiceAttachmentResponse.md)

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

<a id="deletedocumentattachment"></a>
# **DeleteDocumentAttachment**
> SimpleBoolResponse DeleteDocumentAttachment (string documentId, string attachmentId)

Delete Document Attachment

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteDocumentAttachmentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentAttachmentsApi(config);
            var documentId = "documentId_example";  // string | 
            var attachmentId = "attachmentId_example";  // string | 

            try
            {
                // Delete Document Attachment
                SimpleBoolResponse result = apiInstance.DeleteDocumentAttachment(documentId, attachmentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentAttachmentsApi.DeleteDocumentAttachment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteDocumentAttachmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Document Attachment
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteDocumentAttachmentWithHttpInfo(documentId, attachmentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentAttachmentsApi.DeleteDocumentAttachmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |
| **attachmentId** | **string** |  |  |

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

<a id="listdocumentattachments"></a>
# **ListDocumentAttachments**
> InvoiceAttachmentsListResponse ListDocumentAttachments (string documentId)

List Document Attachments

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListDocumentAttachmentsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DocumentAttachmentsApi(config);
            var documentId = "documentId_example";  // string | 

            try
            {
                // List Document Attachments
                InvoiceAttachmentsListResponse result = apiInstance.ListDocumentAttachments(documentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DocumentAttachmentsApi.ListDocumentAttachments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListDocumentAttachmentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Document Attachments
    ApiResponse<InvoiceAttachmentsListResponse> response = apiInstance.ListDocumentAttachmentsWithHttpInfo(documentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DocumentAttachmentsApi.ListDocumentAttachmentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |

### Return type

[**InvoiceAttachmentsListResponse**](InvoiceAttachmentsListResponse.md)

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

