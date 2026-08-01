# InvoicePDFs.Api.NumberingSequencesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ConsumeNextApiV1NumberingSequencesSequenceIdNextPost**](NumberingSequencesApi.md#consumenextapiv1numberingsequencessequenceidnextpost) | **POST** /api/v1/numbering-sequences/{sequence_id}/next | Consume Next |
| [**CreateSequenceApiV1NumberingSequencesPost**](NumberingSequencesApi.md#createsequenceapiv1numberingsequencespost) | **POST** /api/v1/numbering-sequences | Create Sequence |
| [**DeleteSequenceApiV1NumberingSequencesSequenceIdDelete**](NumberingSequencesApi.md#deletesequenceapiv1numberingsequencessequenceiddelete) | **DELETE** /api/v1/numbering-sequences/{sequence_id} | Delete Sequence |
| [**GetSequenceApiV1NumberingSequencesSequenceIdGet**](NumberingSequencesApi.md#getsequenceapiv1numberingsequencessequenceidget) | **GET** /api/v1/numbering-sequences/{sequence_id} | Get Sequence |
| [**ListSequencesApiV1NumberingSequencesGet**](NumberingSequencesApi.md#listsequencesapiv1numberingsequencesget) | **GET** /api/v1/numbering-sequences | List Sequences |
| [**PreviewSequenceApiV1NumberingSequencesSequenceIdPreviewPost**](NumberingSequencesApi.md#previewsequenceapiv1numberingsequencessequenceidpreviewpost) | **POST** /api/v1/numbering-sequences/{sequence_id}/preview | Preview Sequence |
| [**UpdateSequenceApiV1NumberingSequencesSequenceIdPatch**](NumberingSequencesApi.md#updatesequenceapiv1numberingsequencessequenceidpatch) | **PATCH** /api/v1/numbering-sequences/{sequence_id} | Update Sequence |

<a id="consumenextapiv1numberingsequencessequenceidnextpost"></a>
# **ConsumeNextApiV1NumberingSequencesSequenceIdNextPost**
> NumberingSequenceResponse ConsumeNextApiV1NumberingSequencesSequenceIdNextPost (string sequenceId)

Consume Next

Consume and return the next number, incrementing the counter.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ConsumeNextApiV1NumberingSequencesSequenceIdNextPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new NumberingSequencesApi(config);
            var sequenceId = "sequenceId_example";  // string | 

            try
            {
                // Consume Next
                NumberingSequenceResponse result = apiInstance.ConsumeNextApiV1NumberingSequencesSequenceIdNextPost(sequenceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.ConsumeNextApiV1NumberingSequencesSequenceIdNextPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConsumeNextApiV1NumberingSequencesSequenceIdNextPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Consume Next
    ApiResponse<NumberingSequenceResponse> response = apiInstance.ConsumeNextApiV1NumberingSequencesSequenceIdNextPostWithHttpInfo(sequenceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.ConsumeNextApiV1NumberingSequencesSequenceIdNextPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sequenceId** | **string** |  |  |

### Return type

[**NumberingSequenceResponse**](NumberingSequenceResponse.md)

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

<a id="createsequenceapiv1numberingsequencespost"></a>
# **CreateSequenceApiV1NumberingSequencesPost**
> NumberingSequenceResponse CreateSequenceApiV1NumberingSequencesPost (NumberingSequenceCreateRequest numberingSequenceCreateRequest)

Create Sequence

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateSequenceApiV1NumberingSequencesPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new NumberingSequencesApi(config);
            var numberingSequenceCreateRequest = new NumberingSequenceCreateRequest(); // NumberingSequenceCreateRequest | 

            try
            {
                // Create Sequence
                NumberingSequenceResponse result = apiInstance.CreateSequenceApiV1NumberingSequencesPost(numberingSequenceCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.CreateSequenceApiV1NumberingSequencesPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateSequenceApiV1NumberingSequencesPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Sequence
    ApiResponse<NumberingSequenceResponse> response = apiInstance.CreateSequenceApiV1NumberingSequencesPostWithHttpInfo(numberingSequenceCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.CreateSequenceApiV1NumberingSequencesPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **numberingSequenceCreateRequest** | [**NumberingSequenceCreateRequest**](NumberingSequenceCreateRequest.md) |  |  |

### Return type

[**NumberingSequenceResponse**](NumberingSequenceResponse.md)

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

<a id="deletesequenceapiv1numberingsequencessequenceiddelete"></a>
# **DeleteSequenceApiV1NumberingSequencesSequenceIdDelete**
> SimpleBoolResponse DeleteSequenceApiV1NumberingSequencesSequenceIdDelete (string sequenceId)

Delete Sequence

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteSequenceApiV1NumberingSequencesSequenceIdDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new NumberingSequencesApi(config);
            var sequenceId = "sequenceId_example";  // string | 

            try
            {
                // Delete Sequence
                SimpleBoolResponse result = apiInstance.DeleteSequenceApiV1NumberingSequencesSequenceIdDelete(sequenceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.DeleteSequenceApiV1NumberingSequencesSequenceIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteSequenceApiV1NumberingSequencesSequenceIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Sequence
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteSequenceApiV1NumberingSequencesSequenceIdDeleteWithHttpInfo(sequenceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.DeleteSequenceApiV1NumberingSequencesSequenceIdDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sequenceId** | **string** |  |  |

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

<a id="getsequenceapiv1numberingsequencessequenceidget"></a>
# **GetSequenceApiV1NumberingSequencesSequenceIdGet**
> NumberingSequenceResponse GetSequenceApiV1NumberingSequencesSequenceIdGet (string sequenceId)

Get Sequence

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetSequenceApiV1NumberingSequencesSequenceIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new NumberingSequencesApi(config);
            var sequenceId = "sequenceId_example";  // string | 

            try
            {
                // Get Sequence
                NumberingSequenceResponse result = apiInstance.GetSequenceApiV1NumberingSequencesSequenceIdGet(sequenceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.GetSequenceApiV1NumberingSequencesSequenceIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSequenceApiV1NumberingSequencesSequenceIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Sequence
    ApiResponse<NumberingSequenceResponse> response = apiInstance.GetSequenceApiV1NumberingSequencesSequenceIdGetWithHttpInfo(sequenceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.GetSequenceApiV1NumberingSequencesSequenceIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sequenceId** | **string** |  |  |

### Return type

[**NumberingSequenceResponse**](NumberingSequenceResponse.md)

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

<a id="listsequencesapiv1numberingsequencesget"></a>
# **ListSequencesApiV1NumberingSequencesGet**
> NumberingSequencesListResponse ListSequencesApiV1NumberingSequencesGet (int? limit = null, string? cursor = null)

List Sequences

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListSequencesApiV1NumberingSequencesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new NumberingSequencesApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Sequences
                NumberingSequencesListResponse result = apiInstance.ListSequencesApiV1NumberingSequencesGet(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.ListSequencesApiV1NumberingSequencesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListSequencesApiV1NumberingSequencesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Sequences
    ApiResponse<NumberingSequencesListResponse> response = apiInstance.ListSequencesApiV1NumberingSequencesGetWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.ListSequencesApiV1NumberingSequencesGetWithHttpInfo: " + e.Message);
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

[**NumberingSequencesListResponse**](NumberingSequencesListResponse.md)

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

<a id="previewsequenceapiv1numberingsequencessequenceidpreviewpost"></a>
# **PreviewSequenceApiV1NumberingSequencesSequenceIdPreviewPost**
> NumberingSequencePreviewResponse PreviewSequenceApiV1NumberingSequencesSequenceIdPreviewPost (string sequenceId)

Preview Sequence

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PreviewSequenceApiV1NumberingSequencesSequenceIdPreviewPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new NumberingSequencesApi(config);
            var sequenceId = "sequenceId_example";  // string | 

            try
            {
                // Preview Sequence
                NumberingSequencePreviewResponse result = apiInstance.PreviewSequenceApiV1NumberingSequencesSequenceIdPreviewPost(sequenceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.PreviewSequenceApiV1NumberingSequencesSequenceIdPreviewPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PreviewSequenceApiV1NumberingSequencesSequenceIdPreviewPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Preview Sequence
    ApiResponse<NumberingSequencePreviewResponse> response = apiInstance.PreviewSequenceApiV1NumberingSequencesSequenceIdPreviewPostWithHttpInfo(sequenceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.PreviewSequenceApiV1NumberingSequencesSequenceIdPreviewPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sequenceId** | **string** |  |  |

### Return type

[**NumberingSequencePreviewResponse**](NumberingSequencePreviewResponse.md)

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

<a id="updatesequenceapiv1numberingsequencessequenceidpatch"></a>
# **UpdateSequenceApiV1NumberingSequencesSequenceIdPatch**
> NumberingSequenceResponse UpdateSequenceApiV1NumberingSequencesSequenceIdPatch (string sequenceId, NumberingSequencePatchRequest numberingSequencePatchRequest)

Update Sequence

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UpdateSequenceApiV1NumberingSequencesSequenceIdPatchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new NumberingSequencesApi(config);
            var sequenceId = "sequenceId_example";  // string | 
            var numberingSequencePatchRequest = new NumberingSequencePatchRequest(); // NumberingSequencePatchRequest | 

            try
            {
                // Update Sequence
                NumberingSequenceResponse result = apiInstance.UpdateSequenceApiV1NumberingSequencesSequenceIdPatch(sequenceId, numberingSequencePatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.UpdateSequenceApiV1NumberingSequencesSequenceIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateSequenceApiV1NumberingSequencesSequenceIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Sequence
    ApiResponse<NumberingSequenceResponse> response = apiInstance.UpdateSequenceApiV1NumberingSequencesSequenceIdPatchWithHttpInfo(sequenceId, numberingSequencePatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.UpdateSequenceApiV1NumberingSequencesSequenceIdPatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sequenceId** | **string** |  |  |
| **numberingSequencePatchRequest** | [**NumberingSequencePatchRequest**](NumberingSequencePatchRequest.md) |  |  |

### Return type

[**NumberingSequenceResponse**](NumberingSequenceResponse.md)

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

