# InvoicePDFs.Model.ComplianceCheckOut

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Profile** | **string** |  | 
**RulesetVersion** | **string** | The version these rules came from. Worth recording alongside any document you file — rulesets revise, and &#39;which rules did this pass?&#39; is what an audit asks years later. | 
**Valid** | **bool** |  | 
**Violations** | [**List&lt;ComplianceViolationOut&gt;**](ComplianceViolationOut.md) | Every violation found, not the first — fixing one field per round trip is the experience this avoids. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

