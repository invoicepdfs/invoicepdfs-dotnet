# InvoicePDFs.Api.ReferenceApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ListCountriesApiV1ReferenceCountriesGet**](ReferenceApi.md#listcountriesapiv1referencecountriesget) | **GET** /api/v1/reference/countries | List Countries |
| [**ListCurrenciesApiV1ReferenceCurrenciesGet**](ReferenceApi.md#listcurrenciesapiv1referencecurrenciesget) | **GET** /api/v1/reference/currencies | List Currencies |
| [**ListDocumentTypesApiV1ReferenceDocumentTypesGet**](ReferenceApi.md#listdocumenttypesapiv1referencedocumenttypesget) | **GET** /api/v1/reference/document-types | List Document Types |
| [**ListLocalesApiV1ReferenceLocalesGet**](ReferenceApi.md#listlocalesapiv1referencelocalesget) | **GET** /api/v1/reference/locales | List Locales |
| [**ListPageSizesApiV1ReferencePageSizesGet**](ReferenceApi.md#listpagesizesapiv1referencepagesizesget) | **GET** /api/v1/reference/page-sizes | List Page Sizes |
| [**ListTimezonesApiV1ReferenceTimezonesGet**](ReferenceApi.md#listtimezonesapiv1referencetimezonesget) | **GET** /api/v1/reference/timezones | List Timezones |

<a id="listcountriesapiv1referencecountriesget"></a>
# **ListCountriesApiV1ReferenceCountriesGet**
> Dictionary&lt;string, Object&gt; ListCountriesApiV1ReferenceCountriesGet ()

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
    public class ListCountriesApiV1ReferenceCountriesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new ReferenceApi(config);

            try
            {
                // List Countries
                Dictionary<string, Object> result = apiInstance.ListCountriesApiV1ReferenceCountriesGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReferenceApi.ListCountriesApiV1ReferenceCountriesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCountriesApiV1ReferenceCountriesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Countries
    ApiResponse<Dictionary<string, Object>> response = apiInstance.ListCountriesApiV1ReferenceCountriesGetWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReferenceApi.ListCountriesApiV1ReferenceCountriesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**Dictionary<string, Object>**

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

<a id="listcurrenciesapiv1referencecurrenciesget"></a>
# **ListCurrenciesApiV1ReferenceCurrenciesGet**
> Dictionary&lt;string, Object&gt; ListCurrenciesApiV1ReferenceCurrenciesGet ()

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
    public class ListCurrenciesApiV1ReferenceCurrenciesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new ReferenceApi(config);

            try
            {
                // List Currencies
                Dictionary<string, Object> result = apiInstance.ListCurrenciesApiV1ReferenceCurrenciesGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReferenceApi.ListCurrenciesApiV1ReferenceCurrenciesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListCurrenciesApiV1ReferenceCurrenciesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Currencies
    ApiResponse<Dictionary<string, Object>> response = apiInstance.ListCurrenciesApiV1ReferenceCurrenciesGetWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReferenceApi.ListCurrenciesApiV1ReferenceCurrenciesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**Dictionary<string, Object>**

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

<a id="listdocumenttypesapiv1referencedocumenttypesget"></a>
# **ListDocumentTypesApiV1ReferenceDocumentTypesGet**
> Dictionary&lt;string, Object&gt; ListDocumentTypesApiV1ReferenceDocumentTypesGet ()

List Document Types

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListDocumentTypesApiV1ReferenceDocumentTypesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new ReferenceApi(config);

            try
            {
                // List Document Types
                Dictionary<string, Object> result = apiInstance.ListDocumentTypesApiV1ReferenceDocumentTypesGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReferenceApi.ListDocumentTypesApiV1ReferenceDocumentTypesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListDocumentTypesApiV1ReferenceDocumentTypesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Document Types
    ApiResponse<Dictionary<string, Object>> response = apiInstance.ListDocumentTypesApiV1ReferenceDocumentTypesGetWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReferenceApi.ListDocumentTypesApiV1ReferenceDocumentTypesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**Dictionary<string, Object>**

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

<a id="listlocalesapiv1referencelocalesget"></a>
# **ListLocalesApiV1ReferenceLocalesGet**
> Dictionary&lt;string, Object&gt; ListLocalesApiV1ReferenceLocalesGet ()

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
    public class ListLocalesApiV1ReferenceLocalesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new ReferenceApi(config);

            try
            {
                // List Locales
                Dictionary<string, Object> result = apiInstance.ListLocalesApiV1ReferenceLocalesGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReferenceApi.ListLocalesApiV1ReferenceLocalesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListLocalesApiV1ReferenceLocalesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Locales
    ApiResponse<Dictionary<string, Object>> response = apiInstance.ListLocalesApiV1ReferenceLocalesGetWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReferenceApi.ListLocalesApiV1ReferenceLocalesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**Dictionary<string, Object>**

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

<a id="listpagesizesapiv1referencepagesizesget"></a>
# **ListPageSizesApiV1ReferencePageSizesGet**
> Dictionary&lt;string, Object&gt; ListPageSizesApiV1ReferencePageSizesGet ()

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
    public class ListPageSizesApiV1ReferencePageSizesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new ReferenceApi(config);

            try
            {
                // List Page Sizes
                Dictionary<string, Object> result = apiInstance.ListPageSizesApiV1ReferencePageSizesGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReferenceApi.ListPageSizesApiV1ReferencePageSizesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListPageSizesApiV1ReferencePageSizesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Page Sizes
    ApiResponse<Dictionary<string, Object>> response = apiInstance.ListPageSizesApiV1ReferencePageSizesGetWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReferenceApi.ListPageSizesApiV1ReferencePageSizesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**Dictionary<string, Object>**

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

<a id="listtimezonesapiv1referencetimezonesget"></a>
# **ListTimezonesApiV1ReferenceTimezonesGet**
> Dictionary&lt;string, Object&gt; ListTimezonesApiV1ReferenceTimezonesGet ()

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
    public class ListTimezonesApiV1ReferenceTimezonesGetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new ReferenceApi(config);

            try
            {
                // List Timezones
                Dictionary<string, Object> result = apiInstance.ListTimezonesApiV1ReferenceTimezonesGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReferenceApi.ListTimezonesApiV1ReferenceTimezonesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListTimezonesApiV1ReferenceTimezonesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Timezones
    ApiResponse<Dictionary<string, Object>> response = apiInstance.ListTimezonesApiV1ReferenceTimezonesGetWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReferenceApi.ListTimezonesApiV1ReferenceTimezonesGetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**Dictionary<string, Object>**

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

