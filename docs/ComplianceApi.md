# InvoicePDFs.Api.ComplianceApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DownloadDocumentXml**](ComplianceApi.md#downloaddocumentxml) | **GET** /api/v1/documents/{document_id}/xml | Download Document Xml |
| [**RenderDocumentXml**](ComplianceApi.md#renderdocumentxml) | **POST** /api/v1/documents/xml | Render Document Xml |
| [**ValidateCompliance**](ComplianceApi.md#validatecompliance) | **POST** /api/v1/documents/validate-compliance | Validate Compliance |

<a id="downloaddocumentxml"></a>
# **DownloadDocumentXml**
> string DownloadDocumentXml (string documentId, string profile)

Download Document Xml

The e-invoicing XML for a document already stored here.  Reads `data_json` directly rather than going through the render path's reconstruction: the status, the logo and the source document's number are all attached there for the *PDF*, and none of them belong in the XML. The credit note's BG-3 reference is already in the stored payload, resolved when the document was written.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class DownloadDocumentXmlExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ComplianceApi(config);
            var documentId = "documentId_example";  // string | 
            var profile = peppol_bis_billing_3;  // string | Which ruleset to write this against. No default: a document valid under one can be rejected by another, so the choice is the request.

            try
            {
                // Download Document Xml
                string result = apiInstance.DownloadDocumentXml(documentId, profile);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ComplianceApi.DownloadDocumentXml: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DownloadDocumentXmlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Download Document Xml
    ApiResponse<string> response = apiInstance.DownloadDocumentXmlWithHttpInfo(documentId, profile);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ComplianceApi.DownloadDocumentXmlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentId** | **string** |  |  |
| **profile** | **string** | Which ruleset to write this against. No default: a document valid under one can be rejected by another, so the choice is the request. |  |

### Return type

**string**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The stored document as XML, in the syntax the chosen profile is expressed in — UBL for Peppol BIS, CII for Factur-X. |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="renderdocumentxml"></a>
# **RenderDocumentXml**
> string RenderDocumentXml (DocumentComplianceRequest documentComplianceRequest)

Render Document Xml

The e-invoicing XML for a document, without storing anything.  Takes the same body as `/validate-compliance`, and the pairing is the point: check first, then take the XML once it passes. Nothing here validates against the ruleset — a document missing mandatory fields serialises to XML missing those elements, which is a more useful artefact to look at than a refusal, and `/validate-compliance` is where the refusal belongs.  The syntax is not a parameter. It follows from the profile, because a profile already is a syntax plus a ruleset, and asking a caller for both is asking them to know that Peppol means UBL.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class RenderDocumentXmlExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ComplianceApi(config);
            var documentComplianceRequest = new DocumentComplianceRequest(); // DocumentComplianceRequest | 

            try
            {
                // Render Document Xml
                string result = apiInstance.RenderDocumentXml(documentComplianceRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ComplianceApi.RenderDocumentXml: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RenderDocumentXmlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Render Document Xml
    ApiResponse<string> response = apiInstance.RenderDocumentXmlWithHttpInfo(documentComplianceRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ComplianceApi.RenderDocumentXmlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentComplianceRequest** | [**DocumentComplianceRequest**](DocumentComplianceRequest.md) |  |  |

### Return type

**string**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/xml, application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The document as XML, in the syntax the chosen profile is expressed in — UBL for Peppol BIS, CII for Factur-X. |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="validatecompliance"></a>
# **ValidateCompliance**
> DocumentComplianceResponse ValidateCompliance (DocumentComplianceRequest documentComplianceRequest)

Validate Compliance

Check a document against an e-invoicing ruleset without rendering it.  Costs no renders: nothing is stored and no PDF is produced, so a caller can check every invoice they are about to send rather than discovering the problem from a rejection weeks later.  Two tiers run, and both are reported. The mandatory-field check names a field of the request you can go and change. Schematron then serializes the document and runs the **published rules at a pinned version** over the result — the same artefacts an access point runs — so a finding here quotes the rule id a rejection notice would quote.  Read `valid` together with `fully_checked`: `valid` says nothing fatal was found, and `rulesets` says what actually ran to find it.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using InvoicePDFs.Api;
using InvoicePDFs.Client;
using InvoicePDFs.Model;

namespace Example
{
    public class ValidateComplianceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "http://localhost";
            // Configure Bearer token for authorization: HTTPBearer
            config.AccessToken = "YOUR_BEARER_TOKEN";

            var apiInstance = new ComplianceApi(config);
            var documentComplianceRequest = new DocumentComplianceRequest(); // DocumentComplianceRequest | 

            try
            {
                // Validate Compliance
                DocumentComplianceResponse result = apiInstance.ValidateCompliance(documentComplianceRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ComplianceApi.ValidateCompliance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ValidateComplianceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Validate Compliance
    ApiResponse<DocumentComplianceResponse> response = apiInstance.ValidateComplianceWithHttpInfo(documentComplianceRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ComplianceApi.ValidateComplianceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **documentComplianceRequest** | [**DocumentComplianceRequest**](DocumentComplianceRequest.md) |  |  |

### Return type

[**DocumentComplianceResponse**](DocumentComplianceResponse.md)

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

