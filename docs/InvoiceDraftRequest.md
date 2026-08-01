# InvoicePDFs.Model.InvoiceDraftRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**InvoiceNumber** | **string** |  | 
**DocumentType** | **string** |  | [optional] [default to DocumentTypeEnum.Invoice]
**IssueDate** | **DateOnly** |  | 
**DueDate** | **DateOnly** |  | [optional] 
**Currency** | **string** |  | 
**Locale** | **string** |  | [optional] 
**BusinessProfileId** | **string** |  | 
**CustomerId** | **string** |  | 
**ShipTo** | [**PostalAddress**](PostalAddress.md) |  | [optional] 
**LineItems** | [**List&lt;InvoiceLineItemInput&gt;**](InvoiceLineItemInput.md) |  | 
**Discounts** | [**List&lt;InvoiceDiscountInput&gt;**](InvoiceDiscountInput.md) |  | [optional] 
**Shipping** | [**InvoiceShippingInput**](InvoiceShippingInput.md) |  | [optional] 
**Notes** | [**List&lt;InvoiceNoteInput&gt;**](InvoiceNoteInput.md) |  | [optional] 
**Terms** | [**List&lt;InvoiceTermInput&gt;**](InvoiceTermInput.md) |  | [optional] 
**CustomFields** | [**List&lt;InvoiceCustomFieldInput&gt;**](InvoiceCustomFieldInput.md) |  | [optional] 
**Payment** | [**InvoicePaymentInput**](InvoicePaymentInput.md) |  | [optional] 
**Branding** | [**InvoiceBrandingInput**](InvoiceBrandingInput.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

