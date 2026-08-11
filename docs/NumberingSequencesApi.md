# InvoicePDFs.Api.NumberingSequencesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ConsumeSequenceNumber**](NumberingSequencesApi.md#consumesequencenumber) | **POST** /api/v1/numbering-sequences/{sequence_id}/next | Consume Sequence Number |
| [**CreateSequence**](NumberingSequencesApi.md#createsequence) | **POST** /api/v1/numbering-sequences | Create Sequence |
| [**DeleteSequence**](NumberingSequencesApi.md#deletesequence) | **DELETE** /api/v1/numbering-sequences/{sequence_id} | Delete Sequence |
| [**GetSequence**](NumberingSequencesApi.md#getsequence) | **GET** /api/v1/numbering-sequences/{sequence_id} | Get Sequence |
| [**ListSequences**](NumberingSequencesApi.md#listsequences) | **GET** /api/v1/numbering-sequences | List Sequences |
| [**PreviewSequence**](NumberingSequencesApi.md#previewsequence) | **POST** /api/v1/numbering-sequences/{sequence_id}/preview | Preview Sequence |
| [**UpdateSequence**](NumberingSequencesApi.md#updatesequence) | **PATCH** /api/v1/numbering-sequences/{sequence_id} | Update Sequence |

<a id="consumesequencenumber"></a>
# **ConsumeSequenceNumber**
> NumberingSequenceResponse ConsumeSequenceNumber (string sequenceId)

Consume Sequence Number

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
    public class ConsumeSequenceNumberExample
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
                // Consume Sequence Number
                NumberingSequenceResponse result = apiInstance.ConsumeSequenceNumber(sequenceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.ConsumeSequenceNumber: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ConsumeSequenceNumberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Consume Sequence Number
    ApiResponse<NumberingSequenceResponse> response = apiInstance.ConsumeSequenceNumberWithHttpInfo(sequenceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.ConsumeSequenceNumberWithHttpInfo: " + e.Message);
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

<a id="createsequence"></a>
# **CreateSequence**
> NumberingSequenceResponse CreateSequence (NumberingSequenceCreateRequest numberingSequenceCreateRequest)

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
    public class CreateSequenceExample
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
                NumberingSequenceResponse result = apiInstance.CreateSequence(numberingSequenceCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.CreateSequence: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateSequenceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Sequence
    ApiResponse<NumberingSequenceResponse> response = apiInstance.CreateSequenceWithHttpInfo(numberingSequenceCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.CreateSequenceWithHttpInfo: " + e.Message);
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

<a id="deletesequence"></a>
# **DeleteSequence**
> SimpleBoolResponse DeleteSequence (string sequenceId)

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
    public class DeleteSequenceExample
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
                SimpleBoolResponse result = apiInstance.DeleteSequence(sequenceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.DeleteSequence: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteSequenceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Sequence
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteSequenceWithHttpInfo(sequenceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.DeleteSequenceWithHttpInfo: " + e.Message);
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

<a id="getsequence"></a>
# **GetSequence**
> NumberingSequenceResponse GetSequence (string sequenceId)

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
    public class GetSequenceExample
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
                NumberingSequenceResponse result = apiInstance.GetSequence(sequenceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.GetSequence: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSequenceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Sequence
    ApiResponse<NumberingSequenceResponse> response = apiInstance.GetSequenceWithHttpInfo(sequenceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.GetSequenceWithHttpInfo: " + e.Message);
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

<a id="listsequences"></a>
# **ListSequences**
> NumberingSequencesListResponse ListSequences (int? limit = null, string? cursor = null)

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
    public class ListSequencesExample
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
                NumberingSequencesListResponse result = apiInstance.ListSequences(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.ListSequences: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListSequencesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Sequences
    ApiResponse<NumberingSequencesListResponse> response = apiInstance.ListSequencesWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.ListSequencesWithHttpInfo: " + e.Message);
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

<a id="previewsequence"></a>
# **PreviewSequence**
> NumberingSequencePreviewResponse PreviewSequence (string sequenceId)

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
    public class PreviewSequenceExample
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
                NumberingSequencePreviewResponse result = apiInstance.PreviewSequence(sequenceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.PreviewSequence: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PreviewSequenceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Preview Sequence
    ApiResponse<NumberingSequencePreviewResponse> response = apiInstance.PreviewSequenceWithHttpInfo(sequenceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.PreviewSequenceWithHttpInfo: " + e.Message);
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

<a id="updatesequence"></a>
# **UpdateSequence**
> NumberingSequenceResponse UpdateSequence (string sequenceId, NumberingSequencePatchRequest numberingSequencePatchRequest)

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
    public class UpdateSequenceExample
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
                NumberingSequenceResponse result = apiInstance.UpdateSequence(sequenceId, numberingSequencePatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling NumberingSequencesApi.UpdateSequence: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateSequenceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Sequence
    ApiResponse<NumberingSequenceResponse> response = apiInstance.UpdateSequenceWithHttpInfo(sequenceId, numberingSequencePatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling NumberingSequencesApi.UpdateSequenceWithHttpInfo: " + e.Message);
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

