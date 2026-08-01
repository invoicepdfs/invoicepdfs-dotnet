# InvoicePDFs.Api.InvoiceAttachmentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateAttachmentApiV1InvoicesInvoiceIdAttachmentsPost**](InvoiceAttachmentsApi.md#createattachmentapiv1invoicesinvoiceidattachmentspost) | **POST** /api/v1/invoices/{invoice_id}/attachments | Create Attachment |
| [**DeleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete**](InvoiceAttachmentsApi.md#deleteattachmentapiv1invoicesinvoiceidattachmentsattachmentiddelete) | **DELETE** /api/v1/invoices/{invoice_id}/attachments/{attachment_id} | Delete Attachment |
| [**ListAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet**](InvoiceAttachmentsApi.md#listattachmentsapiv1invoicesinvoiceidattachmentsget) | **GET** /api/v1/invoices/{invoice_id}/attachments | List Attachments |

<a id="createattachmentapiv1invoicesinvoiceidattachmentspost"></a>
# **CreateAttachmentApiV1InvoicesInvoiceIdAttachmentsPost**
> InvoiceAttachmentResponse CreateAttachmentApiV1InvoicesInvoiceIdAttachmentsPost (string invoiceId, InvoiceAttachmentCreateRequest invoiceAttachmentCreateRequest)

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
    public class CreateAttachmentApiV1InvoicesInvoiceIdAttachmentsPostExample
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
                InvoiceAttachmentResponse result = apiInstance.CreateAttachmentApiV1InvoicesInvoiceIdAttachmentsPost(invoiceId, invoiceAttachmentCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoiceAttachmentsApi.CreateAttachmentApiV1InvoicesInvoiceIdAttachmentsPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAttachmentApiV1InvoicesInvoiceIdAttachmentsPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Attachment
    ApiResponse<InvoiceAttachmentResponse> response = apiInstance.CreateAttachmentApiV1InvoicesInvoiceIdAttachmentsPostWithHttpInfo(invoiceId, invoiceAttachmentCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoiceAttachmentsApi.CreateAttachmentApiV1InvoicesInvoiceIdAttachmentsPostWithHttpInfo: " + e.Message);
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

<a id="deleteattachmentapiv1invoicesinvoiceidattachmentsattachmentiddelete"></a>
# **DeleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete**
> SimpleBoolResponse DeleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete (string invoiceId, string attachmentId)

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
    public class DeleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDeleteExample
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
                SimpleBoolResponse result = apiInstance.DeleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete(invoiceId, attachmentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoiceAttachmentsApi.DeleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Attachment
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDeleteWithHttpInfo(invoiceId, attachmentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoiceAttachmentsApi.DeleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDeleteWithHttpInfo: " + e.Message);
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

<a id="listattachmentsapiv1invoicesinvoiceidattachmentsget"></a>
# **ListAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet**
> InvoiceAttachmentsListResponse ListAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet (string invoiceId)

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
    public class ListAttachmentsApiV1InvoicesInvoiceIdAttachmentsGetExample
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
                InvoiceAttachmentsListResponse result = apiInstance.ListAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet(invoiceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoiceAttachmentsApi.ListAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAttachmentsApiV1InvoicesInvoiceIdAttachmentsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Attachments
    ApiResponse<InvoiceAttachmentsListResponse> response = apiInstance.ListAttachmentsApiV1InvoicesInvoiceIdAttachmentsGetWithHttpInfo(invoiceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoiceAttachmentsApi.ListAttachmentsApiV1InvoicesInvoiceIdAttachmentsGetWithHttpInfo: " + e.Message);
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

