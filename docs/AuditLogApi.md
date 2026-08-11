# InvoicePDFs.Api.AuditLogApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetAuditEvent**](AuditLogApi.md#getauditevent) | **GET** /api/v1/audit-events/{audit_event_id} | Get Audit Event |
| [**ListAuditEvents**](AuditLogApi.md#listauditevents) | **GET** /api/v1/audit-events | List Audit Events |

<a id="getauditevent"></a>
# **GetAuditEvent**
> AuditEventResponse GetAuditEvent (string auditEventId)

Get Audit Event

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetAuditEventExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new AuditLogApi(config);
            var auditEventId = "auditEventId_example";  // string | 

            try
            {
                // Get Audit Event
                AuditEventResponse result = apiInstance.GetAuditEvent(auditEventId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuditLogApi.GetAuditEvent: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAuditEventWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Audit Event
    ApiResponse<AuditEventResponse> response = apiInstance.GetAuditEventWithHttpInfo(auditEventId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuditLogApi.GetAuditEventWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **auditEventId** | **string** |  |  |

### Return type

[**AuditEventResponse**](AuditEventResponse.md)

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

<a id="listauditevents"></a>
# **ListAuditEvents**
> AuditEventsListResponse ListAuditEvents (int? limit = null, string? cursor = null, string? action = null, string? resourceType = null, string? resourceId = null)

List Audit Events

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListAuditEventsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new AuditLogApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 
            var action = "action_example";  // string? |  (optional) 
            var resourceType = "resourceType_example";  // string? |  (optional) 
            var resourceId = "resourceId_example";  // string? |  (optional) 

            try
            {
                // List Audit Events
                AuditEventsListResponse result = apiInstance.ListAuditEvents(limit, cursor, action, resourceType, resourceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuditLogApi.ListAuditEvents: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListAuditEventsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Audit Events
    ApiResponse<AuditEventsListResponse> response = apiInstance.ListAuditEventsWithHttpInfo(limit, cursor, action, resourceType, resourceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuditLogApi.ListAuditEventsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **limit** | **int?** |  | [optional] [default to 50] |
| **cursor** | **string?** |  | [optional]  |
| **action** | **string?** |  | [optional]  |
| **resourceType** | **string?** |  | [optional]  |
| **resourceId** | **string?** |  | [optional]  |

### Return type

[**AuditEventsListResponse**](AuditEventsListResponse.md)

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

