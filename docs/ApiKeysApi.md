# InvoicePDFs.Api.ApiKeysApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateApiKeyApiV1ApiKeysPost**](ApiKeysApi.md#createapikeyapiv1apikeyspost) | **POST** /api/v1/api-keys | Create Api Key |
| [**GetApiKeyApiV1ApiKeysApiKeyIdGet**](ApiKeysApi.md#getapikeyapiv1apikeysapikeyidget) | **GET** /api/v1/api-keys/{api_key_id} | Get Api Key |
| [**ListApiKeysApiV1ApiKeysGet**](ApiKeysApi.md#listapikeysapiv1apikeysget) | **GET** /api/v1/api-keys | List Api Keys |
| [**PatchApiKeyApiV1ApiKeysApiKeyIdPatch**](ApiKeysApi.md#patchapikeyapiv1apikeysapikeyidpatch) | **PATCH** /api/v1/api-keys/{api_key_id} | Patch Api Key |
| [**RevokeApiKeyApiV1ApiKeysApiKeyIdDelete**](ApiKeysApi.md#revokeapikeyapiv1apikeysapikeyiddelete) | **DELETE** /api/v1/api-keys/{api_key_id} | Revoke Api Key |
| [**RotateApiKeyApiV1ApiKeysApiKeyIdRotatePost**](ApiKeysApi.md#rotateapikeyapiv1apikeysapikeyidrotatepost) | **POST** /api/v1/api-keys/{api_key_id}/rotate | Rotate Api Key |

<a id="createapikeyapiv1apikeyspost"></a>
# **CreateApiKeyApiV1ApiKeysPost**
> ApiKeyCreateResponse CreateApiKeyApiV1ApiKeysPost (ApiKeyCreateRequest apiKeyCreateRequest)

Create Api Key

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateApiKeyApiV1ApiKeysPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ApiKeysApi(config);
            var apiKeyCreateRequest = new ApiKeyCreateRequest(); // ApiKeyCreateRequest | 

            try
            {
                // Create Api Key
                ApiKeyCreateResponse result = apiInstance.CreateApiKeyApiV1ApiKeysPost(apiKeyCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApiKeysApi.CreateApiKeyApiV1ApiKeysPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateApiKeyApiV1ApiKeysPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Api Key
    ApiResponse<ApiKeyCreateResponse> response = apiInstance.CreateApiKeyApiV1ApiKeysPostWithHttpInfo(apiKeyCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApiKeysApi.CreateApiKeyApiV1ApiKeysPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **apiKeyCreateRequest** | [**ApiKeyCreateRequest**](ApiKeyCreateRequest.md) |  |  |

### Return type

[**ApiKeyCreateResponse**](ApiKeyCreateResponse.md)

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

<a id="getapikeyapiv1apikeysapikeyidget"></a>
# **GetApiKeyApiV1ApiKeysApiKeyIdGet**
> ApiKeyDetailResponse GetApiKeyApiV1ApiKeysApiKeyIdGet (string apiKeyId)

Get Api Key

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetApiKeyApiV1ApiKeysApiKeyIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ApiKeysApi(config);
            var apiKeyId = "apiKeyId_example";  // string | 

            try
            {
                // Get Api Key
                ApiKeyDetailResponse result = apiInstance.GetApiKeyApiV1ApiKeysApiKeyIdGet(apiKeyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApiKeysApi.GetApiKeyApiV1ApiKeysApiKeyIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetApiKeyApiV1ApiKeysApiKeyIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Api Key
    ApiResponse<ApiKeyDetailResponse> response = apiInstance.GetApiKeyApiV1ApiKeysApiKeyIdGetWithHttpInfo(apiKeyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApiKeysApi.GetApiKeyApiV1ApiKeysApiKeyIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **apiKeyId** | **string** |  |  |

### Return type

[**ApiKeyDetailResponse**](ApiKeyDetailResponse.md)

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

<a id="listapikeysapiv1apikeysget"></a>
# **ListApiKeysApiV1ApiKeysGet**
> ApiKeyListResponse ListApiKeysApiV1ApiKeysGet ()

List Api Keys

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListApiKeysApiV1ApiKeysGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ApiKeysApi(config);

            try
            {
                // List Api Keys
                ApiKeyListResponse result = apiInstance.ListApiKeysApiV1ApiKeysGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApiKeysApi.ListApiKeysApiV1ApiKeysGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListApiKeysApiV1ApiKeysGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Api Keys
    ApiResponse<ApiKeyListResponse> response = apiInstance.ListApiKeysApiV1ApiKeysGetWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApiKeysApi.ListApiKeysApiV1ApiKeysGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**ApiKeyListResponse**](ApiKeyListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="patchapikeyapiv1apikeysapikeyidpatch"></a>
# **PatchApiKeyApiV1ApiKeysApiKeyIdPatch**
> ApiKeyDetailResponse PatchApiKeyApiV1ApiKeysApiKeyIdPatch (string apiKeyId, ApiKeyPatchRequest apiKeyPatchRequest)

Patch Api Key

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PatchApiKeyApiV1ApiKeysApiKeyIdPatchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ApiKeysApi(config);
            var apiKeyId = "apiKeyId_example";  // string | 
            var apiKeyPatchRequest = new ApiKeyPatchRequest(); // ApiKeyPatchRequest | 

            try
            {
                // Patch Api Key
                ApiKeyDetailResponse result = apiInstance.PatchApiKeyApiV1ApiKeysApiKeyIdPatch(apiKeyId, apiKeyPatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApiKeysApi.PatchApiKeyApiV1ApiKeysApiKeyIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PatchApiKeyApiV1ApiKeysApiKeyIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Patch Api Key
    ApiResponse<ApiKeyDetailResponse> response = apiInstance.PatchApiKeyApiV1ApiKeysApiKeyIdPatchWithHttpInfo(apiKeyId, apiKeyPatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApiKeysApi.PatchApiKeyApiV1ApiKeysApiKeyIdPatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **apiKeyId** | **string** |  |  |
| **apiKeyPatchRequest** | [**ApiKeyPatchRequest**](ApiKeyPatchRequest.md) |  |  |

### Return type

[**ApiKeyDetailResponse**](ApiKeyDetailResponse.md)

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

<a id="revokeapikeyapiv1apikeysapikeyiddelete"></a>
# **RevokeApiKeyApiV1ApiKeysApiKeyIdDelete**
> ApiKeyRevokeResponse RevokeApiKeyApiV1ApiKeysApiKeyIdDelete (string apiKeyId)

Revoke Api Key

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RevokeApiKeyApiV1ApiKeysApiKeyIdDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ApiKeysApi(config);
            var apiKeyId = "apiKeyId_example";  // string | 

            try
            {
                // Revoke Api Key
                ApiKeyRevokeResponse result = apiInstance.RevokeApiKeyApiV1ApiKeysApiKeyIdDelete(apiKeyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApiKeysApi.RevokeApiKeyApiV1ApiKeysApiKeyIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RevokeApiKeyApiV1ApiKeysApiKeyIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Revoke Api Key
    ApiResponse<ApiKeyRevokeResponse> response = apiInstance.RevokeApiKeyApiV1ApiKeysApiKeyIdDeleteWithHttpInfo(apiKeyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApiKeysApi.RevokeApiKeyApiV1ApiKeysApiKeyIdDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **apiKeyId** | **string** |  |  |

### Return type

[**ApiKeyRevokeResponse**](ApiKeyRevokeResponse.md)

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

<a id="rotateapikeyapiv1apikeysapikeyidrotatepost"></a>
# **RotateApiKeyApiV1ApiKeysApiKeyIdRotatePost**
> ApiKeyRotateResponse RotateApiKeyApiV1ApiKeysApiKeyIdRotatePost (string apiKeyId)

Rotate Api Key

Revoke the existing key and create a new one with the same name.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RotateApiKeyApiV1ApiKeysApiKeyIdRotatePostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ApiKeysApi(config);
            var apiKeyId = "apiKeyId_example";  // string | 

            try
            {
                // Rotate Api Key
                ApiKeyRotateResponse result = apiInstance.RotateApiKeyApiV1ApiKeysApiKeyIdRotatePost(apiKeyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApiKeysApi.RotateApiKeyApiV1ApiKeysApiKeyIdRotatePost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RotateApiKeyApiV1ApiKeysApiKeyIdRotatePostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rotate Api Key
    ApiResponse<ApiKeyRotateResponse> response = apiInstance.RotateApiKeyApiV1ApiKeysApiKeyIdRotatePostWithHttpInfo(apiKeyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApiKeysApi.RotateApiKeyApiV1ApiKeysApiKeyIdRotatePostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **apiKeyId** | **string** |  |  |

### Return type

[**ApiKeyRotateResponse**](ApiKeyRotateResponse.md)

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

