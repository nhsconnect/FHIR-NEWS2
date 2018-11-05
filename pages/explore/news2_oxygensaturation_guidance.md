---
title: NEWS2 Oxygen Saturation Guidance
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: news2_oxygensaturation_guidance.html
summary: Guidance for populating the NEWS2 Oxygen Saturation Observation.
toc: false
---

The NEWS2 oxygen saturation observation reading uses the <a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-OxygenSaturation-Observation-1" target="_blank">**CareConnect-OxygenSaturation-Observation-1**</a> profile.

# Guidance for Populating a NEWS2 Oxygen Saturation Observation #

_Note that some elements are "Left uncurated as no use case in NEWS2", and are not needed for NEWS2._

<table>
<tr><th>CareConnect-OxygenSaturation-Observation-1 element</th><th>Population Guidance</th></tr>
<tr><td>identifier</td><td>A unique identifier assigned to this observation (such as a generated universally unique identifier (uuid))</td></tr>
<tr><td>basedOn</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>status</td><td>Fixed to "final"</td></tr>
<tr><td>category</td><td>code is fixed to "vital-signs" <br/>system is fixed to "http://hl7.org/fhir/observation-category"</td></tr>
<tr><td>code</td><td>code MUST contain the <a href="https://www.hl7.org/fhir/observation-vitalsigns.html#vitals-table" target="_blank"><b>Magic Code</b></a> as per the HL7 vital signs guidance, MUST also have a SNOMED CT equivalent Magic Code and MAY have a more refined SNOMED CT concept code<br/><br/>For NEWS2 Oxygen Saturation Magic Code, code is fixed to "59408-5", system is fixed to "http://loinc.org"<br/><br/>For NEWS2 oxygen saturation SNOMED CT Magic Code, code is fixed to "103228002", system is fixed to "http://snomed.info/sct"<br/>For more refined SNOMED CT codes, code is from the valueSet defined <a href="#more-refined-snomed-ct-codes-for-pulse-rate"><b>here</b></a>, system is fixed to "http://snomed.info/sct".<br/><br/>If a more refined SNOMED CT code is used, then the userSelected element for that code MUST be checked. </td></tr>
<tr><td>subject</td><td>A link to the Patient</td></tr>
<tr><td>context</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>effective[x]</td><td>The date and time that the oxygen saturation was taken, using effectiveDateTime.</td></tr>
<tr><td>issued</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>performer</td><td>A link to the performer who carried out this observation. This must be a qualified practitioner and associated organisation.</td></tr>
<tr><td>value[x]</td><td>The actual oxygen saturation reading as a valueQuantity. The unit is fixed to "%" and the system fixed to UCUM "http://unitsofmeasure.org"</td></tr>
<tr><td>dataAbsentReason</td><td>Left uncurated as no use case in NEWS2 (as only observations with values should be sent for NEWS2).</td></tr>
<tr><td>interpretation</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>comment</td><td>Any additional notes or actions that the performer wishes to convey</td></tr>
<tr><td>bodySite</td><td>Left uncurated as no use case in NEWS2. Body site information may be implied by the pre-coordinated SNOMED CT concept used in Observation.code</td></tr>
<tr><td>method</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>device</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>referenceRange</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>related</td><td>A link to any related observations.</td></tr>
<tr><td>component</td><td>None of the component elements are required for NEWS2 Pulse rate Observation</td></tr>
</table>


## More Refined SNOMED CT Codes for Oxygen Saturation ##
<<103228002|Hemoglobin saturation with oxygen (observable entity)| <br/>
MINUS (<<442349007|Venous oxygen saturation (observable entity)| <br/>
OR <<927981000000106|Baseline oxygen saturation at periphery (observable entity)| <br/>
OR <<852651000000100|Maximum peripheral oxygen saturation (observable entity)| <br/>
OR <<852661000000102|Minimum peripheral oxygen saturation (observable entity)| <br/>
OR <<852641000000103|Target peripheral oxygen saturation (observable entity)|)

# Example #

<script src="https://gist.github.com/IOPS-DEV/0ad8d083080ad5fe73a5567923d1e35e.js"></script>
