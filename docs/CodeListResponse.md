# InvoicePDFs.Model.CodeListResponse
A coded list from a standard, and whether it is the whole of one.  `exhaustive` is the field that changes what a client does. `true` means a value outside `data` is wrong, so the list can back a picker with no escape hatch. `false` means `data` is a shortlist of the codes an invoice usually needs — the API accepts any code, nothing validates against this, and treating it as closed rejects values that are perfectly valid.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Data** | [**List&lt;CodeOut&gt;**](CodeOut.md) |  | 
**Standard** | **string** | The code list these values come from. | 
**Exhaustive** | **bool** | Whether &#x60;data&#x60; is the complete list. When false it is a shortlist and other codes remain valid. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

