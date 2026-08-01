# InvoicePDFs.Model.StandardLineItemInput
A fully priced line: unit, price, tax, discount and SKU.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Description** | **string** |  | [optional] 
**Quantity** | **string** | Decimal string | 
**UnitPrice** | **string** | Decimal string, major units | [optional] [default to "0.00"]
**Unit** | **string** |  | [optional] 
**Sku** | **string** |  | [optional] 
**Discount** | [**LineItemDiscountInput**](LineItemDiscountInput.md) |  | [optional] 
**Taxes** | [**List&lt;LineItemTaxInput&gt;**](LineItemTaxInput.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

