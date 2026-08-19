# InvoicePDFs.Model.NumberingNextOut
What POST /numbering-sequences/{id}/next allocated.  The number is the point of the call. It used to answer with the sequence row instead, so a caller burned a number and had to reconstruct the string itself from prefix, date pattern and padding — the one thing the endpoint exists to do for them.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Number** | **string** |  | 
**SequenceId** | **string** |  | 
**NextNumber** | **int** | The counter after this allocation | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

