# InvoicePDFs.Api.WorkspacesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddWorkspaceMember**](WorkspacesApi.md#addworkspacemember) | **POST** /api/v1/workspaces/{workspace_id}/members | Add Workspace Member |
| [**CreateWorkspace**](WorkspacesApi.md#createworkspace) | **POST** /api/v1/workspaces | Create Workspace |
| [**DeleteWorkspace**](WorkspacesApi.md#deleteworkspace) | **DELETE** /api/v1/workspaces/{workspace_id} | Delete Workspace |
| [**GetWorkspace**](WorkspacesApi.md#getworkspace) | **GET** /api/v1/workspaces/{workspace_id} | Get Workspace |
| [**ListWorkspaceMembers**](WorkspacesApi.md#listworkspacemembers) | **GET** /api/v1/workspaces/{workspace_id}/members | List Workspace Members |
| [**ListWorkspaces**](WorkspacesApi.md#listworkspaces) | **GET** /api/v1/workspaces | List Workspaces |
| [**RemoveWorkspaceMember**](WorkspacesApi.md#removeworkspacemember) | **DELETE** /api/v1/workspaces/{workspace_id}/members/{member_id} | Remove Workspace Member |
| [**UpdateWorkspace**](WorkspacesApi.md#updateworkspace) | **PATCH** /api/v1/workspaces/{workspace_id} | Update Workspace |
| [**UpdateWorkspaceMember**](WorkspacesApi.md#updateworkspacemember) | **PATCH** /api/v1/workspaces/{workspace_id}/members/{member_id} | Update Workspace Member |

<a id="addworkspacemember"></a>
# **AddWorkspaceMember**
> WorkspaceMembersListResponse AddWorkspaceMember (string workspaceId, WorkspaceMemberCreateRequest workspaceMemberCreateRequest, string? idempotencyKey = null)

Add Workspace Member

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class AddWorkspaceMemberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WorkspacesApi(config);
            var workspaceId = "workspaceId_example";  // string | 
            var workspaceMemberCreateRequest = new WorkspaceMemberCreateRequest(); // WorkspaceMemberCreateRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Add Workspace Member
                WorkspaceMembersListResponse result = apiInstance.AddWorkspaceMember(workspaceId, workspaceMemberCreateRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.AddWorkspaceMember: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddWorkspaceMemberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add Workspace Member
    ApiResponse<WorkspaceMembersListResponse> response = apiInstance.AddWorkspaceMemberWithHttpInfo(workspaceId, workspaceMemberCreateRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.AddWorkspaceMemberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceId** | **string** |  |  |
| **workspaceMemberCreateRequest** | [**WorkspaceMemberCreateRequest**](WorkspaceMemberCreateRequest.md) |  |  |
| **idempotencyKey** | **string?** |  | [optional]  |

### Return type

[**WorkspaceMembersListResponse**](WorkspaceMembersListResponse.md)

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

<a id="createworkspace"></a>
# **CreateWorkspace**
> WorkspaceResponse CreateWorkspace (WorkspaceCreateRequest workspaceCreateRequest, string? idempotencyKey = null)

Create Workspace

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateWorkspaceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WorkspacesApi(config);
            var workspaceCreateRequest = new WorkspaceCreateRequest(); // WorkspaceCreateRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Create Workspace
                WorkspaceResponse result = apiInstance.CreateWorkspace(workspaceCreateRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.CreateWorkspace: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateWorkspaceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Workspace
    ApiResponse<WorkspaceResponse> response = apiInstance.CreateWorkspaceWithHttpInfo(workspaceCreateRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.CreateWorkspaceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceCreateRequest** | [**WorkspaceCreateRequest**](WorkspaceCreateRequest.md) |  |  |
| **idempotencyKey** | **string?** |  | [optional]  |

### Return type

[**WorkspaceResponse**](WorkspaceResponse.md)

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

<a id="deleteworkspace"></a>
# **DeleteWorkspace**
> SimpleBoolResponse DeleteWorkspace (string workspaceId)

Delete Workspace

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteWorkspaceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WorkspacesApi(config);
            var workspaceId = "workspaceId_example";  // string | 

            try
            {
                // Delete Workspace
                SimpleBoolResponse result = apiInstance.DeleteWorkspace(workspaceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.DeleteWorkspace: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteWorkspaceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Workspace
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteWorkspaceWithHttpInfo(workspaceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.DeleteWorkspaceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceId** | **string** |  |  |

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

<a id="getworkspace"></a>
# **GetWorkspace**
> WorkspaceResponse GetWorkspace (string workspaceId)

Get Workspace

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetWorkspaceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WorkspacesApi(config);
            var workspaceId = "workspaceId_example";  // string | 

            try
            {
                // Get Workspace
                WorkspaceResponse result = apiInstance.GetWorkspace(workspaceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.GetWorkspace: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWorkspaceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Workspace
    ApiResponse<WorkspaceResponse> response = apiInstance.GetWorkspaceWithHttpInfo(workspaceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.GetWorkspaceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceId** | **string** |  |  |

### Return type

[**WorkspaceResponse**](WorkspaceResponse.md)

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

<a id="listworkspacemembers"></a>
# **ListWorkspaceMembers**
> WorkspaceMembersListResponse ListWorkspaceMembers (string workspaceId)

List Workspace Members

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListWorkspaceMembersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WorkspacesApi(config);
            var workspaceId = "workspaceId_example";  // string | 

            try
            {
                // List Workspace Members
                WorkspaceMembersListResponse result = apiInstance.ListWorkspaceMembers(workspaceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.ListWorkspaceMembers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWorkspaceMembersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Workspace Members
    ApiResponse<WorkspaceMembersListResponse> response = apiInstance.ListWorkspaceMembersWithHttpInfo(workspaceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.ListWorkspaceMembersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceId** | **string** |  |  |

### Return type

[**WorkspaceMembersListResponse**](WorkspaceMembersListResponse.md)

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

<a id="listworkspaces"></a>
# **ListWorkspaces**
> WorkspacesListResponse ListWorkspaces (int? limit = null, string? cursor = null)

List Workspaces

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListWorkspacesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WorkspacesApi(config);
            var limit = 50;  // int? |  (optional)  (default to 50)
            var cursor = "cursor_example";  // string? |  (optional) 

            try
            {
                // List Workspaces
                WorkspacesListResponse result = apiInstance.ListWorkspaces(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.ListWorkspaces: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWorkspacesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Workspaces
    ApiResponse<WorkspacesListResponse> response = apiInstance.ListWorkspacesWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.ListWorkspacesWithHttpInfo: " + e.Message);
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

[**WorkspacesListResponse**](WorkspacesListResponse.md)

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

<a id="removeworkspacemember"></a>
# **RemoveWorkspaceMember**
> SimpleBoolResponse RemoveWorkspaceMember (string workspaceId, string memberId)

Remove Workspace Member

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RemoveWorkspaceMemberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WorkspacesApi(config);
            var workspaceId = "workspaceId_example";  // string | 
            var memberId = "memberId_example";  // string | 

            try
            {
                // Remove Workspace Member
                SimpleBoolResponse result = apiInstance.RemoveWorkspaceMember(workspaceId, memberId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.RemoveWorkspaceMember: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveWorkspaceMemberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Remove Workspace Member
    ApiResponse<SimpleBoolResponse> response = apiInstance.RemoveWorkspaceMemberWithHttpInfo(workspaceId, memberId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.RemoveWorkspaceMemberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceId** | **string** |  |  |
| **memberId** | **string** |  |  |

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

<a id="updateworkspace"></a>
# **UpdateWorkspace**
> WorkspaceResponse UpdateWorkspace (string workspaceId, WorkspacePatchRequest workspacePatchRequest, string? idempotencyKey = null)

Update Workspace

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UpdateWorkspaceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WorkspacesApi(config);
            var workspaceId = "workspaceId_example";  // string | 
            var workspacePatchRequest = new WorkspacePatchRequest(); // WorkspacePatchRequest | 
            var idempotencyKey = "idempotencyKey_example";  // string? |  (optional) 

            try
            {
                // Update Workspace
                WorkspaceResponse result = apiInstance.UpdateWorkspace(workspaceId, workspacePatchRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.UpdateWorkspace: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateWorkspaceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Workspace
    ApiResponse<WorkspaceResponse> response = apiInstance.UpdateWorkspaceWithHttpInfo(workspaceId, workspacePatchRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.UpdateWorkspaceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceId** | **string** |  |  |
| **workspacePatchRequest** | [**WorkspacePatchRequest**](WorkspacePatchRequest.md) |  |  |
| **idempotencyKey** | **string?** |  | [optional]  |

### Return type

[**WorkspaceResponse**](WorkspaceResponse.md)

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

<a id="updateworkspacemember"></a>
# **UpdateWorkspaceMember**
> WorkspaceMemberOut UpdateWorkspaceMember (string workspaceId, string memberId, WorkspaceMemberPatchRequest workspaceMemberPatchRequest)

Update Workspace Member

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UpdateWorkspaceMemberExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new WorkspacesApi(config);
            var workspaceId = "workspaceId_example";  // string | 
            var memberId = "memberId_example";  // string | 
            var workspaceMemberPatchRequest = new WorkspaceMemberPatchRequest(); // WorkspaceMemberPatchRequest | 

            try
            {
                // Update Workspace Member
                WorkspaceMemberOut result = apiInstance.UpdateWorkspaceMember(workspaceId, memberId, workspaceMemberPatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.UpdateWorkspaceMember: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateWorkspaceMemberWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Workspace Member
    ApiResponse<WorkspaceMemberOut> response = apiInstance.UpdateWorkspaceMemberWithHttpInfo(workspaceId, memberId, workspaceMemberPatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.UpdateWorkspaceMemberWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **workspaceId** | **string** |  |  |
| **memberId** | **string** |  |  |
| **workspaceMemberPatchRequest** | [**WorkspaceMemberPatchRequest**](WorkspaceMemberPatchRequest.md) |  |  |

### Return type

[**WorkspaceMemberOut**](WorkspaceMemberOut.md)

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

