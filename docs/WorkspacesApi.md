# InvoicePDFs.Api.WorkspacesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateMemberApiV1WorkspacesWorkspaceIdMembersPost**](WorkspacesApi.md#creatememberapiv1workspacesworkspaceidmemberspost) | **POST** /api/v1/workspaces/{workspace_id}/members | Create Member |
| [**CreateWorkspaceApiV1WorkspacesPost**](WorkspacesApi.md#createworkspaceapiv1workspacespost) | **POST** /api/v1/workspaces | Create Workspace |
| [**DeleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete**](WorkspacesApi.md#deletememberapiv1workspacesworkspaceidmembersmemberiddelete) | **DELETE** /api/v1/workspaces/{workspace_id}/members/{member_id} | Delete Member |
| [**DeleteWorkspaceApiV1WorkspacesWorkspaceIdDelete**](WorkspacesApi.md#deleteworkspaceapiv1workspacesworkspaceiddelete) | **DELETE** /api/v1/workspaces/{workspace_id} | Delete Workspace |
| [**GetWorkspaceApiV1WorkspacesWorkspaceIdGet**](WorkspacesApi.md#getworkspaceapiv1workspacesworkspaceidget) | **GET** /api/v1/workspaces/{workspace_id} | Get Workspace |
| [**ListMembersApiV1WorkspacesWorkspaceIdMembersGet**](WorkspacesApi.md#listmembersapiv1workspacesworkspaceidmembersget) | **GET** /api/v1/workspaces/{workspace_id}/members | List Members |
| [**ListWorkspacesApiV1WorkspacesGet**](WorkspacesApi.md#listworkspacesapiv1workspacesget) | **GET** /api/v1/workspaces | List Workspaces |
| [**PatchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch**](WorkspacesApi.md#patchmemberapiv1workspacesworkspaceidmembersmemberidpatch) | **PATCH** /api/v1/workspaces/{workspace_id}/members/{member_id} | Patch Member |
| [**PatchWorkspaceApiV1WorkspacesWorkspaceIdPatch**](WorkspacesApi.md#patchworkspaceapiv1workspacesworkspaceidpatch) | **PATCH** /api/v1/workspaces/{workspace_id} | Patch Workspace |

<a id="creatememberapiv1workspacesworkspaceidmemberspost"></a>
# **CreateMemberApiV1WorkspacesWorkspaceIdMembersPost**
> WorkspaceMembersListResponse CreateMemberApiV1WorkspacesWorkspaceIdMembersPost (string workspaceId, WorkspaceMemberCreateRequest workspaceMemberCreateRequest, string? idempotencyKey = null)

Create Member

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class CreateMemberApiV1WorkspacesWorkspaceIdMembersPostExample
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
                // Create Member
                WorkspaceMembersListResponse result = apiInstance.CreateMemberApiV1WorkspacesWorkspaceIdMembersPost(workspaceId, workspaceMemberCreateRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.CreateMemberApiV1WorkspacesWorkspaceIdMembersPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateMemberApiV1WorkspacesWorkspaceIdMembersPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Member
    ApiResponse<WorkspaceMembersListResponse> response = apiInstance.CreateMemberApiV1WorkspacesWorkspaceIdMembersPostWithHttpInfo(workspaceId, workspaceMemberCreateRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.CreateMemberApiV1WorkspacesWorkspaceIdMembersPostWithHttpInfo: " + e.Message);
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

<a id="createworkspaceapiv1workspacespost"></a>
# **CreateWorkspaceApiV1WorkspacesPost**
> WorkspaceResponse CreateWorkspaceApiV1WorkspacesPost (WorkspaceCreateRequest workspaceCreateRequest, string? idempotencyKey = null)

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
    public class CreateWorkspaceApiV1WorkspacesPostExample
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
                WorkspaceResponse result = apiInstance.CreateWorkspaceApiV1WorkspacesPost(workspaceCreateRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.CreateWorkspaceApiV1WorkspacesPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateWorkspaceApiV1WorkspacesPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create Workspace
    ApiResponse<WorkspaceResponse> response = apiInstance.CreateWorkspaceApiV1WorkspacesPostWithHttpInfo(workspaceCreateRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.CreateWorkspaceApiV1WorkspacesPostWithHttpInfo: " + e.Message);
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

<a id="deletememberapiv1workspacesworkspaceidmembersmemberiddelete"></a>
# **DeleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete**
> SimpleBoolResponse DeleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete (string workspaceId, string memberId)

Delete Member

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DeleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDeleteExample
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
                // Delete Member
                SimpleBoolResponse result = apiInstance.DeleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete(workspaceId, memberId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.DeleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Member
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDeleteWithHttpInfo(workspaceId, memberId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.DeleteMemberApiV1WorkspacesWorkspaceIdMembersMemberIdDeleteWithHttpInfo: " + e.Message);
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

<a id="deleteworkspaceapiv1workspacesworkspaceiddelete"></a>
# **DeleteWorkspaceApiV1WorkspacesWorkspaceIdDelete**
> SimpleBoolResponse DeleteWorkspaceApiV1WorkspacesWorkspaceIdDelete (string workspaceId)

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
    public class DeleteWorkspaceApiV1WorkspacesWorkspaceIdDeleteExample
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
                SimpleBoolResponse result = apiInstance.DeleteWorkspaceApiV1WorkspacesWorkspaceIdDelete(workspaceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.DeleteWorkspaceApiV1WorkspacesWorkspaceIdDelete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteWorkspaceApiV1WorkspacesWorkspaceIdDeleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete Workspace
    ApiResponse<SimpleBoolResponse> response = apiInstance.DeleteWorkspaceApiV1WorkspacesWorkspaceIdDeleteWithHttpInfo(workspaceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.DeleteWorkspaceApiV1WorkspacesWorkspaceIdDeleteWithHttpInfo: " + e.Message);
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

<a id="getworkspaceapiv1workspacesworkspaceidget"></a>
# **GetWorkspaceApiV1WorkspacesWorkspaceIdGet**
> WorkspaceResponse GetWorkspaceApiV1WorkspacesWorkspaceIdGet (string workspaceId)

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
    public class GetWorkspaceApiV1WorkspacesWorkspaceIdGetExample
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
                WorkspaceResponse result = apiInstance.GetWorkspaceApiV1WorkspacesWorkspaceIdGet(workspaceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.GetWorkspaceApiV1WorkspacesWorkspaceIdGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWorkspaceApiV1WorkspacesWorkspaceIdGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Workspace
    ApiResponse<WorkspaceResponse> response = apiInstance.GetWorkspaceApiV1WorkspacesWorkspaceIdGetWithHttpInfo(workspaceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.GetWorkspaceApiV1WorkspacesWorkspaceIdGetWithHttpInfo: " + e.Message);
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

<a id="listmembersapiv1workspacesworkspaceidmembersget"></a>
# **ListMembersApiV1WorkspacesWorkspaceIdMembersGet**
> WorkspaceMembersListResponse ListMembersApiV1WorkspacesWorkspaceIdMembersGet (string workspaceId)

List Members

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ListMembersApiV1WorkspacesWorkspaceIdMembersGetExample
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
                // List Members
                WorkspaceMembersListResponse result = apiInstance.ListMembersApiV1WorkspacesWorkspaceIdMembersGet(workspaceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.ListMembersApiV1WorkspacesWorkspaceIdMembersGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListMembersApiV1WorkspacesWorkspaceIdMembersGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Members
    ApiResponse<WorkspaceMembersListResponse> response = apiInstance.ListMembersApiV1WorkspacesWorkspaceIdMembersGetWithHttpInfo(workspaceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.ListMembersApiV1WorkspacesWorkspaceIdMembersGetWithHttpInfo: " + e.Message);
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

<a id="listworkspacesapiv1workspacesget"></a>
# **ListWorkspacesApiV1WorkspacesGet**
> WorkspacesListResponse ListWorkspacesApiV1WorkspacesGet (int? limit = null, string? cursor = null)

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
    public class ListWorkspacesApiV1WorkspacesGetExample
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
                WorkspacesListResponse result = apiInstance.ListWorkspacesApiV1WorkspacesGet(limit, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.ListWorkspacesApiV1WorkspacesGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ListWorkspacesApiV1WorkspacesGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Workspaces
    ApiResponse<WorkspacesListResponse> response = apiInstance.ListWorkspacesApiV1WorkspacesGetWithHttpInfo(limit, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.ListWorkspacesApiV1WorkspacesGetWithHttpInfo: " + e.Message);
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

<a id="patchmemberapiv1workspacesworkspaceidmembersmemberidpatch"></a>
# **PatchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch**
> WorkspaceMemberOut PatchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch (string workspaceId, string memberId, WorkspaceMemberPatchRequest workspaceMemberPatchRequest)

Patch Member

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PatchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatchExample
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
                // Patch Member
                WorkspaceMemberOut result = apiInstance.PatchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch(workspaceId, memberId, workspaceMemberPatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.PatchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PatchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Patch Member
    ApiResponse<WorkspaceMemberOut> response = apiInstance.PatchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatchWithHttpInfo(workspaceId, memberId, workspaceMemberPatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.PatchMemberApiV1WorkspacesWorkspaceIdMembersMemberIdPatchWithHttpInfo: " + e.Message);
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

<a id="patchworkspaceapiv1workspacesworkspaceidpatch"></a>
# **PatchWorkspaceApiV1WorkspacesWorkspaceIdPatch**
> WorkspaceResponse PatchWorkspaceApiV1WorkspacesWorkspaceIdPatch (string workspaceId, WorkspacePatchRequest workspacePatchRequest, string? idempotencyKey = null)

Patch Workspace

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class PatchWorkspaceApiV1WorkspacesWorkspaceIdPatchExample
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
                // Patch Workspace
                WorkspaceResponse result = apiInstance.PatchWorkspaceApiV1WorkspacesWorkspaceIdPatch(workspaceId, workspacePatchRequest, idempotencyKey);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WorkspacesApi.PatchWorkspaceApiV1WorkspacesWorkspaceIdPatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PatchWorkspaceApiV1WorkspacesWorkspaceIdPatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Patch Workspace
    ApiResponse<WorkspaceResponse> response = apiInstance.PatchWorkspaceApiV1WorkspacesWorkspaceIdPatchWithHttpInfo(workspaceId, workspacePatchRequest, idempotencyKey);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WorkspacesApi.PatchWorkspaceApiV1WorkspacesWorkspaceIdPatchWithHttpInfo: " + e.Message);
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

