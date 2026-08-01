# InvoicePDFs.Api.PaymentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreatePaymentApiV1InvoicesInvoiceIdPaymentsPost**](PaymentsApi.md#createpaymentapiv1invoicesinvoiceidpaymentspost) | **POST** /api/v1/invoices/{invoice_id}/payments | Create Payment |
| [**DeletePaymentApiV1PaymentsPaymentIdDelete**](PaymentsApi.md#deletepaymentapiv1paymentspaymentiddelete) | **DELETE** /api/v1/payments/{payment_id} | Delete Payment |
| [**GetPaymentApiV1PaymentsPaymentIdGet**](PaymentsApi.md#getpaymentapiv1paymentspaymentidget) | **GET** /api/v1/payments/{payment_id} | Get Payment |
| [**ListInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGet**](PaymentsApi.md#listinvoicepaymentsapiv1invoicesinvoiceidpaymentsget) | **GET** /api/v1/invoices/{invoice_id}/payments | List Invoice Payments |
| [**UpdatePaymentApiV1PaymentsPaymentIdPatch**](PaymentsApi.md#updatepaymentapiv1paymentspaymentidpatch) | **PATCH** /api/v1/payments/{payment_id} | Update Payment |

<a id="createpaymentapiv1invoicesinvoiceidpaymentspost"></a>
# **CreatePaymentApiV1InvoicesInvoiceIdPaymentsPost**
> PaymentResponse CreatePaymentApiV1InvoicesInvoiceIdPaymentsPost (string invoiceId, PaymentCreateRequest paymentCreateRequest)

Create Payment

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreatePaymentApiV1InvoicesInvoiceIdPaymentsPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PaymentsApi(config);
            var invoiceId = "invoiceId_example";  // string | 
            var paymentCreateRequest = new PaymentCreateRequest(); // PaymentCreateRequest | 

            try
            {
                // Create Payment
                PaymentResponse result = apiInstance.CreatePaymentApiV1InvoicesInvoiceIdPaymentsPost(invoiceId, paymentCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PaymentsApi.CreatePaymentApiV1InvoicesInvoiceIdPaymentsPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreatePaymentApiV1InvoicesInvoiceIdPaymentsPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Payment
    ApiResponse<PaymentResponse> response = apiInstance.CreatePaymentApiV1InvoicesInvoiceIdPaymentsPostWithHttpInfo(invoiceId, paymentCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PaymentsApi.CreatePaymentApiV1InvoicesInvoiceIdPaymentsPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |
| **paymentCreateRequest** | [**PaymentCreateRequest**](PaymentCreateRequest.md) |  |  |

### Return type

[**PaymentResponse**](PaymentResponse.md)

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

<a id="deletepaymentapiv1paymentspaymentiddelete"></a>
# **DeletePaymentApiV1PaymentsPaymentIdDelete**
> SimpleBoolResponse DeletePaymentApiV1PaymentsPaymentIdDelete (string paymentId)

Delete Payment

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeletePaymentApiV1PaymentsPaymentIdDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PaymentsApi(config);
            var paymentId = "paymentId_example";  // string | 

            try
            {
                // Delete Payment
                SimpleBoolResponse result = apiInstance.DeletePaymentApiV1PaymentsPaymentIdDelete(paymentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PaymentsApi.DeletePaymentApiV1PaymentsPaymentIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeletePaymentApiV1PaymentsPaymentIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Payment
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeletePaymentApiV1PaymentsPaymentIdDeleteWithHttpInfo(paymentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PaymentsApi.DeletePaymentApiV1PaymentsPaymentIdDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **paymentId** | **string** |  |  |

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

<a id="getpaymentapiv1paymentspaymentidget"></a>
# **GetPaymentApiV1PaymentsPaymentIdGet**
> PaymentResponse GetPaymentApiV1PaymentsPaymentIdGet (string paymentId)

Get Payment

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetPaymentApiV1PaymentsPaymentIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PaymentsApi(config);
            var paymentId = "paymentId_example";  // string | 

            try
            {
                // Get Payment
                PaymentResponse result = apiInstance.GetPaymentApiV1PaymentsPaymentIdGet(paymentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PaymentsApi.GetPaymentApiV1PaymentsPaymentIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPaymentApiV1PaymentsPaymentIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Payment
    ApiResponse<PaymentResponse> response = apiInstance.GetPaymentApiV1PaymentsPaymentIdGetWithHttpInfo(paymentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PaymentsApi.GetPaymentApiV1PaymentsPaymentIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **paymentId** | **string** |  |  |

### Return type

[**PaymentResponse**](PaymentResponse.md)

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

<a id="listinvoicepaymentsapiv1invoicesinvoiceidpaymentsget"></a>
# **ListInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGet**
> PaymentsListResponse ListInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGet (string invoiceId, int? limit = null, string? cursor = null)

List Invoice Payments

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PaymentsApi(config);
            var invoiceId = "invoiceId_example";  // string | 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Invoice Payments
                PaymentsListResponse result = apiInstance.ListInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGet(invoiceId, limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PaymentsApi.ListInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Invoice Payments
    ApiResponse<PaymentsListResponse> response = apiInstance.ListInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGetWithHttpInfo(invoiceId, limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PaymentsApi.ListInvoicePaymentsApiV1InvoicesInvoiceIdPaymentsGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **invoiceId** | **string** |  |  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** |  | [optional]  |

### Return type

[**PaymentsListResponse**](PaymentsListResponse.md)

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

<a id="updatepaymentapiv1paymentspaymentidpatch"></a>
# **UpdatePaymentApiV1PaymentsPaymentIdPatch**
> PaymentResponse UpdatePaymentApiV1PaymentsPaymentIdPatch (string paymentId, PaymentPatchRequest paymentPatchRequest)

Update Payment

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UpdatePaymentApiV1PaymentsPaymentIdPatchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new PaymentsApi(config);
            var paymentId = "paymentId_example";  // string | 
            var paymentPatchRequest = new PaymentPatchRequest(); // PaymentPatchRequest | 

            try
            {
                // Update Payment
                PaymentResponse result = apiInstance.UpdatePaymentApiV1PaymentsPaymentIdPatch(paymentId, paymentPatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PaymentsApi.UpdatePaymentApiV1PaymentsPaymentIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdatePaymentApiV1PaymentsPaymentIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Payment
    ApiResponse<PaymentResponse> response = apiInstance.UpdatePaymentApiV1PaymentsPaymentIdPatchWithHttpInfo(paymentId, paymentPatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PaymentsApi.UpdatePaymentApiV1PaymentsPaymentIdPatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **paymentId** | **string** |  |  |
| **paymentPatchRequest** | [**PaymentPatchRequest**](PaymentPatchRequest.md) |  |  |

### Return type

[**PaymentResponse**](PaymentResponse.md)

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

