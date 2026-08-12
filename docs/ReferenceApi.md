# InvoicePDFs.Api.ReferenceApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ListCountries**](ReferenceApi.md#listcountries) | **GET** /api/v1/reference/countries | List Countries |
| [**ListCurrencies**](ReferenceApi.md#listcurrencies) | **GET** /api/v1/reference/currencies | List Currencies |
| [**ListDocumentTypes**](ReferenceApi.md#listdocumenttypes) | **GET** /api/v1/reference/document-types | List Document Types |
| [**ListLocales**](ReferenceApi.md#listlocales) | **GET** /api/v1/reference/locales | List Locales |
| [**ListPageSizes**](ReferenceApi.md#listpagesizes) | **GET** /api/v1/reference/page-sizes | List Page Sizes |
| [**ListTimezones**](ReferenceApi.md#listtimezones) | **GET** /api/v1/reference/timezones | List Timezones |

<a id="listcountries"></a>
# **ListCountries**
> CountriesListResponse ListCountries ()

List Countries

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListCountriesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new ReferenceApi(config);

            try
            {
                // List Countries
                CountriesListResponse result = apiInstance.ListCountries();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReferenceApi.ListCountries: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCountriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Countries
    ApiResponse<CountriesListResponse> response = apiInstance.ListCountriesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReferenceApi.ListCountriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**CountriesListResponse**](CountriesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listcurrencies"></a>
# **ListCurrencies**
> CurrenciesListResponse ListCurrencies ()

List Currencies

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListCurrenciesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new ReferenceApi(config);

            try
            {
                // List Currencies
                CurrenciesListResponse result = apiInstance.ListCurrencies();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReferenceApi.ListCurrencies: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCurrenciesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Currencies
    ApiResponse<CurrenciesListResponse> response = apiInstance.ListCurrenciesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReferenceApi.ListCurrenciesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**CurrenciesListResponse**](CurrenciesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listdocumenttypes"></a>
# **ListDocumentTypes**
> DocumentTypesListResponse ListDocumentTypes ()

List Document Types

List every supported document type with the metadata a client needs to build a type-aware create form: the number prefix, whether it is payable / takes a source document / supports a reason, which line-item shape it uses (``standard`` = priced, ``shipped`` = quantities only), and the lifecycle actions available to it.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListDocumentTypesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new ReferenceApi(config);

            try
            {
                // List Document Types
                DocumentTypesListResponse result = apiInstance.ListDocumentTypes();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReferenceApi.ListDocumentTypes: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListDocumentTypesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Document Types
    ApiResponse<DocumentTypesListResponse> response = apiInstance.ListDocumentTypesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReferenceApi.ListDocumentTypesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**DocumentTypesListResponse**](DocumentTypesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listlocales"></a>
# **ListLocales**
> LocalesListResponse ListLocales ()

List Locales

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListLocalesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new ReferenceApi(config);

            try
            {
                // List Locales
                LocalesListResponse result = apiInstance.ListLocales();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReferenceApi.ListLocales: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListLocalesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Locales
    ApiResponse<LocalesListResponse> response = apiInstance.ListLocalesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReferenceApi.ListLocalesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**LocalesListResponse**](LocalesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listpagesizes"></a>
# **ListPageSizes**
> PageSizesListResponse ListPageSizes ()

List Page Sizes

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListPageSizesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new ReferenceApi(config);

            try
            {
                // List Page Sizes
                PageSizesListResponse result = apiInstance.ListPageSizes();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReferenceApi.ListPageSizes: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListPageSizesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Page Sizes
    ApiResponse<PageSizesListResponse> response = apiInstance.ListPageSizesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReferenceApi.ListPageSizesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**PageSizesListResponse**](PageSizesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="listtimezones"></a>
# **ListTimezones**
> TimezonesListResponse ListTimezones ()

List Timezones

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListTimezonesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new ReferenceApi(config);

            try
            {
                // List Timezones
                TimezonesListResponse result = apiInstance.ListTimezones();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReferenceApi.ListTimezones: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTimezonesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Timezones
    ApiResponse<TimezonesListResponse> response = apiInstance.ListTimezonesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReferenceApi.ListTimezonesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**TimezonesListResponse**](TimezonesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

