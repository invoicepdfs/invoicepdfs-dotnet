# InvoicePDFs.Model.RecurringInvoiceCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BusinessProfileId** | **string** |  | 
**CustomerId** | **string** |  | 
**Frequency** | **string** | daily, weekly, monthly, quarterly, or yearly | 
**Interval** | **int** | Every N periods | [optional] [default to 1]
**StartDate** | **DateOnly** | Date of the first invoice | 
**EndDate** | **DateOnly** |  | [optional] 
**MaxOccurrences** | **int?** |  | [optional] 
**NumberingSequenceId** | **string** |  | [optional] 
**AutoFinalize** | **bool** | Automatically finalize generated invoices | [optional] [default to false]
**InvoiceTemplate** | [**InvoiceDraftRequest**](InvoiceDraftRequest.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

