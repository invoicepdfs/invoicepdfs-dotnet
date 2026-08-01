# InvoicePDFs.Api.ImportsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CancelImportApiV1ImportsImportIdCancelPost**](ImportsApi.md#cancelimportapiv1importsimportidcancelpost) | **POST** /api/v1/imports/{import_id}/cancel | Cancel Import |
| [**ConfirmImportApiV1ImportsImportIdConfirmPost**](ImportsApi.md#confirmimportapiv1importsimportidconfirmpost) | **POST** /api/v1/imports/{import_id}/confirm | Confirm Import |
| [**CreateImportApiV1ImportsPost**](ImportsApi.md#createimportapiv1importspost) | **POST** /api/v1/imports | Create Import |
| [**GetImportApiV1ImportsImportIdGet**](ImportsApi.md#getimportapiv1importsimportidget) | **GET** /api/v1/imports/{import_id} | Get Import |

<a id="cancelimportapiv1importsimportidcancelpost"></a>
# **CancelImportApiV1ImportsImportIdCancelPost**
> ImportResponse CancelImportApiV1ImportsImportIdCancelPost (string importId)

Cancel Import

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CancelImportApiV1ImportsImportIdCancelPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ImportsApi(config);
            var importId = "importId_example";  // string | 

            try
            {
                // Cancel Import
                ImportResponse result = apiInstance.CancelImportApiV1ImportsImportIdCancelPost(importId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportsApi.CancelImportApiV1ImportsImportIdCancelPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelImportApiV1ImportsImportIdCancelPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancel Import
    ApiResponse<ImportResponse> response = apiInstance.CancelImportApiV1ImportsImportIdCancelPostWithHttpInfo(importId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportsApi.CancelImportApiV1ImportsImportIdCancelPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **importId** | **string** |  |  |

### Return type

[**ImportResponse**](ImportResponse.md)

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

<a id="confirmimportapiv1importsimportidconfirmpost"></a>
# **ConfirmImportApiV1ImportsImportIdConfirmPost**
> ImportResponse ConfirmImportApiV1ImportsImportIdConfirmPost (string importId)

Confirm Import

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ConfirmImportApiV1ImportsImportIdConfirmPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ImportsApi(config);
            var importId = "importId_example";  // string | 

            try
            {
                // Confirm Import
                ImportResponse result = apiInstance.ConfirmImportApiV1ImportsImportIdConfirmPost(importId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportsApi.ConfirmImportApiV1ImportsImportIdConfirmPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConfirmImportApiV1ImportsImportIdConfirmPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Confirm Import
    ApiResponse<ImportResponse> response = apiInstance.ConfirmImportApiV1ImportsImportIdConfirmPostWithHttpInfo(importId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportsApi.ConfirmImportApiV1ImportsImportIdConfirmPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **importId** | **string** |  |  |

### Return type

[**ImportResponse**](ImportResponse.md)

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

<a id="createimportapiv1importspost"></a>
# **CreateImportApiV1ImportsPost**
> ImportResponse CreateImportApiV1ImportsPost (ImportCreateRequest importCreateRequest)

Create Import

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateImportApiV1ImportsPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ImportsApi(config);
            var importCreateRequest = new ImportCreateRequest(); // ImportCreateRequest | 

            try
            {
                // Create Import
                ImportResponse result = apiInstance.CreateImportApiV1ImportsPost(importCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportsApi.CreateImportApiV1ImportsPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateImportApiV1ImportsPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Import
    ApiResponse<ImportResponse> response = apiInstance.CreateImportApiV1ImportsPostWithHttpInfo(importCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportsApi.CreateImportApiV1ImportsPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **importCreateRequest** | [**ImportCreateRequest**](ImportCreateRequest.md) |  |  |

### Return type

[**ImportResponse**](ImportResponse.md)

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

<a id="getimportapiv1importsimportidget"></a>
# **GetImportApiV1ImportsImportIdGet**
> ImportResponse GetImportApiV1ImportsImportIdGet (string importId)

Get Import

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetImportApiV1ImportsImportIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ImportsApi(config);
            var importId = "importId_example";  // string | 

            try
            {
                // Get Import
                ImportResponse result = apiInstance.GetImportApiV1ImportsImportIdGet(importId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImportsApi.GetImportApiV1ImportsImportIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetImportApiV1ImportsImportIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Import
    ApiResponse<ImportResponse> response = apiInstance.GetImportApiV1ImportsImportIdGetWithHttpInfo(importId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImportsApi.GetImportApiV1ImportsImportIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **importId** | **string** |  |  |

### Return type

[**ImportResponse**](ImportResponse.md)

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

