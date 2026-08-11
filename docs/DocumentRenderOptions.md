# InvoicePDFs.Model.DocumentRenderOptions
Render options for an already-stored document (``POST /documents/{id}/renders``).  Distinct from ``app.schemas.v1.DocumentRenderRequest``, which carries a full inline document for the stateless ``POST /documents/render``. Two classes sharing one name made FastAPI fall back to module-qualified schema names in the spec (``app__documents__schemas__DocumentRenderRequest``), which the SDK generators turned into ``AppDocumentsSchemasDocumentRenderRequest``.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TemplateId** | **string** |  | [optional] [default to "tpl_modern"]
**PageSize** | **string** |  | [optional] [default to "LETTER"]
**ExpiresIn** | **int** |  | [optional] [default to 3600]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

