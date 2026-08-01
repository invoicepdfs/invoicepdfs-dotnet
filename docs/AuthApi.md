# InvoicePDFs.Api.AuthApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ForgotPasswordApiV1AuthForgotPasswordPost**](AuthApi.md#forgotpasswordapiv1authforgotpasswordpost) | **POST** /api/v1/auth/forgot-password | Forgot Password |
| [**LogoutApiV1AuthLogoutPost**](AuthApi.md#logoutapiv1authlogoutpost) | **POST** /api/v1/auth/logout | Logout |
| [**MeApiV1AuthMeGet**](AuthApi.md#meapiv1authmeget) | **GET** /api/v1/auth/me | Me |
| [**PatchMeApiV1AuthMePatch**](AuthApi.md#patchmeapiv1authmepatch) | **PATCH** /api/v1/auth/me | Patch Me |
| [**RefreshApiV1AuthRefreshPost**](AuthApi.md#refreshapiv1authrefreshpost) | **POST** /api/v1/auth/refresh | Refresh |
| [**RegisterApiV1AuthRegisterPost**](AuthApi.md#registerapiv1authregisterpost) | **POST** /api/v1/auth/register | Register |
| [**ResetPasswordApiV1AuthResetPasswordPost**](AuthApi.md#resetpasswordapiv1authresetpasswordpost) | **POST** /api/v1/auth/reset-password | Reset Password |
| [**TokenExchangeApiV1AuthTokenPost**](AuthApi.md#tokenexchangeapiv1authtokenpost) | **POST** /api/v1/auth/token | Token Exchange |

<a id="forgotpasswordapiv1authforgotpasswordpost"></a>
# **ForgotPasswordApiV1AuthForgotPasswordPost**
> AuthMessageResponse ForgotPasswordApiV1AuthForgotPasswordPost (AuthForgotPasswordRequest authForgotPasswordRequest)

Forgot Password

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
    public class ForgotPasswordApiV1AuthForgotPasswordPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new AuthApi(config);
            var authForgotPasswordRequest = new AuthForgotPasswordRequest(); // AuthForgotPasswordRequest | 

            try
            {
                // Forgot Password
                AuthMessageResponse result = apiInstance.ForgotPasswordApiV1AuthForgotPasswordPost(authForgotPasswordRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.ForgotPasswordApiV1AuthForgotPasswordPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ForgotPasswordApiV1AuthForgotPasswordPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Forgot Password
    ApiResponse<AuthMessageResponse> response = apiInstance.ForgotPasswordApiV1AuthForgotPasswordPostWithHttpInfo(authForgotPasswordRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.ForgotPasswordApiV1AuthForgotPasswordPostWithHttpInfo: " + e.Message);
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

<a id="logoutapiv1authlogoutpost"></a>
# **LogoutApiV1AuthLogoutPost**
> AuthMessageResponse LogoutApiV1AuthLogoutPost ()

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
    public class LogoutApiV1AuthLogoutPostExample
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
                AuthMessageResponse result = apiInstance.LogoutApiV1AuthLogoutPost();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.LogoutApiV1AuthLogoutPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LogoutApiV1AuthLogoutPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Logout
    ApiResponse<AuthMessageResponse> response = apiInstance.LogoutApiV1AuthLogoutPostWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.LogoutApiV1AuthLogoutPostWithHttpInfo: " + e.Message);
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

<a id="meapiv1authmeget"></a>
# **MeApiV1AuthMeGet**
> AuthMeResponse MeApiV1AuthMeGet ()

Me

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class MeApiV1AuthMeGetExample
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
                // Me
                AuthMeResponse result = apiInstance.MeApiV1AuthMeGet();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.MeApiV1AuthMeGet: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the MeApiV1AuthMeGetWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Me
    ApiResponse<AuthMeResponse> response = apiInstance.MeApiV1AuthMeGetWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.MeApiV1AuthMeGetWithHttpInfo: " + e.Message);
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

<a id="patchmeapiv1authmepatch"></a>
# **PatchMeApiV1AuthMePatch**
> AuthMeResponse PatchMeApiV1AuthMePatch (AuthMePatchRequest authMePatchRequest)

Patch Me

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
    public class PatchMeApiV1AuthMePatchExample
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
                // Patch Me
                AuthMeResponse result = apiInstance.PatchMeApiV1AuthMePatch(authMePatchRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.PatchMeApiV1AuthMePatch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PatchMeApiV1AuthMePatchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Patch Me
    ApiResponse<AuthMeResponse> response = apiInstance.PatchMeApiV1AuthMePatchWithHttpInfo(authMePatchRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.PatchMeApiV1AuthMePatchWithHttpInfo: " + e.Message);
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

<a id="refreshapiv1authrefreshpost"></a>
# **RefreshApiV1AuthRefreshPost**
> AuthRefreshResponse RefreshApiV1AuthRefreshPost (AuthRefreshRequest authRefreshRequest)

Refresh

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
    public class RefreshApiV1AuthRefreshPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new AuthApi(config);
            var authRefreshRequest = new AuthRefreshRequest(); // AuthRefreshRequest | 

            try
            {
                // Refresh
                AuthRefreshResponse result = apiInstance.RefreshApiV1AuthRefreshPost(authRefreshRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.RefreshApiV1AuthRefreshPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RefreshApiV1AuthRefreshPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Refresh
    ApiResponse<AuthRefreshResponse> response = apiInstance.RefreshApiV1AuthRefreshPostWithHttpInfo(authRefreshRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.RefreshApiV1AuthRefreshPostWithHttpInfo: " + e.Message);
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

<a id="registerapiv1authregisterpost"></a>
# **RegisterApiV1AuthRegisterPost**
> AuthRegisterResponse RegisterApiV1AuthRegisterPost (AuthRegisterRequest authRegisterRequest)

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
    public class RegisterApiV1AuthRegisterPostExample
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
                AuthRegisterResponse result = apiInstance.RegisterApiV1AuthRegisterPost(authRegisterRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.RegisterApiV1AuthRegisterPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RegisterApiV1AuthRegisterPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Register
    ApiResponse<AuthRegisterResponse> response = apiInstance.RegisterApiV1AuthRegisterPostWithHttpInfo(authRegisterRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.RegisterApiV1AuthRegisterPostWithHttpInfo: " + e.Message);
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

<a id="resetpasswordapiv1authresetpasswordpost"></a>
# **ResetPasswordApiV1AuthResetPasswordPost**
> AuthMessageResponse ResetPasswordApiV1AuthResetPasswordPost (AuthResetPasswordRequest authResetPasswordRequest)

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
    public class ResetPasswordApiV1AuthResetPasswordPostExample
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
                AuthMessageResponse result = apiInstance.ResetPasswordApiV1AuthResetPasswordPost(authResetPasswordRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.ResetPasswordApiV1AuthResetPasswordPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResetPasswordApiV1AuthResetPasswordPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reset Password
    ApiResponse<AuthMessageResponse> response = apiInstance.ResetPasswordApiV1AuthResetPasswordPostWithHttpInfo(authResetPasswordRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.ResetPasswordApiV1AuthResetPasswordPostWithHttpInfo: " + e.Message);
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

<a id="tokenexchangeapiv1authtokenpost"></a>
# **TokenExchangeApiV1AuthTokenPost**
> AuthTokenResponse TokenExchangeApiV1AuthTokenPost (AuthTokenRequest authTokenRequest)

Token Exchange

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
    public class TokenExchangeApiV1AuthTokenPostExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            var apiInstance = new AuthApi(config);
            var authTokenRequest = new AuthTokenRequest(); // AuthTokenRequest | 

            try
            {
                // Token Exchange
                AuthTokenResponse result = apiInstance.TokenExchangeApiV1AuthTokenPost(authTokenRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AuthApi.TokenExchangeApiV1AuthTokenPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TokenExchangeApiV1AuthTokenPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Token Exchange
    ApiResponse<AuthTokenResponse> response = apiInstance.TokenExchangeApiV1AuthTokenPostWithHttpInfo(authTokenRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AuthApi.TokenExchangeApiV1AuthTokenPostWithHttpInfo: " + e.Message);
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

