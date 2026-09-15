# InvoicePDFs.Model.RenderComplianceOut
What this PDF was held to, for a render that carries embedded XML.  Absent on a plain `pdf`: no ruleset was applied, so there is no claim to report. A render that was produced at all satisfied every fatal rule that ran — the render is refused otherwise — so the useful questions are which rules those were, and whether all of them ran.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Profile** | **string** | The ruleset this document was built and validated against. | 
**RulesetVersion** | **string** | The artefact versions the check actually ran. A profile is held to more than one ruleset, and they are regenerated over time, so this is what makes &#39;which rules did this pass?&#39; answerable later. | 
**FullyChecked** | **bool** | False when a ruleset could not run. The document still satisfied everything that did, but the authoritative Schematron tier being absent is a materially weaker statement than it passing. | 
**Advisories** | [**List&lt;ComplianceViolationOut&gt;**](ComplianceViolationOut.md) | Non-fatal findings the render proceeded past. Both rulesets grade a large share of their rules as advisory, so these are worth reading and are not a rejection. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

