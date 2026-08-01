# InvoicePDFs.Api.RendersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DownloadRenderApiV1RendersRenderIdDownloadGet**](RendersApi.md#downloadrenderapiv1rendersrenderiddownloadget) | **GET** /api/v1/renders/{render_id}/download | Download Render |
| [**GetRenderApiV1RendersRenderIdGet**](RendersApi.md#getrenderapiv1rendersrenderidget) | **GET** /api/v1/renders/{render_id} | Get Render |

<a id="downloadrenderapiv1rendersrenderiddownloadget"></a>
# **DownloadRenderApiV1RendersRenderIdDownloadGet**
> System.IO.Stream DownloadRenderApiV1RendersRenderIdDownloadGet (string renderId)

Download Render

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DownloadRenderApiV1RendersRenderIdDownloadGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new RendersApi(config);
            var renderId = "renderId_example";  // string | 

            try
            {
                // Download Render
                System.IO.Stream result = apiInstance.DownloadRenderApiV1RendersRenderIdDownloadGet(renderId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RendersApi.DownloadRenderApiV1RendersRenderIdDownloadGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DownloadRenderApiV1RendersRenderIdDownloadGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Download Render
    ApiResponse<System.IO.Stream> response = apiInstance.DownloadRenderApiV1RendersRenderIdDownloadGetWithHttpInfo(renderId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RendersApi.DownloadRenderApiV1RendersRenderIdDownloadGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **renderId** | **string** |  |  |

### Return type

**System.IO.Stream**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | PDF file |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getrenderapiv1rendersrenderidget"></a>
# **GetRenderApiV1RendersRenderIdGet**
> Dictionary&lt;string, Object&gt; GetRenderApiV1RendersRenderIdGet (string renderId)

Get Render

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetRenderApiV1RendersRenderIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new RendersApi(config);
            var renderId = "renderId_example";  // string | 

            try
            {
                // Get Render
                Dictionary<string, Object> result = apiInstance.GetRenderApiV1RendersRenderIdGet(renderId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RendersApi.GetRenderApiV1RendersRenderIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRenderApiV1RendersRenderIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Render
    ApiResponse<Dictionary<string, Object>> response = apiInstance.GetRenderApiV1RendersRenderIdGetWithHttpInfo(renderId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RendersApi.GetRenderApiV1RendersRenderIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **renderId** | **string** |  |  |

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

