# InvoicePDFs.Api.DeliveriesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetDeliveryApiV1DeliveriesDeliveryIdGet**](DeliveriesApi.md#getdeliveryapiv1deliveriesdeliveryidget) | **GET** /api/v1/deliveries/{delivery_id} | Get Delivery |
| [**RetryDeliveryApiV1DeliveriesDeliveryIdRetryPost**](DeliveriesApi.md#retrydeliveryapiv1deliveriesdeliveryidretrypost) | **POST** /api/v1/deliveries/{delivery_id}/retry | Retry Delivery |

<a id="getdeliveryapiv1deliveriesdeliveryidget"></a>
# **GetDeliveryApiV1DeliveriesDeliveryIdGet**
> DeliveryResponse GetDeliveryApiV1DeliveriesDeliveryIdGet (string deliveryId)

Get Delivery

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetDeliveryApiV1DeliveriesDeliveryIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DeliveriesApi(config);
            var deliveryId = "deliveryId_example";  // string | 

            try
            {
                // Get Delivery
                DeliveryResponse result = apiInstance.GetDeliveryApiV1DeliveriesDeliveryIdGet(deliveryId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveriesApi.GetDeliveryApiV1DeliveriesDeliveryIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDeliveryApiV1DeliveriesDeliveryIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Delivery
    ApiResponse<DeliveryResponse> response = apiInstance.GetDeliveryApiV1DeliveriesDeliveryIdGetWithHttpInfo(deliveryId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveriesApi.GetDeliveryApiV1DeliveriesDeliveryIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryId** | **string** |  |  |

### Return type

[**DeliveryResponse**](DeliveryResponse.md)

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

<a id="retrydeliveryapiv1deliveriesdeliveryidretrypost"></a>
# **RetryDeliveryApiV1DeliveriesDeliveryIdRetryPost**
> DeliveryResponse RetryDeliveryApiV1DeliveriesDeliveryIdRetryPost (string deliveryId)

Retry Delivery

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RetryDeliveryApiV1DeliveriesDeliveryIdRetryPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new DeliveriesApi(config);
            var deliveryId = "deliveryId_example";  // string | 

            try
            {
                // Retry Delivery
                DeliveryResponse result = apiInstance.RetryDeliveryApiV1DeliveriesDeliveryIdRetryPost(deliveryId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DeliveriesApi.RetryDeliveryApiV1DeliveriesDeliveryIdRetryPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RetryDeliveryApiV1DeliveriesDeliveryIdRetryPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retry Delivery
    ApiResponse<DeliveryResponse> response = apiInstance.RetryDeliveryApiV1DeliveriesDeliveryIdRetryPostWithHttpInfo(deliveryId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DeliveriesApi.RetryDeliveryApiV1DeliveriesDeliveryIdRetryPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **deliveryId** | **string** |  |  |

### Return type

[**DeliveryResponse**](DeliveryResponse.md)

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

