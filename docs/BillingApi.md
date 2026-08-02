# InvoicePDFs.Api.BillingApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateCheckoutApiV1BillingCheckoutSessionPost**](BillingApi.md#createcheckoutapiv1billingcheckoutsessionpost) | **POST** /api/v1/billing/checkout-session | Create Checkout |
| [**CreatePortalApiV1BillingPortalSessionPost**](BillingApi.md#createportalapiv1billingportalsessionpost) | **POST** /api/v1/billing/portal-session | Create Portal |
| [**GetSubscriptionApiV1BillingSubscriptionGet**](BillingApi.md#getsubscriptionapiv1billingsubscriptionget) | **GET** /api/v1/billing/subscription | Get Subscription |
| [**ListPlansApiV1BillingPlansGet**](BillingApi.md#listplansapiv1billingplansget) | **GET** /api/v1/billing/plans | List Plans |

<a id="createcheckoutapiv1billingcheckoutsessionpost"></a>
# **CreateCheckoutApiV1BillingCheckoutSessionPost**
> BillingCheckoutResponse CreateCheckoutApiV1BillingCheckoutSessionPost (BillingCheckoutRequest billingCheckoutRequest)

Create Checkout

Create a Stripe Checkout session for a subscription.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateCheckoutApiV1BillingCheckoutSessionPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BillingApi(config);
            var billingCheckoutRequest = new BillingCheckoutRequest(); // BillingCheckoutRequest | 

            try
            {
                // Create Checkout
                BillingCheckoutResponse result = apiInstance.CreateCheckoutApiV1BillingCheckoutSessionPost(billingCheckoutRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BillingApi.CreateCheckoutApiV1BillingCheckoutSessionPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateCheckoutApiV1BillingCheckoutSessionPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Checkout
    ApiResponse<BillingCheckoutResponse> response = apiInstance.CreateCheckoutApiV1BillingCheckoutSessionPostWithHttpInfo(billingCheckoutRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BillingApi.CreateCheckoutApiV1BillingCheckoutSessionPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **billingCheckoutRequest** | [**BillingCheckoutRequest**](BillingCheckoutRequest.md) |  |  |

### Return type

[**BillingCheckoutResponse**](BillingCheckoutResponse.md)

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

<a id="createportalapiv1billingportalsessionpost"></a>
# **CreatePortalApiV1BillingPortalSessionPost**
> BillingPortalResponse CreatePortalApiV1BillingPortalSessionPost ()

Create Portal

Create a Stripe Customer Portal session for self-service management.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreatePortalApiV1BillingPortalSessionPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BillingApi(config);

            try
            {
                // Create Portal
                BillingPortalResponse result = apiInstance.CreatePortalApiV1BillingPortalSessionPost();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BillingApi.CreatePortalApiV1BillingPortalSessionPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreatePortalApiV1BillingPortalSessionPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Portal
    ApiResponse<BillingPortalResponse> response = apiInstance.CreatePortalApiV1BillingPortalSessionPostWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BillingApi.CreatePortalApiV1BillingPortalSessionPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**BillingPortalResponse**](BillingPortalResponse.md)

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

<a id="getsubscriptionapiv1billingsubscriptionget"></a>
# **GetSubscriptionApiV1BillingSubscriptionGet**
> BillingSubscriptionResponse GetSubscriptionApiV1BillingSubscriptionGet ()

Get Subscription

Get current subscription status (from DB, no Stripe API call).

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetSubscriptionApiV1BillingSubscriptionGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BillingApi(config);

            try
            {
                // Get Subscription
                BillingSubscriptionResponse result = apiInstance.GetSubscriptionApiV1BillingSubscriptionGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BillingApi.GetSubscriptionApiV1BillingSubscriptionGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSubscriptionApiV1BillingSubscriptionGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Subscription
    ApiResponse<BillingSubscriptionResponse> response = apiInstance.GetSubscriptionApiV1BillingSubscriptionGetWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BillingApi.GetSubscriptionApiV1BillingSubscriptionGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**BillingSubscriptionResponse**](BillingSubscriptionResponse.md)

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

<a id="listplansapiv1billingplansget"></a>
# **ListPlansApiV1BillingPlansGet**
> BillingPlansListResponse ListPlansApiV1BillingPlansGet ()

List Plans

Purchasable plans — the ones wired to a Stripe price.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListPlansApiV1BillingPlansGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new BillingApi(config);

            try
            {
                // List Plans
                BillingPlansListResponse result = apiInstance.ListPlansApiV1BillingPlansGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BillingApi.ListPlansApiV1BillingPlansGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListPlansApiV1BillingPlansGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Plans
    ApiResponse<BillingPlansListResponse> response = apiInstance.ListPlansApiV1BillingPlansGetWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BillingApi.ListPlansApiV1BillingPlansGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**BillingPlansListResponse**](BillingPlansListResponse.md)

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

