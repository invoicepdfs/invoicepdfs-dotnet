# InvoicePDFs.Model.ImportStatus
Three, not the five that were published. `confirm_import` does the work inside the request — \"For MVP, mark as completed immediately; future: background processing\" (app/api/v1/imports.py) — so nothing is ever `processing`, and nothing sets `failed`. They described a background path that was never built, the same way `render.*` events and `bounced` did.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

