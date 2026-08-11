# InvoicePDFs.Api.AuthApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ExchangeAuthToken**](AuthApi.md#exchangeauthtoken) | **POST** /api/v1/auth/token | Exchange Auth Token |
| [**GetCurrentUser**](AuthApi.md#getcurrentuser) | **GET** /api/v1/auth/me | Get Current User |
| [**Logout**](AuthApi.md#logout) | **POST** /api/v1/auth/logout | Logout |
| [**RefreshAccessToken**](AuthApi.md#refreshaccesstoken) | **POST** /api/v1/auth/refresh | Refresh Access Token |
| [**Register**](AuthApi.md#register) | **POST** /api/v1/auth/register | Register |
| [**RequestPasswordReset**](AuthApi.md#requestpasswordreset) | **POST** /api/v1/auth/forgot-password | Request Password Reset |
| [**ResetPassword**](AuthApi.md#resetpassword) | **POST** /api/v1/auth/reset-password | Reset Password |
| [**UpdateCurrentUser**](AuthApi.md#updatecurrentuser) | **PATCH** /api/v1/auth/me | Update Current User |

<a id="exchangeauthtoken"></a>
# **ExchangeAuthToken**
> AuthTokenResponse ExchangeAuthToken (AuthTokenRequest authTokenRequest)

Exchange Auth Token

Exchange a Firebase ID token for account info.  Use this on login: the client authenticates with Firebase, sends the ID token here, and receives the InvoicePDFs account details. The Firebase token itself is used as the Bearer token for subsequent API calls.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ExchangeAuthTokenExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new AuthApi(config);
            var authTokenRequest = new AuthTokenRequest(); // AuthTokenRequest | 

            try
            {
                // Exchange Auth Token
                AuthTokenResponse result = apiInstance.ExchangeAuthToken(authTokenRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.ExchangeAuthToken: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExchangeAuthTokenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Exchange Auth Token
    ApiResponse<AuthTokenResponse> response = apiInstance.ExchangeAuthTokenWithHttpInfo(authTokenRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.ExchangeAuthTokenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **authTokenRequest** | [**AuthTokenRequest**](AuthTokenRequest.md) |  |  |

### Return type

[**AuthTokenResponse**](AuthTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="getcurrentuser"></a>
# **GetCurrentUser**
> AuthMeResponse GetCurrentUser ()

Get Current User

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class GetCurrentUserExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new AuthApi(config);

            try
            {
                // Get Current User
                AuthMeResponse result = apiInstance.GetCurrentUser();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.GetCurrentUser: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetCurrentUserWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Current User
    ApiResponse<AuthMeResponse> response = apiInstance.GetCurrentUserWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.GetCurrentUserWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**AuthMeResponse**](AuthMeResponse.md)

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

<a id="logout"></a>
# **Logout**
> AuthMessageResponse Logout ()

Logout

Revoke all Firebase refresh tokens for the authenticated user.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class LogoutExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new AuthApi(config);

            try
            {
                // Logout
                AuthMessageResponse result = apiInstance.Logout();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.Logout: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LogoutWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Logout
    ApiResponse<AuthMessageResponse> response = apiInstance.LogoutWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.LogoutWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**AuthMessageResponse**](AuthMessageResponse.md)

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

<a id="refreshaccesstoken"></a>
# **RefreshAccessToken**
> AuthRefreshResponse RefreshAccessToken (AuthRefreshRequest authRefreshRequest)

Refresh Access Token

Exchange a Firebase refresh token for a new ID token.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RefreshAccessTokenExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new AuthApi(config);
            var authRefreshRequest = new AuthRefreshRequest(); // AuthRefreshRequest | 

            try
            {
                // Refresh Access Token
                AuthRefreshResponse result = apiInstance.RefreshAccessToken(authRefreshRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.RefreshAccessToken: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefreshAccessTokenWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Refresh Access Token
    ApiResponse<AuthRefreshResponse> response = apiInstance.RefreshAccessTokenWithHttpInfo(authRefreshRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.RefreshAccessTokenWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **authRefreshRequest** | [**AuthRefreshRequest**](AuthRefreshRequest.md) |  |  |

### Return type

[**AuthRefreshResponse**](AuthRefreshResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="register"></a>
# **Register**
> AuthRegisterResponse Register (AuthRegisterRequest authRegisterRequest)

Register

Register a new account using a Firebase ID token.  The client authenticates with Firebase (email/password, Google, etc.) and sends the resulting ID token here to create an InvoicePDFs account.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RegisterExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new AuthApi(config);
            var authRegisterRequest = new AuthRegisterRequest(); // AuthRegisterRequest | 

            try
            {
                // Register
                AuthRegisterResponse result = apiInstance.Register(authRegisterRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.Register: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RegisterWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Register
    ApiResponse<AuthRegisterResponse> response = apiInstance.RegisterWithHttpInfo(authRegisterRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.RegisterWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **authRegisterRequest** | [**AuthRegisterRequest**](AuthRegisterRequest.md) |  |  |

### Return type

[**AuthRegisterResponse**](AuthRegisterResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="requestpasswordreset"></a>
# **RequestPasswordReset**
> AuthMessageResponse RequestPasswordReset (AuthForgotPasswordRequest authForgotPasswordRequest)

Request Password Reset

Send a password reset email via Firebase.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RequestPasswordResetExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new AuthApi(config);
            var authForgotPasswordRequest = new AuthForgotPasswordRequest(); // AuthForgotPasswordRequest | 

            try
            {
                // Request Password Reset
                AuthMessageResponse result = apiInstance.RequestPasswordReset(authForgotPasswordRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.RequestPasswordReset: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RequestPasswordResetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Request Password Reset
    ApiResponse<AuthMessageResponse> response = apiInstance.RequestPasswordResetWithHttpInfo(authForgotPasswordRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.RequestPasswordResetWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **authForgotPasswordRequest** | [**AuthForgotPasswordRequest**](AuthForgotPasswordRequest.md) |  |  |

### Return type

[**AuthMessageResponse**](AuthMessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="resetpassword"></a>
# **ResetPassword**
> AuthMessageResponse ResetPassword (AuthResetPasswordRequest authResetPasswordRequest)

Reset Password

Confirm a password reset using the code from the reset email.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ResetPasswordExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new AuthApi(config);
            var authResetPasswordRequest = new AuthResetPasswordRequest(); // AuthResetPasswordRequest | 

            try
            {
                // Reset Password
                AuthMessageResponse result = apiInstance.ResetPassword(authResetPasswordRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.ResetPassword: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResetPasswordWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reset Password
    ApiResponse<AuthMessageResponse> response = apiInstance.ResetPasswordWithHttpInfo(authResetPasswordRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.ResetPasswordWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **authResetPasswordRequest** | [**AuthResetPasswordRequest**](AuthResetPasswordRequest.md) |  |  |

### Return type

[**AuthMessageResponse**](AuthMessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="updatecurrentuser"></a>
# **UpdateCurrentUser**
> AuthMeResponse UpdateCurrentUser (AuthMePatchRequest authMePatchRequest)

Update Current User

Update the authenticated account's name or email.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class UpdateCurrentUserExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new AuthApi(config);
            var authMePatchRequest = new AuthMePatchRequest(); // AuthMePatchRequest | 

            try
            {
                // Update Current User
                AuthMeResponse result = apiInstance.UpdateCurrentUser(authMePatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.UpdateCurrentUser: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateCurrentUserWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Current User
    ApiResponse<AuthMeResponse> response = apiInstance.UpdateCurrentUserWithHttpInfo(authMePatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.UpdateCurrentUserWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **authMePatchRequest** | [**AuthMePatchRequest**](AuthMePatchRequest.md) |  |  |

### Return type

[**AuthMeResponse**](AuthMeResponse.md)

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

