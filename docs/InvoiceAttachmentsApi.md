# InvoicePDFs.Api.InvoiceAttachmentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateAttachmentApiV1DocumentsInvoiceIdAttachmentsPost**](InvoiceAttachmentsApi.md#createattachmentapiv1documentsinvoiceidattachmentspost) | **POST** /api/v1/documents/{invoice_id}/attachments | Create Attachment |
| [**DeleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete**](InvoiceAttachmentsApi.md#deleteattachmentapiv1documentsinvoiceidattachmentsattachmentiddelete) | **DELETE** /api/v1/documents/{invoice_id}/attachments/{attachment_id} | Delete Attachment |
| [**ListAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet**](InvoiceAttachmentsApi.md#listattachmentsapiv1documentsinvoiceidattachmentsget) | **GET** /api/v1/documents/{invoice_id}/attachments | List Attachments |

<a id="createattachmentapiv1documentsinvoiceidattachmentspost"></a>
# **CreateAttachmentApiV1DocumentsInvoiceIdAttachmentsPost**
> InvoiceAttachmentResponse CreateAttachmentApiV1DocumentsInvoiceIdAttachmentsPost (string invoiceId, InvoiceAttachmentCreateRequest invoiceAttachmentCreateRequest)

Create Attachment

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateAttachmentApiV1DocumentsInvoiceIdAttachmentsPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoiceAttachmentsApi(config);
            var invoiceId = "invoiceId_example";  // string | 
            var invoiceAttachmentCreateRequest = new InvoiceAttachmentCreateRequest(); // InvoiceAttachmentCreateRequest | 

            try
            {
                // Create Attachment
                InvoiceAttachmentResponse result = apiInstance.CreateAttachmentApiV1DocumentsInvoiceIdAttachmentsPost(invoiceId, invoiceAttachmentCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoiceAttachmentsApi.CreateAttachmentApiV1DocumentsInvoiceIdAttachmentsPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAttachmentApiV1DocumentsInvoiceIdAttachmentsPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Attachment
    ApiResponse<InvoiceAttachmentResponse> response = apiInstance.CreateAttachmentApiV1DocumentsInvoiceIdAttachmentsPostWithHttpInfo(invoiceId, invoiceAttachmentCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoiceAttachmentsApi.CreateAttachmentApiV1DocumentsInvoiceIdAttachmentsPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |
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

<a id="deleteattachmentapiv1documentsinvoiceidattachmentsattachmentiddelete"></a>
# **DeleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete**
> SimpleBoolResponse DeleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete (string invoiceId, string attachmentId)

Delete Attachment

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoiceAttachmentsApi(config);
            var invoiceId = "invoiceId_example";  // string | 
            var attachmentId = "attachmentId_example";  // string | 

            try
            {
                // Delete Attachment
                SimpleBoolResponse result = apiInstance.DeleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete(invoiceId, attachmentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoiceAttachmentsApi.DeleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Attachment
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDeleteWithHttpInfo(invoiceId, attachmentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoiceAttachmentsApi.DeleteAttachmentApiV1DocumentsInvoiceIdAttachmentsAttachmentIdDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |
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

<a id="listattachmentsapiv1documentsinvoiceidattachmentsget"></a>
# **ListAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet**
> InvoiceAttachmentsListResponse ListAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet (string invoiceId)

List Attachments

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListAttachmentsApiV1DocumentsInvoiceIdAttachmentsGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoiceAttachmentsApi(config);
            var invoiceId = "invoiceId_example";  // string | 

            try
            {
                // List Attachments
                InvoiceAttachmentsListResponse result = apiInstance.ListAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet(invoiceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoiceAttachmentsApi.ListAttachmentsApiV1DocumentsInvoiceIdAttachmentsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAttachmentsApiV1DocumentsInvoiceIdAttachmentsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Attachments
    ApiResponse<InvoiceAttachmentsListResponse> response = apiInstance.ListAttachmentsApiV1DocumentsInvoiceIdAttachmentsGetWithHttpInfo(invoiceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoiceAttachmentsApi.ListAttachmentsApiV1DocumentsInvoiceIdAttachmentsGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |

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

