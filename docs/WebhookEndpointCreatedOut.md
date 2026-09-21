# InvoicePDFs.Model.WebhookEndpointCreatedOut
A newly created endpoint, including its signing secret.  The only time the secret is returned. Store it now: reading or listing endpoints never includes it, and the only way to obtain another is to rotate, which invalidates this one.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Url** | **string** |  | 
**Description** | **string** |  | [optional] 
**Events** | **List&lt;string&gt;** |  | 
**IsActive** | **bool** |  | 
**CreatedAt** | **string** |  | 
**UpdatedAt** | **string** |  | 
**Secret** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

