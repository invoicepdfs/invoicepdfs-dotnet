# InvoicePDFs.Api.WebhooksApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateWebhookEndpointApiV1WebhookEndpointsPost**](WebhooksApi.md#createwebhookendpointapiv1webhookendpointspost) | **POST** /api/v1/webhook-endpoints | Create Webhook Endpoint |
| [**DeleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete**](WebhooksApi.md#deletewebhookendpointapiv1webhookendpointsendpointiddelete) | **DELETE** /api/v1/webhook-endpoints/{endpoint_id} | Delete Webhook Endpoint |
| [**GetWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet**](WebhooksApi.md#getwebhookdeliveryapiv1webhookdeliveriesdeliveryidget) | **GET** /api/v1/webhook-deliveries/{delivery_id} | Get Webhook Delivery |
| [**GetWebhookEndpointApiV1WebhookEndpointsEndpointIdGet**](WebhooksApi.md#getwebhookendpointapiv1webhookendpointsendpointidget) | **GET** /api/v1/webhook-endpoints/{endpoint_id} | Get Webhook Endpoint |
| [**ListWebhookDeliveriesApiV1WebhookDeliveriesGet**](WebhooksApi.md#listwebhookdeliveriesapiv1webhookdeliveriesget) | **GET** /api/v1/webhook-deliveries | List Webhook Deliveries |
| [**ListWebhookEndpointsApiV1WebhookEndpointsGet**](WebhooksApi.md#listwebhookendpointsapiv1webhookendpointsget) | **GET** /api/v1/webhook-endpoints | List Webhook Endpoints |
| [**RetryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost**](WebhooksApi.md#retrywebhookdeliveryapiv1webhookdeliveriesdeliveryidretrypost) | **POST** /api/v1/webhook-deliveries/{delivery_id}/retry | Retry Webhook Delivery |
| [**RotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost**](WebhooksApi.md#rotatewebhooksecretapiv1webhookendpointsendpointidrotatesecretpost) | **POST** /api/v1/webhook-endpoints/{endpoint_id}/rotate-secret | Rotate Webhook Secret |
| [**TestWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost**](WebhooksApi.md#testwebhookendpointapiv1webhookendpointsendpointidtestpost) | **POST** /api/v1/webhook-endpoints/{endpoint_id}/test | Test Webhook Endpoint |
| [**UpdateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch**](WebhooksApi.md#updatewebhookendpointapiv1webhookendpointsendpointidpatch) | **PATCH** /api/v1/webhook-endpoints/{endpoint_id} | Update Webhook Endpoint |

<a id="createwebhookendpointapiv1webhookendpointspost"></a>
# **CreateWebhookEndpointApiV1WebhookEndpointsPost**
> WebhookEndpointResponse CreateWebhookEndpointApiV1WebhookEndpointsPost (WebhookEndpointCreateRequest webhookEndpointCreateRequest)

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
    public class CreateWebhookEndpointApiV1WebhookEndpointsPostExample
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
                WebhookEndpointResponse result = apiInstance.CreateWebhookEndpointApiV1WebhookEndpointsPost(webhookEndpointCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.CreateWebhookEndpointApiV1WebhookEndpointsPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateWebhookEndpointApiV1WebhookEndpointsPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Webhook Endpoint
    ApiResponse<WebhookEndpointResponse> response = apiInstance.CreateWebhookEndpointApiV1WebhookEndpointsPostWithHttpInfo(webhookEndpointCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.CreateWebhookEndpointApiV1WebhookEndpointsPostWithHttpInfo: " + e.Message);
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

<a id="deletewebhookendpointapiv1webhookendpointsendpointiddelete"></a>
# **DeleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete**
> SimpleBoolResponse DeleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete (string endpointId)

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
    public class DeleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDeleteExample
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
                SimpleBoolResponse result = apiInstance.DeleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete(endpointId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.DeleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Webhook Endpoint
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDeleteWithHttpInfo(endpointId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.DeleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDeleteWithHttpInfo: " + e.Message);
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

<a id="getwebhookdeliveryapiv1webhookdeliveriesdeliveryidget"></a>
# **GetWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet**
> WebhookDeliveryResponse GetWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet (string deliveryId)

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
    public class GetWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGetExample
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
                WebhookDeliveryResponse result = apiInstance.GetWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet(deliveryId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.GetWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Webhook Delivery
    ApiResponse<WebhookDeliveryResponse> response = apiInstance.GetWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGetWithHttpInfo(deliveryId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.GetWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGetWithHttpInfo: " + e.Message);
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

<a id="getwebhookendpointapiv1webhookendpointsendpointidget"></a>
# **GetWebhookEndpointApiV1WebhookEndpointsEndpointIdGet**
> WebhookEndpointResponse GetWebhookEndpointApiV1WebhookEndpointsEndpointIdGet (string endpointId)

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
    public class GetWebhookEndpointApiV1WebhookEndpointsEndpointIdGetExample
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
                WebhookEndpointResponse result = apiInstance.GetWebhookEndpointApiV1WebhookEndpointsEndpointIdGet(endpointId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.GetWebhookEndpointApiV1WebhookEndpointsEndpointIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWebhookEndpointApiV1WebhookEndpointsEndpointIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Webhook Endpoint
    ApiResponse<WebhookEndpointResponse> response = apiInstance.GetWebhookEndpointApiV1WebhookEndpointsEndpointIdGetWithHttpInfo(endpointId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.GetWebhookEndpointApiV1WebhookEndpointsEndpointIdGetWithHttpInfo: " + e.Message);
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

<a id="listwebhookdeliveriesapiv1webhookdeliveriesget"></a>
# **ListWebhookDeliveriesApiV1WebhookDeliveriesGet**
> WebhookDeliveriesListResponse ListWebhookDeliveriesApiV1WebhookDeliveriesGet (int? limit = null, string? cursor = null)

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
    public class ListWebhookDeliveriesApiV1WebhookDeliveriesGetExample
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
                WebhookDeliveriesListResponse result = apiInstance.ListWebhookDeliveriesApiV1WebhookDeliveriesGet(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.ListWebhookDeliveriesApiV1WebhookDeliveriesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWebhookDeliveriesApiV1WebhookDeliveriesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Webhook Deliveries
    ApiResponse<WebhookDeliveriesListResponse> response = apiInstance.ListWebhookDeliveriesApiV1WebhookDeliveriesGetWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.ListWebhookDeliveriesApiV1WebhookDeliveriesGetWithHttpInfo: " + e.Message);
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

<a id="listwebhookendpointsapiv1webhookendpointsget"></a>
# **ListWebhookEndpointsApiV1WebhookEndpointsGet**
> WebhookEndpointsListResponse ListWebhookEndpointsApiV1WebhookEndpointsGet (int? limit = null, string? cursor = null)

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
    public class ListWebhookEndpointsApiV1WebhookEndpointsGetExample
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
                WebhookEndpointsListResponse result = apiInstance.ListWebhookEndpointsApiV1WebhookEndpointsGet(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.ListWebhookEndpointsApiV1WebhookEndpointsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWebhookEndpointsApiV1WebhookEndpointsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Webhook Endpoints
    ApiResponse<WebhookEndpointsListResponse> response = apiInstance.ListWebhookEndpointsApiV1WebhookEndpointsGetWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.ListWebhookEndpointsApiV1WebhookEndpointsGetWithHttpInfo: " + e.Message);
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

<a id="retrywebhookdeliveryapiv1webhookdeliveriesdeliveryidretrypost"></a>
# **RetryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost**
> WebhookDeliveryResponse RetryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost (string deliveryId)

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
    public class RetryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPostExample
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
                WebhookDeliveryResponse result = apiInstance.RetryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost(deliveryId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.RetryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RetryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retry Webhook Delivery
    ApiResponse<WebhookDeliveryResponse> response = apiInstance.RetryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPostWithHttpInfo(deliveryId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.RetryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPostWithHttpInfo: " + e.Message);
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

<a id="rotatewebhooksecretapiv1webhookendpointsendpointidrotatesecretpost"></a>
# **RotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost**
> WebhookSecretResponse RotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost (string endpointId)

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
    public class RotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPostExample
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
                WebhookSecretResponse result = apiInstance.RotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost(endpointId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.RotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Rotate Webhook Secret
    ApiResponse<WebhookSecretResponse> response = apiInstance.RotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPostWithHttpInfo(endpointId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.RotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPostWithHttpInfo: " + e.Message);
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

<a id="testwebhookendpointapiv1webhookendpointsendpointidtestpost"></a>
# **TestWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost**
> WebhookDeliveryResponse TestWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost (string endpointId)

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
    public class TestWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPostExample
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
                WebhookDeliveryResponse result = apiInstance.TestWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost(endpointId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.TestWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TestWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Test Webhook Endpoint
    ApiResponse<WebhookDeliveryResponse> response = apiInstance.TestWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPostWithHttpInfo(endpointId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.TestWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPostWithHttpInfo: " + e.Message);
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

<a id="updatewebhookendpointapiv1webhookendpointsendpointidpatch"></a>
# **UpdateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch**
> WebhookEndpointResponse UpdateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch (string endpointId, WebhookEndpointPatchRequest webhookEndpointPatchRequest)

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
    public class UpdateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatchExample
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
                WebhookEndpointResponse result = apiInstance.UpdateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch(endpointId, webhookEndpointPatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.UpdateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Webhook Endpoint
    ApiResponse<WebhookEndpointResponse> response = apiInstance.UpdateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatchWithHttpInfo(endpointId, webhookEndpointPatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.UpdateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatchWithHttpInfo: " + e.Message);
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

