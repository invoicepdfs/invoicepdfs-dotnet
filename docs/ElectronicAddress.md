# InvoicePDFs.Model.ElectronicAddress
BT-34 / BT-49 — where a document is routed on Peppol or DBNA.  Both halves are required: an identifier without its scheme cannot be resolved, because the same string means different things in different code lists. This is not the tax id, which identifies a company to a tax authority rather than a mailbox on a network.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Value** | **string** |  | 
**SchemeId** | **string** | EAS code list identifier — 0088 is GLN, 9930 a German VAT number. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

