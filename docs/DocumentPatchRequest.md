# InvoicePDFs.Model.DocumentPatchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Number** | **string** |  | [optional] 
**DocumentType** | **string** |  | [optional] 
**IssueDate** | **DateOnly** |  | [optional] 
**DueDate** | **DateOnly** |  | [optional] 
**Currency** | **string** |  | [optional] 
**Locale** | **string** |  | [optional] 
**BusinessProfileId** | **string** |  | [optional] 
**CustomerId** | **string** |  | [optional] 
**SourceDocumentId** | **string** |  | [optional] 
**Reason** | **string** |  | [optional] 
**ShipTo** | [**PostalAddress**](PostalAddress.md) |  | [optional] 
**LineItems** | [**List&lt;StandardLineItemInput&gt;**](StandardLineItemInput.md) |  | [optional] 
**Discounts** | [**List&lt;LineItemDiscountInput&gt;**](LineItemDiscountInput.md) |  | [optional] 
**Shipping** | [**InvoiceShippingInput**](InvoiceShippingInput.md) |  | [optional] 
**Notes** | [**List&lt;InvoiceNoteInput&gt;**](InvoiceNoteInput.md) |  | [optional] 
**Terms** | [**List&lt;InvoiceTermInput&gt;**](InvoiceTermInput.md) |  | [optional] 
**CustomFields** | [**List&lt;InvoiceCustomFieldInput&gt;**](InvoiceCustomFieldInput.md) |  | [optional] 
**Payment** | [**InvoicePaymentInput**](InvoicePaymentInput.md) |  | [optional] 
**Branding** | [**InvoiceBrandingInput**](InvoiceBrandingInput.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

