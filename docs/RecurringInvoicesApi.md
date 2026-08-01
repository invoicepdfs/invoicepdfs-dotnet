# InvoicePDFs.Api.RecurringInvoicesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete**](RecurringInvoicesApi.md#cancelrecurringinvoiceapiv1recurringinvoicesrecurringiddelete) | **DELETE** /api/v1/recurring-invoices/{recurring_id} | Cancel Recurring Invoice |
| [**CreateRecurringInvoiceApiV1RecurringInvoicesPost**](RecurringInvoicesApi.md#createrecurringinvoiceapiv1recurringinvoicespost) | **POST** /api/v1/recurring-invoices | Create Recurring Invoice |
| [**GetRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet**](RecurringInvoicesApi.md#getrecurringinvoiceapiv1recurringinvoicesrecurringidget) | **GET** /api/v1/recurring-invoices/{recurring_id} | Get Recurring Invoice |
| [**ListGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet**](RecurringInvoicesApi.md#listgeneratedinvoicesapiv1recurringinvoicesrecurringidinvoicesget) | **GET** /api/v1/recurring-invoices/{recurring_id}/invoices | List Generated Invoices |
| [**ListRecurringInvoicesApiV1RecurringInvoicesGet**](RecurringInvoicesApi.md#listrecurringinvoicesapiv1recurringinvoicesget) | **GET** /api/v1/recurring-invoices | List Recurring Invoices |
| [**PatchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch**](RecurringInvoicesApi.md#patchrecurringinvoiceapiv1recurringinvoicesrecurringidpatch) | **PATCH** /api/v1/recurring-invoices/{recurring_id} | Patch Recurring Invoice |
| [**PauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost**](RecurringInvoicesApi.md#pauserecurringinvoiceapiv1recurringinvoicesrecurringidpausepost) | **POST** /api/v1/recurring-invoices/{recurring_id}/pause | Pause Recurring Invoice |
| [**ResumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost**](RecurringInvoicesApi.md#resumerecurringinvoiceapiv1recurringinvoicesrecurringidresumepost) | **POST** /api/v1/recurring-invoices/{recurring_id}/resume | Resume Recurring Invoice |

<a id="cancelrecurringinvoiceapiv1recurringinvoicesrecurringiddelete"></a>
# **CancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete**
> RecurringInvoiceResponse CancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete (string recurringId)

Cancel Recurring Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new RecurringInvoicesApi(config);
            var recurringId = "recurringId_example";  // string | 

            try
            {
                // Cancel Recurring Invoice
                RecurringInvoiceResponse result = apiInstance.CancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete(recurringId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.CancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancel Recurring Invoice
    ApiResponse<RecurringInvoiceResponse> response = apiInstance.CancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDeleteWithHttpInfo(recurringId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.CancelRecurringInvoiceApiV1RecurringInvoicesRecurringIdDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **recurringId** | **string** |  |  |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

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

<a id="createrecurringinvoiceapiv1recurringinvoicespost"></a>
# **CreateRecurringInvoiceApiV1RecurringInvoicesPost**
> RecurringInvoiceResponse CreateRecurringInvoiceApiV1RecurringInvoicesPost (RecurringInvoiceCreateRequest recurringInvoiceCreateRequest)

Create Recurring Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateRecurringInvoiceApiV1RecurringInvoicesPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new RecurringInvoicesApi(config);
            var recurringInvoiceCreateRequest = new RecurringInvoiceCreateRequest(); // RecurringInvoiceCreateRequest | 

            try
            {
                // Create Recurring Invoice
                RecurringInvoiceResponse result = apiInstance.CreateRecurringInvoiceApiV1RecurringInvoicesPost(recurringInvoiceCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.CreateRecurringInvoiceApiV1RecurringInvoicesPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateRecurringInvoiceApiV1RecurringInvoicesPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Recurring Invoice
    ApiResponse<RecurringInvoiceResponse> response = apiInstance.CreateRecurringInvoiceApiV1RecurringInvoicesPostWithHttpInfo(recurringInvoiceCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.CreateRecurringInvoiceApiV1RecurringInvoicesPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **recurringInvoiceCreateRequest** | [**RecurringInvoiceCreateRequest**](RecurringInvoiceCreateRequest.md) |  |  |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

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

<a id="getrecurringinvoiceapiv1recurringinvoicesrecurringidget"></a>
# **GetRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet**
> RecurringInvoiceResponse GetRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet (string recurringId)

Get Recurring Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetRecurringInvoiceApiV1RecurringInvoicesRecurringIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new RecurringInvoicesApi(config);
            var recurringId = "recurringId_example";  // string | 

            try
            {
                // Get Recurring Invoice
                RecurringInvoiceResponse result = apiInstance.GetRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet(recurringId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.GetRecurringInvoiceApiV1RecurringInvoicesRecurringIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRecurringInvoiceApiV1RecurringInvoicesRecurringIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Recurring Invoice
    ApiResponse<RecurringInvoiceResponse> response = apiInstance.GetRecurringInvoiceApiV1RecurringInvoicesRecurringIdGetWithHttpInfo(recurringId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.GetRecurringInvoiceApiV1RecurringInvoicesRecurringIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **recurringId** | **string** |  |  |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

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

<a id="listgeneratedinvoicesapiv1recurringinvoicesrecurringidinvoicesget"></a>
# **ListGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet**
> InvoicesListResponse ListGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet (string recurringId, int? limit = null, string? cursor = null)

List Generated Invoices

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new RecurringInvoicesApi(config);
            var recurringId = "recurringId_example";  // string | 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Generated Invoices
                InvoicesListResponse result = apiInstance.ListGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet(recurringId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.ListGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Generated Invoices
    ApiResponse<InvoicesListResponse> response = apiInstance.ListGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGetWithHttpInfo(recurringId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.ListGeneratedInvoicesApiV1RecurringInvoicesRecurringIdInvoicesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **recurringId** | **string** |  |  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** |  | [optional]  |

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

<a id="listrecurringinvoicesapiv1recurringinvoicesget"></a>
# **ListRecurringInvoicesApiV1RecurringInvoicesGet**
> RecurringInvoicesListResponse ListRecurringInvoicesApiV1RecurringInvoicesGet (int? limit = null, string? cursor = null, string? status = null)

List Recurring Invoices

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListRecurringInvoicesApiV1RecurringInvoicesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new RecurringInvoicesApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 
            var status = "status_example";  // string? |  (optional) 

            try
            {
                // List Recurring Invoices
                RecurringInvoicesListResponse result = apiInstance.ListRecurringInvoicesApiV1RecurringInvoicesGet(limit, cursor, status);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.ListRecurringInvoicesApiV1RecurringInvoicesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListRecurringInvoicesApiV1RecurringInvoicesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Recurring Invoices
    ApiResponse<RecurringInvoicesListResponse> response = apiInstance.ListRecurringInvoicesApiV1RecurringInvoicesGetWithHttpInfo(limit, cursor, status);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.ListRecurringInvoicesApiV1RecurringInvoicesGetWithHttpInfo: " + e.Message);
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

[**RecurringInvoicesListResponse**](RecurringInvoicesListResponse.md)

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

<a id="patchrecurringinvoiceapiv1recurringinvoicesrecurringidpatch"></a>
# **PatchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch**
> RecurringInvoiceResponse PatchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch (string recurringId, RecurringInvoicePatchRequest recurringInvoicePatchRequest)

Patch Recurring Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PatchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new RecurringInvoicesApi(config);
            var recurringId = "recurringId_example";  // string | 
            var recurringInvoicePatchRequest = new RecurringInvoicePatchRequest(); // RecurringInvoicePatchRequest | 

            try
            {
                // Patch Recurring Invoice
                RecurringInvoiceResponse result = apiInstance.PatchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch(recurringId, recurringInvoicePatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.PatchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PatchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Patch Recurring Invoice
    ApiResponse<RecurringInvoiceResponse> response = apiInstance.PatchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatchWithHttpInfo(recurringId, recurringInvoicePatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.PatchRecurringInvoiceApiV1RecurringInvoicesRecurringIdPatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **recurringId** | **string** |  |  |
| **recurringInvoicePatchRequest** | [**RecurringInvoicePatchRequest**](RecurringInvoicePatchRequest.md) |  |  |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

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

<a id="pauserecurringinvoiceapiv1recurringinvoicesrecurringidpausepost"></a>
# **PauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost**
> RecurringInvoiceResponse PauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost (string recurringId)

Pause Recurring Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new RecurringInvoicesApi(config);
            var recurringId = "recurringId_example";  // string | 

            try
            {
                // Pause Recurring Invoice
                RecurringInvoiceResponse result = apiInstance.PauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost(recurringId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.PauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pause Recurring Invoice
    ApiResponse<RecurringInvoiceResponse> response = apiInstance.PauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePostWithHttpInfo(recurringId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.PauseRecurringInvoiceApiV1RecurringInvoicesRecurringIdPausePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **recurringId** | **string** |  |  |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

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

<a id="resumerecurringinvoiceapiv1recurringinvoicesrecurringidresumepost"></a>
# **ResumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost**
> RecurringInvoiceResponse ResumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost (string recurringId)

Resume Recurring Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ResumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new RecurringInvoicesApi(config);
            var recurringId = "recurringId_example";  // string | 

            try
            {
                // Resume Recurring Invoice
                RecurringInvoiceResponse result = apiInstance.ResumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost(recurringId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.ResumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resume Recurring Invoice
    ApiResponse<RecurringInvoiceResponse> response = apiInstance.ResumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePostWithHttpInfo(recurringId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.ResumeRecurringInvoiceApiV1RecurringInvoicesRecurringIdResumePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **recurringId** | **string** |  |  |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

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

