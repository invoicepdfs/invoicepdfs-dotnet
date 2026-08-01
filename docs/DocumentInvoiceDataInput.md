# InvoicePDFs.Model.DocumentInvoiceDataInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**InvoiceNumber** | **string** |  | 
**IssueDate** | **DateOnly** |  | 
**DueDate** | **DateOnly** |  | [optional] 
**Currency** | **string** |  | 
**Seller** | [**DocumentPartyInput**](DocumentPartyInput.md) |  | 
**Buyer** | [**DocumentPartyInput**](DocumentPartyInput.md) |  | 
**ShipTo** | [**DocumentPartyInput**](DocumentPartyInput.md) |  | [optional] 
**LineItems** | [**List&lt;DocumentLineItemInput&gt;**](DocumentLineItemInput.md) |  | 
**Discounts** | [**List&lt;DocumentDiscountInput&gt;**](DocumentDiscountInput.md) |  | [optional] 
**Shipping** | [**DocumentShippingInput**](DocumentShippingInput.md) |  | [optional] 
**CustomFields** | [**List&lt;DocumentCustomFieldInput&gt;**](DocumentCustomFieldInput.md) |  | [optional] 
**Payment** | [**DocumentPaymentInput**](DocumentPaymentInput.md) |  | [optional] 
**Branding** | [**DocumentBrandingInput**](DocumentBrandingInput.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

