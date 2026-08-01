# InvoicePDFs.Api.CreditNotesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateCreditNoteApiV1CreditNotesPost**](CreditNotesApi.md#createcreditnoteapiv1creditnotespost) | **POST** /api/v1/credit-notes | Create Credit Note |
| [**FinalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost**](CreditNotesApi.md#finalizecreditnoteapiv1creditnotescreditnoteidfinalizepost) | **POST** /api/v1/credit-notes/{credit_note_id}/finalize | Finalize Credit Note |
| [**GetCreditNoteApiV1CreditNotesCreditNoteIdGet**](CreditNotesApi.md#getcreditnoteapiv1creditnotescreditnoteidget) | **GET** /api/v1/credit-notes/{credit_note_id} | Get Credit Note |
| [**ListCreditNotesApiV1CreditNotesGet**](CreditNotesApi.md#listcreditnotesapiv1creditnotesget) | **GET** /api/v1/credit-notes | List Credit Notes |
| [**RenderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost**](CreditNotesApi.md#rendercreditnoteapiv1creditnotescreditnoteidrenderspost) | **POST** /api/v1/credit-notes/{credit_note_id}/renders | Render Credit Note |

<a id="createcreditnoteapiv1creditnotespost"></a>
# **CreateCreditNoteApiV1CreditNotesPost**
> CreditNoteResponse CreateCreditNoteApiV1CreditNotesPost (CreditNoteCreateRequest creditNoteCreateRequest)

Create Credit Note

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateCreditNoteApiV1CreditNotesPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CreditNotesApi(config);
            var creditNoteCreateRequest = new CreditNoteCreateRequest(); // CreditNoteCreateRequest | 

            try
            {
                // Create Credit Note
                CreditNoteResponse result = apiInstance.CreateCreditNoteApiV1CreditNotesPost(creditNoteCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreditNotesApi.CreateCreditNoteApiV1CreditNotesPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCreditNoteApiV1CreditNotesPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Credit Note
    ApiResponse<CreditNoteResponse> response = apiInstance.CreateCreditNoteApiV1CreditNotesPostWithHttpInfo(creditNoteCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreditNotesApi.CreateCreditNoteApiV1CreditNotesPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **creditNoteCreateRequest** | [**CreditNoteCreateRequest**](CreditNoteCreateRequest.md) |  |  |

### Return type

[**CreditNoteResponse**](CreditNoteResponse.md)

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

<a id="finalizecreditnoteapiv1creditnotescreditnoteidfinalizepost"></a>
# **FinalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost**
> CreditNoteResponse FinalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost (string creditNoteId)

Finalize Credit Note

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class FinalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CreditNotesApi(config);
            var creditNoteId = "creditNoteId_example";  // string | 

            try
            {
                // Finalize Credit Note
                CreditNoteResponse result = apiInstance.FinalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost(creditNoteId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreditNotesApi.FinalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FinalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Finalize Credit Note
    ApiResponse<CreditNoteResponse> response = apiInstance.FinalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePostWithHttpInfo(creditNoteId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreditNotesApi.FinalizeCreditNoteApiV1CreditNotesCreditNoteIdFinalizePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **creditNoteId** | **string** |  |  |

### Return type

[**CreditNoteResponse**](CreditNoteResponse.md)

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

<a id="getcreditnoteapiv1creditnotescreditnoteidget"></a>
# **GetCreditNoteApiV1CreditNotesCreditNoteIdGet**
> CreditNoteResponse GetCreditNoteApiV1CreditNotesCreditNoteIdGet (string creditNoteId)

Get Credit Note

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetCreditNoteApiV1CreditNotesCreditNoteIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CreditNotesApi(config);
            var creditNoteId = "creditNoteId_example";  // string | 

            try
            {
                // Get Credit Note
                CreditNoteResponse result = apiInstance.GetCreditNoteApiV1CreditNotesCreditNoteIdGet(creditNoteId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreditNotesApi.GetCreditNoteApiV1CreditNotesCreditNoteIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCreditNoteApiV1CreditNotesCreditNoteIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Credit Note
    ApiResponse<CreditNoteResponse> response = apiInstance.GetCreditNoteApiV1CreditNotesCreditNoteIdGetWithHttpInfo(creditNoteId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreditNotesApi.GetCreditNoteApiV1CreditNotesCreditNoteIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **creditNoteId** | **string** |  |  |

### Return type

[**CreditNoteResponse**](CreditNoteResponse.md)

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

<a id="listcreditnotesapiv1creditnotesget"></a>
# **ListCreditNotesApiV1CreditNotesGet**
> CreditNotesListResponse ListCreditNotesApiV1CreditNotesGet (int? limit = null, string? cursor = null)

List Credit Notes

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListCreditNotesApiV1CreditNotesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CreditNotesApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Credit Notes
                CreditNotesListResponse result = apiInstance.ListCreditNotesApiV1CreditNotesGet(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreditNotesApi.ListCreditNotesApiV1CreditNotesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCreditNotesApiV1CreditNotesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Credit Notes
    ApiResponse<CreditNotesListResponse> response = apiInstance.ListCreditNotesApiV1CreditNotesGetWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreditNotesApi.ListCreditNotesApiV1CreditNotesGetWithHttpInfo: " + e.Message);
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

[**CreditNotesListResponse**](CreditNotesListResponse.md)

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

<a id="rendercreditnoteapiv1creditnotescreditnoteidrenderspost"></a>
# **RenderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost**
> Object RenderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost (string creditNoteId, CreditNoteRenderRequest? creditNoteRenderRequest = null)

Render Credit Note

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RenderCreditNoteApiV1CreditNotesCreditNoteIdRendersPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new CreditNotesApi(config);
            var creditNoteId = "creditNoteId_example";  // string | 
            var creditNoteRenderRequest = new CreditNoteRenderRequest?(); // CreditNoteRenderRequest? |  (optional) 

            try
            {
                // Render Credit Note
                Object result = apiInstance.RenderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost(creditNoteId, creditNoteRenderRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CreditNotesApi.RenderCreditNoteApiV1CreditNotesCreditNoteIdRendersPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RenderCreditNoteApiV1CreditNotesCreditNoteIdRendersPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Render Credit Note
    ApiResponse<Object> response = apiInstance.RenderCreditNoteApiV1CreditNotesCreditNoteIdRendersPostWithHttpInfo(creditNoteId, creditNoteRenderRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CreditNotesApi.RenderCreditNoteApiV1CreditNotesCreditNoteIdRendersPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **creditNoteId** | **string** |  |  |
| **creditNoteRenderRequest** | [**CreditNoteRenderRequest?**](CreditNoteRenderRequest?.md) |  | [optional]  |

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

