# InvoicePDFs.Api.RecurringInvoicesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CancelRecurringInvoice**](RecurringInvoicesApi.md#cancelrecurringinvoice) | **DELETE** /api/v1/recurring-invoices/{recurring_id} | Cancel Recurring Invoice |
| [**CreateRecurringInvoice**](RecurringInvoicesApi.md#createrecurringinvoice) | **POST** /api/v1/recurring-invoices | Create Recurring Invoice |
| [**GetRecurringInvoice**](RecurringInvoicesApi.md#getrecurringinvoice) | **GET** /api/v1/recurring-invoices/{recurring_id} | Get Recurring Invoice |
| [**ListGeneratedInvoices**](RecurringInvoicesApi.md#listgeneratedinvoices) | **GET** /api/v1/recurring-invoices/{recurring_id}/invoices | List Generated Invoices |
| [**ListRecurringInvoices**](RecurringInvoicesApi.md#listrecurringinvoices) | **GET** /api/v1/recurring-invoices | List Recurring Invoices |
| [**PauseRecurringInvoice**](RecurringInvoicesApi.md#pauserecurringinvoice) | **POST** /api/v1/recurring-invoices/{recurring_id}/pause | Pause Recurring Invoice |
| [**ResumeRecurringInvoice**](RecurringInvoicesApi.md#resumerecurringinvoice) | **POST** /api/v1/recurring-invoices/{recurring_id}/resume | Resume Recurring Invoice |
| [**UpdateRecurringInvoice**](RecurringInvoicesApi.md#updaterecurringinvoice) | **PATCH** /api/v1/recurring-invoices/{recurring_id} | Update Recurring Invoice |

<a id="cancelrecurringinvoice"></a>
# **CancelRecurringInvoice**
> RecurringInvoiceResponse CancelRecurringInvoice (string recurringId)

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
    public class CancelRecurringInvoiceExample
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
                RecurringInvoiceResponse result = apiInstance.CancelRecurringInvoice(recurringId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.CancelRecurringInvoice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelRecurringInvoiceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancel Recurring Invoice
    ApiResponse<RecurringInvoiceResponse> response = apiInstance.CancelRecurringInvoiceWithHttpInfo(recurringId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.CancelRecurringInvoiceWithHttpInfo: " + e.Message);
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

<a id="createrecurringinvoice"></a>
# **CreateRecurringInvoice**
> RecurringInvoiceResponse CreateRecurringInvoice (RecurringInvoiceCreateRequest recurringInvoiceCreateRequest)

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
    public class CreateRecurringInvoiceExample
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
                RecurringInvoiceResponse result = apiInstance.CreateRecurringInvoice(recurringInvoiceCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.CreateRecurringInvoice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateRecurringInvoiceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Recurring Invoice
    ApiResponse<RecurringInvoiceResponse> response = apiInstance.CreateRecurringInvoiceWithHttpInfo(recurringInvoiceCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.CreateRecurringInvoiceWithHttpInfo: " + e.Message);
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

<a id="getrecurringinvoice"></a>
# **GetRecurringInvoice**
> RecurringInvoiceResponse GetRecurringInvoice (string recurringId)

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
    public class GetRecurringInvoiceExample
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
                RecurringInvoiceResponse result = apiInstance.GetRecurringInvoice(recurringId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.GetRecurringInvoice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRecurringInvoiceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Recurring Invoice
    ApiResponse<RecurringInvoiceResponse> response = apiInstance.GetRecurringInvoiceWithHttpInfo(recurringId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.GetRecurringInvoiceWithHttpInfo: " + e.Message);
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

<a id="listgeneratedinvoices"></a>
# **ListGeneratedInvoices**
> InvoicesListResponse ListGeneratedInvoices (string recurringId, int? limit = null, string? cursor = null)

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
    public class ListGeneratedInvoicesExample
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
                InvoicesListResponse result = apiInstance.ListGeneratedInvoices(recurringId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.ListGeneratedInvoices: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListGeneratedInvoicesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Generated Invoices
    ApiResponse<InvoicesListResponse> response = apiInstance.ListGeneratedInvoicesWithHttpInfo(recurringId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.ListGeneratedInvoicesWithHttpInfo: " + e.Message);
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

<a id="listrecurringinvoices"></a>
# **ListRecurringInvoices**
> RecurringInvoicesListResponse ListRecurringInvoices (int? limit = null, string? cursor = null, string? status = null)

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
    public class ListRecurringInvoicesExample
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
                RecurringInvoicesListResponse result = apiInstance.ListRecurringInvoices(limit, cursor, status);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.ListRecurringInvoices: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListRecurringInvoicesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Recurring Invoices
    ApiResponse<RecurringInvoicesListResponse> response = apiInstance.ListRecurringInvoicesWithHttpInfo(limit, cursor, status);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.ListRecurringInvoicesWithHttpInfo: " + e.Message);
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

<a id="pauserecurringinvoice"></a>
# **PauseRecurringInvoice**
> RecurringInvoiceResponse PauseRecurringInvoice (string recurringId)

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
    public class PauseRecurringInvoiceExample
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
                RecurringInvoiceResponse result = apiInstance.PauseRecurringInvoice(recurringId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.PauseRecurringInvoice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PauseRecurringInvoiceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Pause Recurring Invoice
    ApiResponse<RecurringInvoiceResponse> response = apiInstance.PauseRecurringInvoiceWithHttpInfo(recurringId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.PauseRecurringInvoiceWithHttpInfo: " + e.Message);
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

<a id="resumerecurringinvoice"></a>
# **ResumeRecurringInvoice**
> RecurringInvoiceResponse ResumeRecurringInvoice (string recurringId)

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
    public class ResumeRecurringInvoiceExample
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
                RecurringInvoiceResponse result = apiInstance.ResumeRecurringInvoice(recurringId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.ResumeRecurringInvoice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResumeRecurringInvoiceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resume Recurring Invoice
    ApiResponse<RecurringInvoiceResponse> response = apiInstance.ResumeRecurringInvoiceWithHttpInfo(recurringId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.ResumeRecurringInvoiceWithHttpInfo: " + e.Message);
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

<a id="updaterecurringinvoice"></a>
# **UpdateRecurringInvoice**
> RecurringInvoiceResponse UpdateRecurringInvoice (string recurringId, RecurringInvoicePatchRequest recurringInvoicePatchRequest)

Update Recurring Invoice

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UpdateRecurringInvoiceExample
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
                // Update Recurring Invoice
                RecurringInvoiceResponse result = apiInstance.UpdateRecurringInvoice(recurringId, recurringInvoicePatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RecurringInvoicesApi.UpdateRecurringInvoice: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateRecurringInvoiceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Recurring Invoice
    ApiResponse<RecurringInvoiceResponse> response = apiInstance.UpdateRecurringInvoiceWithHttpInfo(recurringId, recurringInvoicePatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RecurringInvoicesApi.UpdateRecurringInvoiceWithHttpInfo: " + e.Message);
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

