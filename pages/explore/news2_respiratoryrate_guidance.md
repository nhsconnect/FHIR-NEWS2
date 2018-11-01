---
title: NEWS2 Respiratory Rate Guidance
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: news2_respiratoryrate_guidance.html
summary: Guidance for populating the NEWS2 Respiratory Rate Observation.
toc: false
---

The NEWS2 respiratory rate observation reading uses the <a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RespiratoryRate-Observation-1">CareConnect-RespiratoryRate-Observation-1</a> profile.

# Guidance for Populating a NEWS2 Respiratory Rate Observation #

When an Observation element has guidance "Not needed for NEWS2", this means that systems MAY populate the element (if appropriate) in the NEWS2 Observation.

<table>
<tr><th>CareConnect-RespiratoryRate-Observation-1 element</th><th>Population Guidance</th></tr>
<tr><td>identifier</td><td>A unique identifier assigned to this observation (such as a generated universally unique identifier (uuid))</td></tr>
<tr><td>basedOn</td><td>Not needed for NEWS2</td></tr>
<tr><td>status</td><td>Fixed to "final"</td></tr>
<tr><td>category</td><td>code is fixed to "vital-signs", system is fixed to "http://hl7.org/fhir/observation-category"</td></tr>
<tr><td>code</td><td>code MUST contain the <a href="https://www.hl7.org/fhir/observation-vitalsigns.html#vitals-table">Magic Code</a> as per the HL7 vital signs guidance, MUST also have a SNOMED CT equivalent Magic Code and MAY have a more refined SNOMED CT concept code<br/><br/>For NEWS2 Respiratory Rate Magic Code, code is fixed to "9279-1", system is fixed to "http://loinc.org"<br/><br/>For NEWS2 respiratory rate SNOMED CT Magic Code, code is fixed to "86290005", system is fixed to "http://snomed.info/sct"<br/>For more refined SNOMED CT codes, code is from the valueSet defined <a href="#more-refined-snomed-ct-codes-for-pulse-rate">here</a>, system is fixed to "http://snomed.info/sct".<br/><br/>If a more refined SNOMED CT code is used, then the userSelected element for that code MUST be checked. </td></tr>
<tr><td>subject</td><td>A link to the Patient</td></tr>
<tr><td>context</td><td>Not needed for NEWS2</td></tr>
<tr><td>effective[x]</td><td>The date and time that the respiratory rate was taken, using effectiveDateTime.</td></tr>
<tr><td>issued</td><td>Not needed for NEWS2</td></tr>
<tr><td>performer</td><td>A link to the performer who carried out this observation. This must be a qualified practitioner and associated organisation.</td></tr>
<tr><td>value[x]</td><td>The actual respiratory rate reading as a valueQuantity. The unit is fixed to "/min" and the system fixed to UCUM "http://unitsofmeasure.org"</td></tr>
<tr><td>dataAbsentReason</td><td>Not needed for NEWS2 (as only observations with values should be sent for NEWS2).</td></tr>
<tr><td>interpretation</td><td>Not needed for NEWS2</td></tr>
<tr><td>comment</td><td>Any additional notes or actions that the performer wishes to convey</td></tr>
<tr><td>bodySite</td><td>Not needed for NEWS2. Body site information may be implied by the pre-coordinated SNOMED CT concept used in Observation.code</td></tr>
<tr><td>method</td><td>Not needed for NEWS2</td></tr>
<tr><td>device</td><td>Not needed for NEWS2</td></tr>
<tr><td>referenceRange</td><td>Not needed for NEWS2</td></tr>
<tr><td>related</td><td>A link to any related observations.</td></tr>
<tr><td>component</td><td>None of the component elements are required for NEWS2 Pulse rate Observation</td></tr>
</table>


## More Refined SNOMED CT Codes for Respiratory Rate ##
86290005|Respiratory rate (observable entity)| <br/>
MINUS <<927961000000102|Baseline respiratory rate (observable entity)|

# Example #

<script src="https://gist.github.com/IOPS-DEV/a3872d5c96d59c8144a2881655026811.js"></script>