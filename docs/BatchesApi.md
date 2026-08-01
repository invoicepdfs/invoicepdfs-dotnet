# InvoicePDFs.Api.BatchesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CancelBatchApiV1BatchesBatchIdCancelPost**](BatchesApi.md#cancelbatchapiv1batchesbatchidcancelpost) | **POST** /api/v1/batches/{batch_id}/cancel | Cancel Batch |
| [**CreateBatchApiV1BatchesPost**](BatchesApi.md#createbatchapiv1batchespost) | **POST** /api/v1/batches | Create Batch |
| [**DownloadBatchApiV1BatchesBatchIdDownloadGet**](BatchesApi.md#downloadbatchapiv1batchesbatchiddownloadget) | **GET** /api/v1/batches/{batch_id}/download | Download Batch |
| [**GetBatchApiV1BatchesBatchIdGet**](BatchesApi.md#getbatchapiv1batchesbatchidget) | **GET** /api/v1/batches/{batch_id} | Get Batch |
| [**ListBatchItemsApiV1BatchesBatchIdItemsGet**](BatchesApi.md#listbatchitemsapiv1batchesbatchiditemsget) | **GET** /api/v1/batches/{batch_id}/items | List Batch Items |
| [**ListBatchesApiV1BatchesGet**](BatchesApi.md#listbatchesapiv1batchesget) | **GET** /api/v1/batches | List Batches |

<a id="cancelbatchapiv1batchesbatchidcancelpost"></a>
# **CancelBatchApiV1BatchesBatchIdCancelPost**
> BatchResponse CancelBatchApiV1BatchesBatchIdCancelPost (string batchId)

Cancel Batch

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CancelBatchApiV1BatchesBatchIdCancelPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BatchesApi(config);
            var batchId = "batchId_example";  // string | 

            try
            {
                // Cancel Batch
                BatchResponse result = apiInstance.CancelBatchApiV1BatchesBatchIdCancelPost(batchId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BatchesApi.CancelBatchApiV1BatchesBatchIdCancelPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelBatchApiV1BatchesBatchIdCancelPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancel Batch
    ApiResponse<BatchResponse> response = apiInstance.CancelBatchApiV1BatchesBatchIdCancelPostWithHttpInfo(batchId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BatchesApi.CancelBatchApiV1BatchesBatchIdCancelPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **batchId** | **string** |  |  |

### Return type

[**BatchResponse**](BatchResponse.md)

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

<a id="createbatchapiv1batchespost"></a>
# **CreateBatchApiV1BatchesPost**
> BatchResponse CreateBatchApiV1BatchesPost (BatchCreateRequest batchCreateRequest)

Create Batch

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateBatchApiV1BatchesPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BatchesApi(config);
            var batchCreateRequest = new BatchCreateRequest(); // BatchCreateRequest | 

            try
            {
                // Create Batch
                BatchResponse result = apiInstance.CreateBatchApiV1BatchesPost(batchCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BatchesApi.CreateBatchApiV1BatchesPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateBatchApiV1BatchesPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Batch
    ApiResponse<BatchResponse> response = apiInstance.CreateBatchApiV1BatchesPostWithHttpInfo(batchCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BatchesApi.CreateBatchApiV1BatchesPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **batchCreateRequest** | [**BatchCreateRequest**](BatchCreateRequest.md) |  |  |

### Return type

[**BatchResponse**](BatchResponse.md)

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

<a id="downloadbatchapiv1batchesbatchiddownloadget"></a>
# **DownloadBatchApiV1BatchesBatchIdDownloadGet**
> Object DownloadBatchApiV1BatchesBatchIdDownloadGet (string batchId)

Download Batch

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DownloadBatchApiV1BatchesBatchIdDownloadGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BatchesApi(config);
            var batchId = "batchId_example";  // string | 

            try
            {
                // Download Batch
                Object result = apiInstance.DownloadBatchApiV1BatchesBatchIdDownloadGet(batchId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BatchesApi.DownloadBatchApiV1BatchesBatchIdDownloadGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DownloadBatchApiV1BatchesBatchIdDownloadGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Download Batch
    ApiResponse<Object> response = apiInstance.DownloadBatchApiV1BatchesBatchIdDownloadGetWithHttpInfo(batchId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BatchesApi.DownloadBatchApiV1BatchesBatchIdDownloadGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **batchId** | **string** |  |  |

### Return type

**Object**

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

<a id="getbatchapiv1batchesbatchidget"></a>
# **GetBatchApiV1BatchesBatchIdGet**
> BatchResponse GetBatchApiV1BatchesBatchIdGet (string batchId)

Get Batch

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetBatchApiV1BatchesBatchIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BatchesApi(config);
            var batchId = "batchId_example";  // string | 

            try
            {
                // Get Batch
                BatchResponse result = apiInstance.GetBatchApiV1BatchesBatchIdGet(batchId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BatchesApi.GetBatchApiV1BatchesBatchIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetBatchApiV1BatchesBatchIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Batch
    ApiResponse<BatchResponse> response = apiInstance.GetBatchApiV1BatchesBatchIdGetWithHttpInfo(batchId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BatchesApi.GetBatchApiV1BatchesBatchIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **batchId** | **string** |  |  |

### Return type

[**BatchResponse**](BatchResponse.md)

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

<a id="listbatchitemsapiv1batchesbatchiditemsget"></a>
# **ListBatchItemsApiV1BatchesBatchIdItemsGet**
> BatchItemsListResponse ListBatchItemsApiV1BatchesBatchIdItemsGet (string batchId, int? limit = null, string? cursor = null)

List Batch Items

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListBatchItemsApiV1BatchesBatchIdItemsGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BatchesApi(config);
            var batchId = "batchId_example";  // string | 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Batch Items
                BatchItemsListResponse result = apiInstance.ListBatchItemsApiV1BatchesBatchIdItemsGet(batchId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BatchesApi.ListBatchItemsApiV1BatchesBatchIdItemsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBatchItemsApiV1BatchesBatchIdItemsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Batch Items
    ApiResponse<BatchItemsListResponse> response = apiInstance.ListBatchItemsApiV1BatchesBatchIdItemsGetWithHttpInfo(batchId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BatchesApi.ListBatchItemsApiV1BatchesBatchIdItemsGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **batchId** | **string** |  |  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** |  | [optional]  |

### Return type

[**BatchItemsListResponse**](BatchItemsListResponse.md)

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

<a id="listbatchesapiv1batchesget"></a>
# **ListBatchesApiV1BatchesGet**
> BatchesListResponse ListBatchesApiV1BatchesGet (int? limit = null, string? cursor = null)

List Batches

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListBatchesApiV1BatchesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BatchesApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Batches
                BatchesListResponse result = apiInstance.ListBatchesApiV1BatchesGet(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BatchesApi.ListBatchesApiV1BatchesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListBatchesApiV1BatchesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Batches
    ApiResponse<BatchesListResponse> response = apiInstance.ListBatchesApiV1BatchesGetWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BatchesApi.ListBatchesApiV1BatchesGetWithHttpInfo: " + e.Message);
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

[**BatchesListResponse**](BatchesListResponse.md)

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

