# InvoicePDFs.Api.InvoicesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ArchiveInvoiceApiV1InvoicesInvoiceIdArchivePost**](InvoicesApi.md#archiveinvoiceapiv1invoicesinvoiceidarchivepost) | **POST** /api/v1/invoices/{invoice_id}/archive | Archive Invoice |
| [**CalculateInvoiceApiV1InvoicesCalculatePost**](InvoicesApi.md#calculateinvoiceapiv1invoicescalculatepost) | **POST** /api/v1/invoices/calculate | Calculate Invoice |
| [**CreateInvoiceApiV1InvoicesPost**](InvoicesApi.md#createinvoiceapiv1invoicespost) | **POST** /api/v1/invoices | Create Invoice |
| [**DeleteInvoiceApiV1InvoicesInvoiceIdDelete**](InvoicesApi.md#deleteinvoiceapiv1invoicesinvoiceiddelete) | **DELETE** /api/v1/invoices/{invoice_id} | Delete Invoice |
| [**DuplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost**](InvoicesApi.md#duplicateinvoiceapiv1invoicesinvoiceidduplicatepost) | **POST** /api/v1/invoices/{invoice_id}/duplicate | Duplicate Invoice |
| [**FinalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost**](InvoicesApi.md#finalizeinvoiceapiv1invoicesinvoiceidfinalizepost) | **POST** /api/v1/invoices/{invoice_id}/finalize | Finalize Invoice |
| [**GetInvoiceApiV1InvoicesInvoiceIdGet**](InvoicesApi.md#getinvoiceapiv1invoicesinvoiceidget) | **GET** /api/v1/invoices/{invoice_id} | Get Invoice |
| [**ListInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet**](InvoicesApi.md#listinvoicedeliveriesapiv1invoicesinvoiceiddeliveriesget) | **GET** /api/v1/invoices/{invoice_id}/deliveries | List Invoice Deliveries |
| [**ListInvoicesApiV1InvoicesGet**](InvoicesApi.md#listinvoicesapiv1invoicesget) | **GET** /api/v1/invoices | List Invoices |
| [**MarkPaidApiV1InvoicesInvoiceIdMarkPaidPost**](InvoicesApi.md#markpaidapiv1invoicesinvoiceidmarkpaidpost) | **POST** /api/v1/invoices/{invoice_id}/mark-paid | Mark Paid |
| [**MarkSentApiV1InvoicesInvoiceIdMarkSentPost**](InvoicesApi.md#marksentapiv1invoicesinvoiceidmarksentpost) | **POST** /api/v1/invoices/{invoice_id}/mark-sent | Mark Sent |
| [**MarkUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost**](InvoicesApi.md#markunpaidapiv1invoicesinvoiceidmarkunpaidpost) | **POST** /api/v1/invoices/{invoice_id}/mark-unpaid | Mark Unpaid |
| [**PatchInvoiceApiV1InvoicesInvoiceIdPatch**](InvoicesApi.md#patchinvoiceapiv1invoicesinvoiceidpatch) | **PATCH** /api/v1/invoices/{invoice_id} | Patch Invoice |
| [**PreviewInvoiceApiV1InvoicesPreviewPost**](InvoicesApi.md#previewinvoiceapiv1invoicespreviewpost) | **POST** /api/v1/invoices/preview | Preview Invoice |
| [**RenderInvoiceApiV1InvoicesInvoiceIdRendersPost**](InvoicesApi.md#renderinvoiceapiv1invoicesinvoiceidrenderspost) | **POST** /api/v1/invoices/{invoice_id}/renders | Render Invoice |
| [**ReplaceInvoiceApiV1InvoicesInvoiceIdPut**](InvoicesApi.md#replaceinvoiceapiv1invoicesinvoiceidput) | **PUT** /api/v1/invoices/{invoice_id} | Replace Invoice |
| [**RestoreInvoiceApiV1InvoicesInvoiceIdRestorePost**](InvoicesApi.md#restoreinvoiceapiv1invoicesinvoiceidrestorepost) | **POST** /api/v1/invoices/{invoice_id}/restore | Restore Invoice |
| [**SendInvoiceApiV1InvoicesInvoiceIdSendPost**](InvoicesApi.md#sendinvoiceapiv1invoicesinvoiceidsendpost) | **POST** /api/v1/invoices/{invoice_id}/send | Send Invoice |
| [**ValidateInvoiceApiV1InvoicesValidatePost**](InvoicesApi.md#validateinvoiceapiv1invoicesvalidatepost) | **POST** /api/v1/invoices/validate | Validate Invoice |
| [**VoidInvoiceApiV1InvoicesInvoiceIdVoidPost**](InvoicesApi.md#voidinvoiceapiv1invoicesinvoiceidvoidpost) | **POST** /api/v1/invoices/{invoice_id}/void | Void Invoice |

<a id="archiveinvoiceapiv1invoicesinvoiceidarchivepost"></a>
# **ArchiveInvoiceApiV1InvoicesInvoiceIdArchivePost**
> InvoiceResponse ArchiveInvoiceApiV1InvoicesInvoiceIdArchivePost (string invoiceId)

Archive Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ArchiveInvoiceApiV1InvoicesInvoiceIdArchivePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 

            try
            {
                // Archive Invoice
                InvoiceResponse result = apiInstance.ArchiveInvoiceApiV1InvoicesInvoiceIdArchivePost(invoiceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.ArchiveInvoiceApiV1InvoicesInvoiceIdArchivePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ArchiveInvoiceApiV1InvoicesInvoiceIdArchivePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Archive Invoice
    ApiResponse<InvoiceResponse> response = apiInstance.ArchiveInvoiceApiV1InvoicesInvoiceIdArchivePostWithHttpInfo(invoiceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.ArchiveInvoiceApiV1InvoicesInvoiceIdArchivePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="calculateinvoiceapiv1invoicescalculatepost"></a>
# **CalculateInvoiceApiV1InvoicesCalculatePost**
> Dictionary&lt;string, Object&gt; CalculateInvoiceApiV1InvoicesCalculatePost (InvoiceDraftRequest invoiceDraftRequest)

Calculate Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CalculateInvoiceApiV1InvoicesCalculatePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceDraftRequest = new InvoiceDraftRequest(); // InvoiceDraftRequest | 

            try
            {
                // Calculate Invoice
                Dictionary<string, Object> result = apiInstance.CalculateInvoiceApiV1InvoicesCalculatePost(invoiceDraftRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.CalculateInvoiceApiV1InvoicesCalculatePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CalculateInvoiceApiV1InvoicesCalculatePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Calculate Invoice
    ApiResponse<Dictionary<string, Object>> response = apiInstance.CalculateInvoiceApiV1InvoicesCalculatePostWithHttpInfo(invoiceDraftRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.CalculateInvoiceApiV1InvoicesCalculatePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceDraftRequest** | [**InvoiceDraftRequest**](InvoiceDraftRequest.md) |  |  |

### Return type

**Dictionary<string, Object>**

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

<a id="createinvoiceapiv1invoicespost"></a>
# **CreateInvoiceApiV1InvoicesPost**
> InvoiceResponse CreateInvoiceApiV1InvoicesPost (InvoiceCreateRequest invoiceCreateRequest, string? idempotencyKey = null)

Create Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateInvoiceApiV1InvoicesPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceCreateRequest = new InvoiceCreateRequest(); // InvoiceCreateRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Create Invoice
                InvoiceResponse result = apiInstance.CreateInvoiceApiV1InvoicesPost(invoiceCreateRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.CreateInvoiceApiV1InvoicesPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateInvoiceApiV1InvoicesPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Invoice
    ApiResponse<InvoiceResponse> response = apiInstance.CreateInvoiceApiV1InvoicesPostWithHttpInfo(invoiceCreateRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.CreateInvoiceApiV1InvoicesPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceCreateRequest** | [**InvoiceCreateRequest**](InvoiceCreateRequest.md) |  |  |
| **idempotencyKey** | **string?** |  | [optional]  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="deleteinvoiceapiv1invoicesinvoiceiddelete"></a>
# **DeleteInvoiceApiV1InvoicesInvoiceIdDelete**
> SimpleBoolResponse DeleteInvoiceApiV1InvoicesInvoiceIdDelete (string invoiceId)

Delete Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteInvoiceApiV1InvoicesInvoiceIdDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 

            try
            {
                // Delete Invoice
                SimpleBoolResponse result = apiInstance.DeleteInvoiceApiV1InvoicesInvoiceIdDelete(invoiceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.DeleteInvoiceApiV1InvoicesInvoiceIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteInvoiceApiV1InvoicesInvoiceIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Invoice
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteInvoiceApiV1InvoicesInvoiceIdDeleteWithHttpInfo(invoiceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.DeleteInvoiceApiV1InvoicesInvoiceIdDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |

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

<a id="duplicateinvoiceapiv1invoicesinvoiceidduplicatepost"></a>
# **DuplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost**
> InvoiceResponse DuplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost (string invoiceId)

Duplicate Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DuplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 

            try
            {
                // Duplicate Invoice
                InvoiceResponse result = apiInstance.DuplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost(invoiceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.DuplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DuplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Duplicate Invoice
    ApiResponse<InvoiceResponse> response = apiInstance.DuplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePostWithHttpInfo(invoiceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.DuplicateInvoiceApiV1InvoicesInvoiceIdDuplicatePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="finalizeinvoiceapiv1invoicesinvoiceidfinalizepost"></a>
# **FinalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost**
> Dictionary&lt;string, Object&gt; FinalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost (string invoiceId, string? idempotencyKey = null)

Finalize Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class FinalizeInvoiceApiV1InvoicesInvoiceIdFinalizePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Finalize Invoice
                Dictionary<string, Object> result = apiInstance.FinalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost(invoiceId, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.FinalizeInvoiceApiV1InvoicesInvoiceIdFinalizePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FinalizeInvoiceApiV1InvoicesInvoiceIdFinalizePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Finalize Invoice
    ApiResponse<Dictionary<string, Object>> response = apiInstance.FinalizeInvoiceApiV1InvoicesInvoiceIdFinalizePostWithHttpInfo(invoiceId, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.FinalizeInvoiceApiV1InvoicesInvoiceIdFinalizePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |
| **idempotencyKey** | **string?** |  | [optional]  |

### Return type

**Dictionary<string, Object>**

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

<a id="getinvoiceapiv1invoicesinvoiceidget"></a>
# **GetInvoiceApiV1InvoicesInvoiceIdGet**
> InvoiceResponse GetInvoiceApiV1InvoicesInvoiceIdGet (string invoiceId)

Get Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetInvoiceApiV1InvoicesInvoiceIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 

            try
            {
                // Get Invoice
                InvoiceResponse result = apiInstance.GetInvoiceApiV1InvoicesInvoiceIdGet(invoiceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.GetInvoiceApiV1InvoicesInvoiceIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInvoiceApiV1InvoicesInvoiceIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Invoice
    ApiResponse<InvoiceResponse> response = apiInstance.GetInvoiceApiV1InvoicesInvoiceIdGetWithHttpInfo(invoiceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.GetInvoiceApiV1InvoicesInvoiceIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="listinvoicedeliveriesapiv1invoicesinvoiceiddeliveriesget"></a>
# **ListInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet**
> DeliveriesListResponse ListInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet (string invoiceId, int? limit = null, string? cursor = null)

List Invoice Deliveries

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Invoice Deliveries
                DeliveriesListResponse result = apiInstance.ListInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet(invoiceId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.ListInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Invoice Deliveries
    ApiResponse<DeliveriesListResponse> response = apiInstance.ListInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGetWithHttpInfo(invoiceId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.ListInvoiceDeliveriesApiV1InvoicesInvoiceIdDeliveriesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |
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

<a id="listinvoicesapiv1invoicesget"></a>
# **ListInvoicesApiV1InvoicesGet**
> InvoicesListResponse ListInvoicesApiV1InvoicesGet (int? limit = null, string? cursor = null, string? status = null)

List Invoices

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListInvoicesApiV1InvoicesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 
            var status = "status_example";  // string? |  (optional) 

            try
            {
                // List Invoices
                InvoicesListResponse result = apiInstance.ListInvoicesApiV1InvoicesGet(limit, cursor, status);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.ListInvoicesApiV1InvoicesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListInvoicesApiV1InvoicesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Invoices
    ApiResponse<InvoicesListResponse> response = apiInstance.ListInvoicesApiV1InvoicesGetWithHttpInfo(limit, cursor, status);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.ListInvoicesApiV1InvoicesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** |  | [optional]  |
| **status** | **string?** |  | [optional]  |

### Return type

[**InvoicesListResponse**](InvoicesListResponse.md)

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

<a id="markpaidapiv1invoicesinvoiceidmarkpaidpost"></a>
# **MarkPaidApiV1InvoicesInvoiceIdMarkPaidPost**
> InvoiceResponse MarkPaidApiV1InvoicesInvoiceIdMarkPaidPost (string invoiceId)

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
    public class MarkPaidApiV1InvoicesInvoiceIdMarkPaidPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 

            try
            {
                // Mark Paid
                InvoiceResponse result = apiInstance.MarkPaidApiV1InvoicesInvoiceIdMarkPaidPost(invoiceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.MarkPaidApiV1InvoicesInvoiceIdMarkPaidPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MarkPaidApiV1InvoicesInvoiceIdMarkPaidPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mark Paid
    ApiResponse<InvoiceResponse> response = apiInstance.MarkPaidApiV1InvoicesInvoiceIdMarkPaidPostWithHttpInfo(invoiceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.MarkPaidApiV1InvoicesInvoiceIdMarkPaidPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="marksentapiv1invoicesinvoiceidmarksentpost"></a>
# **MarkSentApiV1InvoicesInvoiceIdMarkSentPost**
> InvoiceResponse MarkSentApiV1InvoicesInvoiceIdMarkSentPost (string invoiceId)

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
    public class MarkSentApiV1InvoicesInvoiceIdMarkSentPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 

            try
            {
                // Mark Sent
                InvoiceResponse result = apiInstance.MarkSentApiV1InvoicesInvoiceIdMarkSentPost(invoiceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.MarkSentApiV1InvoicesInvoiceIdMarkSentPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MarkSentApiV1InvoicesInvoiceIdMarkSentPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mark Sent
    ApiResponse<InvoiceResponse> response = apiInstance.MarkSentApiV1InvoicesInvoiceIdMarkSentPostWithHttpInfo(invoiceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.MarkSentApiV1InvoicesInvoiceIdMarkSentPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="markunpaidapiv1invoicesinvoiceidmarkunpaidpost"></a>
# **MarkUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost**
> InvoiceResponse MarkUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost (string invoiceId)

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
    public class MarkUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 

            try
            {
                // Mark Unpaid
                InvoiceResponse result = apiInstance.MarkUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost(invoiceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.MarkUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MarkUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Mark Unpaid
    ApiResponse<InvoiceResponse> response = apiInstance.MarkUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPostWithHttpInfo(invoiceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.MarkUnpaidApiV1InvoicesInvoiceIdMarkUnpaidPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="patchinvoiceapiv1invoicesinvoiceidpatch"></a>
# **PatchInvoiceApiV1InvoicesInvoiceIdPatch**
> InvoiceResponse PatchInvoiceApiV1InvoicesInvoiceIdPatch (string invoiceId, InvoicePatchRequest invoicePatchRequest, string? idempotencyKey = null)

Patch Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PatchInvoiceApiV1InvoicesInvoiceIdPatchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 
            var invoicePatchRequest = new InvoicePatchRequest(); // InvoicePatchRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Patch Invoice
                InvoiceResponse result = apiInstance.PatchInvoiceApiV1InvoicesInvoiceIdPatch(invoiceId, invoicePatchRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.PatchInvoiceApiV1InvoicesInvoiceIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PatchInvoiceApiV1InvoicesInvoiceIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Patch Invoice
    ApiResponse<InvoiceResponse> response = apiInstance.PatchInvoiceApiV1InvoicesInvoiceIdPatchWithHttpInfo(invoiceId, invoicePatchRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.PatchInvoiceApiV1InvoicesInvoiceIdPatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |
| **invoicePatchRequest** | [**InvoicePatchRequest**](InvoicePatchRequest.md) |  |  |
| **idempotencyKey** | **string?** |  | [optional]  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="previewinvoiceapiv1invoicespreviewpost"></a>
# **PreviewInvoiceApiV1InvoicesPreviewPost**
> Object PreviewInvoiceApiV1InvoicesPreviewPost (InvoicePreviewRequest invoicePreviewRequest)

Preview Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PreviewInvoiceApiV1InvoicesPreviewPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoicePreviewRequest = new InvoicePreviewRequest(); // InvoicePreviewRequest | 

            try
            {
                // Preview Invoice
                Object result = apiInstance.PreviewInvoiceApiV1InvoicesPreviewPost(invoicePreviewRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.PreviewInvoiceApiV1InvoicesPreviewPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PreviewInvoiceApiV1InvoicesPreviewPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Preview Invoice
    ApiResponse<Object> response = apiInstance.PreviewInvoiceApiV1InvoicesPreviewPostWithHttpInfo(invoicePreviewRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.PreviewInvoiceApiV1InvoicesPreviewPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoicePreviewRequest** | [**InvoicePreviewRequest**](InvoicePreviewRequest.md) |  |  |

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

<a id="renderinvoiceapiv1invoicesinvoiceidrenderspost"></a>
# **RenderInvoiceApiV1InvoicesInvoiceIdRendersPost**
> Object RenderInvoiceApiV1InvoicesInvoiceIdRendersPost (string invoiceId, InvoiceRenderRequest invoiceRenderRequest, string? idempotencyKey = null)

Render Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RenderInvoiceApiV1InvoicesInvoiceIdRendersPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 
            var invoiceRenderRequest = new InvoiceRenderRequest(); // InvoiceRenderRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Render Invoice
                Object result = apiInstance.RenderInvoiceApiV1InvoicesInvoiceIdRendersPost(invoiceId, invoiceRenderRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.RenderInvoiceApiV1InvoicesInvoiceIdRendersPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RenderInvoiceApiV1InvoicesInvoiceIdRendersPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Render Invoice
    ApiResponse<Object> response = apiInstance.RenderInvoiceApiV1InvoicesInvoiceIdRendersPostWithHttpInfo(invoiceId, invoiceRenderRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.RenderInvoiceApiV1InvoicesInvoiceIdRendersPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |
| **invoiceRenderRequest** | [**InvoiceRenderRequest**](InvoiceRenderRequest.md) |  |  |
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

<a id="replaceinvoiceapiv1invoicesinvoiceidput"></a>
# **ReplaceInvoiceApiV1InvoicesInvoiceIdPut**
> InvoiceResponse ReplaceInvoiceApiV1InvoicesInvoiceIdPut (string invoiceId, InvoiceCreateRequest invoiceCreateRequest, string? idempotencyKey = null)

Replace Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ReplaceInvoiceApiV1InvoicesInvoiceIdPutExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 
            var invoiceCreateRequest = new InvoiceCreateRequest(); // InvoiceCreateRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Replace Invoice
                InvoiceResponse result = apiInstance.ReplaceInvoiceApiV1InvoicesInvoiceIdPut(invoiceId, invoiceCreateRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.ReplaceInvoiceApiV1InvoicesInvoiceIdPut: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ReplaceInvoiceApiV1InvoicesInvoiceIdPutWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Replace Invoice
    ApiResponse<InvoiceResponse> response = apiInstance.ReplaceInvoiceApiV1InvoicesInvoiceIdPutWithHttpInfo(invoiceId, invoiceCreateRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.ReplaceInvoiceApiV1InvoicesInvoiceIdPutWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |
| **invoiceCreateRequest** | [**InvoiceCreateRequest**](InvoiceCreateRequest.md) |  |  |
| **idempotencyKey** | **string?** |  | [optional]  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="restoreinvoiceapiv1invoicesinvoiceidrestorepost"></a>
# **RestoreInvoiceApiV1InvoicesInvoiceIdRestorePost**
> InvoiceResponse RestoreInvoiceApiV1InvoicesInvoiceIdRestorePost (string invoiceId)

Restore Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RestoreInvoiceApiV1InvoicesInvoiceIdRestorePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 

            try
            {
                // Restore Invoice
                InvoiceResponse result = apiInstance.RestoreInvoiceApiV1InvoicesInvoiceIdRestorePost(invoiceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.RestoreInvoiceApiV1InvoicesInvoiceIdRestorePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestoreInvoiceApiV1InvoicesInvoiceIdRestorePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Restore Invoice
    ApiResponse<InvoiceResponse> response = apiInstance.RestoreInvoiceApiV1InvoicesInvoiceIdRestorePostWithHttpInfo(invoiceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.RestoreInvoiceApiV1InvoicesInvoiceIdRestorePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

<a id="sendinvoiceapiv1invoicesinvoiceidsendpost"></a>
# **SendInvoiceApiV1InvoicesInvoiceIdSendPost**
> DeliveryResponse SendInvoiceApiV1InvoicesInvoiceIdSendPost (string invoiceId, DeliverySendRequest deliverySendRequest)

Send Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class SendInvoiceApiV1InvoicesInvoiceIdSendPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 
            var deliverySendRequest = new DeliverySendRequest(); // DeliverySendRequest | 

            try
            {
                // Send Invoice
                DeliveryResponse result = apiInstance.SendInvoiceApiV1InvoicesInvoiceIdSendPost(invoiceId, deliverySendRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.SendInvoiceApiV1InvoicesInvoiceIdSendPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendInvoiceApiV1InvoicesInvoiceIdSendPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Send Invoice
    ApiResponse<DeliveryResponse> response = apiInstance.SendInvoiceApiV1InvoicesInvoiceIdSendPostWithHttpInfo(invoiceId, deliverySendRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.SendInvoiceApiV1InvoicesInvoiceIdSendPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |
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

<a id="validateinvoiceapiv1invoicesvalidatepost"></a>
# **ValidateInvoiceApiV1InvoicesValidatePost**
> Dictionary&lt;string, Object&gt; ValidateInvoiceApiV1InvoicesValidatePost (InvoiceDraftRequest invoiceDraftRequest)

Validate Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ValidateInvoiceApiV1InvoicesValidatePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceDraftRequest = new InvoiceDraftRequest(); // InvoiceDraftRequest | 

            try
            {
                // Validate Invoice
                Dictionary<string, Object> result = apiInstance.ValidateInvoiceApiV1InvoicesValidatePost(invoiceDraftRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.ValidateInvoiceApiV1InvoicesValidatePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ValidateInvoiceApiV1InvoicesValidatePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Validate Invoice
    ApiResponse<Dictionary<string, Object>> response = apiInstance.ValidateInvoiceApiV1InvoicesValidatePostWithHttpInfo(invoiceDraftRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.ValidateInvoiceApiV1InvoicesValidatePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceDraftRequest** | [**InvoiceDraftRequest**](InvoiceDraftRequest.md) |  |  |

### Return type

**Dictionary<string, Object>**

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

<a id="voidinvoiceapiv1invoicesinvoiceidvoidpost"></a>
# **VoidInvoiceApiV1InvoicesInvoiceIdVoidPost**
> InvoiceResponse VoidInvoiceApiV1InvoicesInvoiceIdVoidPost (string invoiceId)

Void Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class VoidInvoiceApiV1InvoicesInvoiceIdVoidPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new InvoicesApi(config);
            var invoiceId = "invoiceId_example";  // string | 

            try
            {
                // Void Invoice
                InvoiceResponse result = apiInstance.VoidInvoiceApiV1InvoicesInvoiceIdVoidPost(invoiceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvoicesApi.VoidInvoiceApiV1InvoicesInvoiceIdVoidPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VoidInvoiceApiV1InvoicesInvoiceIdVoidPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Void Invoice
    ApiResponse<InvoiceResponse> response = apiInstance.VoidInvoiceApiV1InvoicesInvoiceIdVoidPostWithHttpInfo(invoiceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvoicesApi.VoidInvoiceApiV1InvoicesInvoiceIdVoidPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

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

