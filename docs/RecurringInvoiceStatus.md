# InvoicePDFs.Model.RecurringInvoiceStatus
`completed` is the schedule running out, not a failure — set by app/recurring/processor.py when the end date or occurrence count is reached. `RecurringInvoiceOut.status` was an unconstrained `str`, so this is the first time the set has been written down anywhere.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

