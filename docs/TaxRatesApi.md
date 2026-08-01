# InvoicePDFs.Api.TaxRatesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTaxRateApiV1TaxRatesPost**](TaxRatesApi.md#createtaxrateapiv1taxratespost) | **POST** /api/v1/tax-rates | Create Tax Rate |
| [**DeleteTaxRateApiV1TaxRatesTaxRateIdDelete**](TaxRatesApi.md#deletetaxrateapiv1taxratestaxrateiddelete) | **DELETE** /api/v1/tax-rates/{tax_rate_id} | Delete Tax Rate |
| [**GetTaxRateApiV1TaxRatesTaxRateIdGet**](TaxRatesApi.md#gettaxrateapiv1taxratestaxrateidget) | **GET** /api/v1/tax-rates/{tax_rate_id} | Get Tax Rate |
| [**ListTaxRatesApiV1TaxRatesGet**](TaxRatesApi.md#listtaxratesapiv1taxratesget) | **GET** /api/v1/tax-rates | List Tax Rates |
| [**UpdateTaxRateApiV1TaxRatesTaxRateIdPatch**](TaxRatesApi.md#updatetaxrateapiv1taxratestaxrateidpatch) | **PATCH** /api/v1/tax-rates/{tax_rate_id} | Update Tax Rate |

<a id="createtaxrateapiv1taxratespost"></a>
# **CreateTaxRateApiV1TaxRatesPost**
> TaxRateResponse CreateTaxRateApiV1TaxRatesPost (TaxRateCreateRequest taxRateCreateRequest)

Create Tax Rate

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateTaxRateApiV1TaxRatesPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TaxRatesApi(config);
            var taxRateCreateRequest = new TaxRateCreateRequest(); // TaxRateCreateRequest | 

            try
            {
                // Create Tax Rate
                TaxRateResponse result = apiInstance.CreateTaxRateApiV1TaxRatesPost(taxRateCreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TaxRatesApi.CreateTaxRateApiV1TaxRatesPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTaxRateApiV1TaxRatesPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Tax Rate
    ApiResponse<TaxRateResponse> response = apiInstance.CreateTaxRateApiV1TaxRatesPostWithHttpInfo(taxRateCreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TaxRatesApi.CreateTaxRateApiV1TaxRatesPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taxRateCreateRequest** | [**TaxRateCreateRequest**](TaxRateCreateRequest.md) |  |  |

### Return type

[**TaxRateResponse**](TaxRateResponse.md)

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

<a id="deletetaxrateapiv1taxratestaxrateiddelete"></a>
# **DeleteTaxRateApiV1TaxRatesTaxRateIdDelete**
> SimpleBoolResponse DeleteTaxRateApiV1TaxRatesTaxRateIdDelete (string taxRateId)

Delete Tax Rate

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteTaxRateApiV1TaxRatesTaxRateIdDeleteExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TaxRatesApi(config);
            var taxRateId = "taxRateId_example";  // string | 

            try
            {
                // Delete Tax Rate
                SimpleBoolResponse result = apiInstance.DeleteTaxRateApiV1TaxRatesTaxRateIdDelete(taxRateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TaxRatesApi.DeleteTaxRateApiV1TaxRatesTaxRateIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTaxRateApiV1TaxRatesTaxRateIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Tax Rate
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteTaxRateApiV1TaxRatesTaxRateIdDeleteWithHttpInfo(taxRateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TaxRatesApi.DeleteTaxRateApiV1TaxRatesTaxRateIdDeleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taxRateId** | **string** |  |  |

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

<a id="gettaxrateapiv1taxratestaxrateidget"></a>
# **GetTaxRateApiV1TaxRatesTaxRateIdGet**
> TaxRateResponse GetTaxRateApiV1TaxRatesTaxRateIdGet (string taxRateId)

Get Tax Rate

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetTaxRateApiV1TaxRatesTaxRateIdGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TaxRatesApi(config);
            var taxRateId = "taxRateId_example";  // string | 

            try
            {
                // Get Tax Rate
                TaxRateResponse result = apiInstance.GetTaxRateApiV1TaxRatesTaxRateIdGet(taxRateId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TaxRatesApi.GetTaxRateApiV1TaxRatesTaxRateIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTaxRateApiV1TaxRatesTaxRateIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Tax Rate
    ApiResponse<TaxRateResponse> response = apiInstance.GetTaxRateApiV1TaxRatesTaxRateIdGetWithHttpInfo(taxRateId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TaxRatesApi.GetTaxRateApiV1TaxRatesTaxRateIdGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taxRateId** | **string** |  |  |

### Return type

[**TaxRateResponse**](TaxRateResponse.md)

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

<a id="listtaxratesapiv1taxratesget"></a>
# **ListTaxRatesApiV1TaxRatesGet**
> TaxRatesListResponse ListTaxRatesApiV1TaxRatesGet (int? limit = null, string? cursor = null)

List Tax Rates

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListTaxRatesApiV1TaxRatesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TaxRatesApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Tax Rates
                TaxRatesListResponse result = apiInstance.ListTaxRatesApiV1TaxRatesGet(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TaxRatesApi.ListTaxRatesApiV1TaxRatesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTaxRatesApiV1TaxRatesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Tax Rates
    ApiResponse<TaxRatesListResponse> response = apiInstance.ListTaxRatesApiV1TaxRatesGetWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TaxRatesApi.ListTaxRatesApiV1TaxRatesGetWithHttpInfo: " + e.Message);
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

[**TaxRatesListResponse**](TaxRatesListResponse.md)

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

<a id="updatetaxrateapiv1taxratestaxrateidpatch"></a>
# **UpdateTaxRateApiV1TaxRatesTaxRateIdPatch**
> TaxRateResponse UpdateTaxRateApiV1TaxRatesTaxRateIdPatch (string taxRateId, TaxRatePatchRequest taxRatePatchRequest)

Update Tax Rate

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UpdateTaxRateApiV1TaxRatesTaxRateIdPatchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new TaxRatesApi(config);
            var taxRateId = "taxRateId_example";  // string | 
            var taxRatePatchRequest = new TaxRatePatchRequest(); // TaxRatePatchRequest | 

            try
            {
                // Update Tax Rate
                TaxRateResponse result = apiInstance.UpdateTaxRateApiV1TaxRatesTaxRateIdPatch(taxRateId, taxRatePatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TaxRatesApi.UpdateTaxRateApiV1TaxRatesTaxRateIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTaxRateApiV1TaxRatesTaxRateIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Tax Rate
    ApiResponse<TaxRateResponse> response = apiInstance.UpdateTaxRateApiV1TaxRatesTaxRateIdPatchWithHttpInfo(taxRateId, taxRatePatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TaxRatesApi.UpdateTaxRateApiV1TaxRatesTaxRateIdPatchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **taxRateId** | **string** |  |  |
| **taxRatePatchRequest** | [**TaxRatePatchRequest**](TaxRatePatchRequest.md) |  |  |

### Return type

[**TaxRateResponse**](TaxRateResponse.md)

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

