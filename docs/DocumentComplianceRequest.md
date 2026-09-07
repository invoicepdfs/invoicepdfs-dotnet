# InvoicePDFs.Model.DocumentComplianceRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DocumentType** | **string** |  | [optional] [default to DocumentTypeEnum.Invoice]
**Data** | [**DocumentInvoiceDataInput**](DocumentInvoiceDataInput.md) |  | 
**Profile** | **string** | Which ruleset to hold the document to. Rulesets differ: a document valid under one can be rejected by another, so there is no default. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

