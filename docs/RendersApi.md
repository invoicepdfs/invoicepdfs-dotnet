# InvoicePDFs.Api.RendersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DownloadRender**](RendersApi.md#downloadrender) | **GET** /api/v1/renders/{render_id}/download | Download Render |
| [**GetRender**](RendersApi.md#getrender) | **GET** /api/v1/renders/{render_id} | Get Render |

<a id="downloadrender"></a>
# **DownloadRender**
> System.IO.Stream DownloadRender (string renderId)

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
    public class DownloadRenderExample
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
                System.IO.Stream result = apiInstance.DownloadRender(renderId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RendersApi.DownloadRender: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DownloadRenderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Download Render
    ApiResponse<System.IO.Stream> response = apiInstance.DownloadRenderWithHttpInfo(renderId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RendersApi.DownloadRenderWithHttpInfo: " + e.Message);
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

<a id="getrender"></a>
# **GetRender**
> RenderResponse GetRender (string renderId)

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
    public class GetRenderExample
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
                RenderResponse result = apiInstance.GetRender(renderId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RendersApi.GetRender: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRenderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Render
    ApiResponse<RenderResponse> response = apiInstance.GetRenderWithHttpInfo(renderId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RendersApi.GetRenderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **renderId** | **string** |  |  |

### Return type

[**RenderResponse**](RenderResponse.md)

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

