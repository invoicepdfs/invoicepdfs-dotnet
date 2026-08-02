# InvoicePDFs.Model.DocumentCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DocumentType** | **string** |  | [optional] [default to DocumentTypeEnum.Invoice]
**Number** | **string** |  | 
**IssueDate** | **DateOnly** |  | 
**DueDate** | **DateOnly** |  | [optional] 
**Currency** | **string** |  | 
**Locale** | **string** |  | [optional] 
**BusinessProfileId** | **string** |  | 
**CustomerId** | **string** |  | 
**SourceDocumentId** | **string** |  | [optional] 
**Reason** | **string** |  | [optional] 
**ShipTo** | [**PostalAddress**](PostalAddress.md) |  | [optional] 
**LineItems** | [**List&lt;StandardLineItemInput&gt;**](StandardLineItemInput.md) |  | 
**Discounts** | [**List&lt;LineItemDiscountInput&gt;**](LineItemDiscountInput.md) |  | [optional] 
**Shipping** | [**InvoiceShippingInput**](InvoiceShippingInput.md) |  | [optional] 
**Notes** | [**List&lt;InvoiceNoteInput&gt;**](InvoiceNoteInput.md) |  | [optional] 
**Terms** | [**List&lt;InvoiceTermInput&gt;**](InvoiceTermInput.md) |  | [optional] 
**CustomFields** | [**List&lt;InvoiceCustomFieldInput&gt;**](InvoiceCustomFieldInput.md) |  | [optional] 
**Payment** | [**InvoicePaymentInput**](InvoicePaymentInput.md) |  | [optional] 
**Branding** | [**InvoiceBrandingInput**](InvoiceBrandingInput.md) |  | [optional] 
**BrandingProfileId** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

