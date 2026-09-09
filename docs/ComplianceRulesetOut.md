# InvoicePDFs.Model.ComplianceRulesetOut
One ruleset the document was held to, and whether it actually ran.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Label** | **string** |  | 
**VarVersion** | **string** | The upstream release of the rules. Empty for checks with no version of their own. | [optional] [default to ""]
**Ran** | **bool** | False when this ruleset could not be run at all. A ruleset that did not run is not a pass — &#x60;valid&#x60; only reports what was checked. | 
**Reason** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

