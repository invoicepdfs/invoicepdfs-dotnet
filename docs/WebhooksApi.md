# InvoicePDFs.Api.WebhooksApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateWebhookEndpoint**](WebhooksApi.md#createwebhookendpoint) | **POST** /api/v1/webhook-endpoints | Create Webhook Endpoint |
| [**DeleteWebhookEndpoint**](WebhooksApi.md#deletewebhookendpoint) | **DELETE** /api/v1/webhook-endpoints/{endpoint_id} | Delete Webhook Endpoint |
| [**GetWebhookDelivery**](WebhooksApi.md#getwebhookdelivery) | **GET** /api/v1/webhook-deliveries/{delivery_id} | Get Webhook Delivery |
| [**GetWebhookEndpoint**](WebhooksApi.md#getwebhookendpoint) | **GET** /api/v1/webhook-endpoints/{endpoint_id} | Get Webhook Endpoint |
| [**ListWebhookDeliveries**](WebhooksApi.md#listwebhookdeliveries) | **GET** /api/v1/webhook-deliveries | List Webhook Deliveries |
| [**ListWebhookEndpoints**](WebhooksApi.md#listwebhookendpoints) | **GET** /api/v1/webhook-endpoints | List Webhook Endpoints |
| [**RetryWebhookDelivery**](WebhooksApi.md#retrywebhookdelivery) | **POST** /api/v1/webhook-deliveries/{delivery_id}/retry | Retry Webhook Delivery |
| [**RotateWebhookSecret**](WebhooksApi.md#rotatewebhooksecret) | **POST** /api/v1/webhook-endpoints/{endpoint_id}/rotate-secret | Rotate Webhook Secret |
| [**TestWebhookEndpoint**](WebhooksApi.md#testwebhookendpoint) | **POST** /api/v1/webhook-endpoints/{endpoint_id}/test | Test Webhook Endpoint |
| [**UpdateWebhookEndpoint**](WebhooksApi.md#updatewebhookendpoint) | **PATCH** /api/v1/webhook-endpoints/{endpoint_id} | Update Webhook Endpoint |

<a id="createwebhookendpoint"></a>
# **CreateWebhookEndpoint**
> WebhookEndpointResponse CreateWebhookEndpoint (WebhookEndpointCreateRequest webhookEndpointCreateRequest)

Create Webhook Endpoint

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateWebhookEndpointExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var webhookEndpointCreateRequest = new WebhookEndpointCreateRequest(); // WebhookEndpointCreateRequest | 

            try
            {
                // Create Webhook Endpoint
                WebhookEndpointResponse result = apiInstance.CreateWebhookEndpoint(webhookEndpointCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.CreateWebhookEndpoint: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateWebhookEndpointWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Webhook Endpoint
    ApiResponse<WebhookEndpointResponse> response = apiInstance.CreateWebhookEndpointWithHttpInfo(webhookEndpointCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.CreateWebhookEndpointWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **webhookEndpointCreateRequest** | [**WebhookEndpointCreateRequest**](WebhookEndpointCreateRequest.md) |  |  |

### Return type

[**WebhookEndpointResponse**](WebhookEndpointResponse.md)

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

<a id="deletewebhookendpoint"></a>
# **DeleteWebhookEndpoint**
> SimpleBoolResponse DeleteWebhookEndpoint (string endpointId)

Delete Webhook Endpoint

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteWebhookEndpointExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var endpointId = "endpointId_example";  // string | 

            try
            {
                // Delete Webhook Endpoint
                SimpleBoolResponse result = apiInstance.DeleteWebhookEndpoint(endpointId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.DeleteWebhookEndpoint: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteWebhookEndpointWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Webhook Endpoint
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteWebhookEndpointWithHttpInfo(endpointId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.DeleteWebhookEndpointWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **endpointId** | **string** |  |  |

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

<a id="getwebhookdelivery"></a>
# **GetWebhookDelivery**
> WebhookDeliveryResponse GetWebhookDelivery (string deliveryId)

Get Webhook Delivery

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetWebhookDeliveryExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var deliveryId = "deliveryId_example";  // string | 

            try
            {
                // Get Webhook Delivery
                WebhookDeliveryResponse result = apiInstance.GetWebhookDelivery(deliveryId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.GetWebhookDelivery: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWebhookDeliveryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Webhook Delivery
    ApiResponse<WebhookDeliveryResponse> response = apiInstance.GetWebhookDeliveryWithHttpInfo(deliveryId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.GetWebhookDeliveryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryId** | **string** |  |  |

### Return type

[**WebhookDeliveryResponse**](WebhookDeliveryResponse.md)

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

<a id="getwebhookendpoint"></a>
# **GetWebhookEndpoint**
> WebhookEndpointResponse GetWebhookEndpoint (string endpointId)

Get Webhook Endpoint

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetWebhookEndpointExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var endpointId = "endpointId_example";  // string | 

            try
            {
                // Get Webhook Endpoint
                WebhookEndpointResponse result = apiInstance.GetWebhookEndpoint(endpointId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.GetWebhookEndpoint: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWebhookEndpointWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Webhook Endpoint
    ApiResponse<WebhookEndpointResponse> response = apiInstance.GetWebhookEndpointWithHttpInfo(endpointId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.GetWebhookEndpointWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **endpointId** | **string** |  |  |

### Return type

[**WebhookEndpointResponse**](WebhookEndpointResponse.md)

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

<a id="listwebhookdeliveries"></a>
# **ListWebhookDeliveries**
> WebhookDeliveriesListResponse ListWebhookDeliveries (int? limit = null, string? cursor = null)

List Webhook Deliveries

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListWebhookDeliveriesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Webhook Deliveries
                WebhookDeliveriesListResponse result = apiInstance.ListWebhookDeliveries(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.ListWebhookDeliveries: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWebhookDeliveriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Webhook Deliveries
    ApiResponse<WebhookDeliveriesListResponse> response = apiInstance.ListWebhookDeliveriesWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.ListWebhookDeliveriesWithHttpInfo: " + e.Message);
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

[**WebhookDeliveriesListResponse**](WebhookDeliveriesListResponse.md)

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

<a id="listwebhookendpoints"></a>
# **ListWebhookEndpoints**
> WebhookEndpointsListResponse ListWebhookEndpoints (int? limit = null, string? cursor = null)

List Webhook Endpoints

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListWebhookEndpointsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Webhook Endpoints
                WebhookEndpointsListResponse result = apiInstance.ListWebhookEndpoints(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.ListWebhookEndpoints: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWebhookEndpointsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Webhook Endpoints
    ApiResponse<WebhookEndpointsListResponse> response = apiInstance.ListWebhookEndpointsWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.ListWebhookEndpointsWithHttpInfo: " + e.Message);
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

[**WebhookEndpointsListResponse**](WebhookEndpointsListResponse.md)

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

<a id="retrywebhookdelivery"></a>
# **RetryWebhookDelivery**
> WebhookDeliveryResponse RetryWebhookDelivery (string deliveryId)

Retry Webhook Delivery

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RetryWebhookDeliveryExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var deliveryId = "deliveryId_example";  // string | 

            try
            {
                // Retry Webhook Delivery
                WebhookDeliveryResponse result = apiInstance.RetryWebhookDelivery(deliveryId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.RetryWebhookDelivery: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RetryWebhookDeliveryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retry Webhook Delivery
    ApiResponse<WebhookDeliveryResponse> response = apiInstance.RetryWebhookDeliveryWithHttpInfo(deliveryId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.RetryWebhookDeliveryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryId** | **string** |  |  |

### Return type

[**WebhookDeliveryResponse**](WebhookDeliveryResponse.md)

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

<a id="rotatewebhooksecret"></a>
# **RotateWebhookSecret**
> WebhookSecretResponse RotateWebhookSecret (string endpointId)

Rotate Webhook Secret

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RotateWebhookSecretExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var endpointId = "endpointId_example";  // string | 

            try
            {
                // Rotate Webhook Secret
                WebhookSecretResponse result = apiInstance.RotateWebhookSecret(endpointId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.RotateWebhookSecret: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RotateWebhookSecretWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rotate Webhook Secret
    ApiResponse<WebhookSecretResponse> response = apiInstance.RotateWebhookSecretWithHttpInfo(endpointId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.RotateWebhookSecretWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **endpointId** | **string** |  |  |

### Return type

[**WebhookSecretResponse**](WebhookSecretResponse.md)

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

<a id="testwebhookendpoint"></a>
# **TestWebhookEndpoint**
> WebhookDeliveryResponse TestWebhookEndpoint (string endpointId)

Test Webhook Endpoint

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class TestWebhookEndpointExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var endpointId = "endpointId_example";  // string | 

            try
            {
                // Test Webhook Endpoint
                WebhookDeliveryResponse result = apiInstance.TestWebhookEndpoint(endpointId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.TestWebhookEndpoint: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TestWebhookEndpointWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Test Webhook Endpoint
    ApiResponse<WebhookDeliveryResponse> response = apiInstance.TestWebhookEndpointWithHttpInfo(endpointId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.TestWebhookEndpointWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **endpointId** | **string** |  |  |

### Return type

[**WebhookDeliveryResponse**](WebhookDeliveryResponse.md)

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

<a id="updatewebhookendpoint"></a>
# **UpdateWebhookEndpoint**
> WebhookEndpointResponse UpdateWebhookEndpoint (string endpointId, WebhookEndpointPatchRequest webhookEndpointPatchRequest)

Update Webhook Endpoint

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UpdateWebhookEndpointExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var endpointId = "endpointId_example";  // string | 
            var webhookEndpointPatchRequest = new WebhookEndpointPatchRequest(); // WebhookEndpointPatchRequest | 

            try
            {
                // Update Webhook Endpoint
                WebhookEndpointResponse result = apiInstance.UpdateWebhookEndpoint(endpointId, webhookEndpointPatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.UpdateWebhookEndpoint: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateWebhookEndpointWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Webhook Endpoint
    ApiResponse<WebhookEndpointResponse> response = apiInstance.UpdateWebhookEndpointWithHttpInfo(endpointId, webhookEndpointPatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.UpdateWebhookEndpointWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **endpointId** | **string** |  |  |
| **webhookEndpointPatchRequest** | [**WebhookEndpointPatchRequest**](WebhookEndpointPatchRequest.md) |  |  |

### Return type

[**WebhookEndpointResponse**](WebhookEndpointResponse.md)

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

