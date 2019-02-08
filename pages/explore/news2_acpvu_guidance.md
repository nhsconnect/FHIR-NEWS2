---
title: NEWS2 ACVPU Guidance
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: news2_acvpu_guidance.html
summary: Guidance for populating the NEWS2 ACVPU Observation.
toc: false
---

The NEWS2 ACVPU observation reading uses the <a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-ACVPU-Observation-1" target="_blank">**CareConnect-ACVPU-Observation-1**</a> profile.

# Guidance for Populating a NEWS2 ACVPU Observation #

_Note that some elements are "Left uncurated as no use case in NEWS2", and are not needed for NEWS2._

<table>
<tr><th>CareConnect-ACVPU-Observation-1 element</th><th>Population Guidance</th></tr>
<tr><td>identifier</td><td>A unique identifier assigned to this observation (such as a generated Universally Unique Identifier {UUID})</td></tr>
<tr><td>basedOn</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>status</td><td>Fixed to "final"</td></tr>
<tr><td>category</td><td>The category holds a categorization from the sending system (for which the code, system & display MUST be populated). If no suitable categorization is available, the category may be omitted</td></tr>
<tr><td>code</td><td>The code is fixed to "1104441000000107" <br/> The system is fixed to "http://snomed.info/sct"</td></tr>
<tr><td>subject</td><td>A link to the Patient</td></tr>
<tr><td>context</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>effective[x]</td><td>The date and time that the ACVPU assessment was made, using effectiveDateTime</td></tr>
<tr><td>issued</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>performer</td><td>A link to the performer who carried out this observation. This must be a qualified practitioner and associated organisation</td></tr>
<tr><td>value[x]</td><td>The ACVPU assessment outcome as a valueCodeableConcept. One of the values in the <a href="https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ACVPU-1" target="_blank"><b>ACVPU valueSet</b></a></td></tr>
<tr><td>dataAbsentReason</td><td>Left uncurated as no use case in NEWS2 (as only observations with values should be sent for NEWS2)</td></tr>
<tr><td>interpretation</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>comment</td><td>Any additional notes or actions that the performer wishes to convey</td></tr>
<tr><td>bodySite</td><td>Left uncurated as no use case in NEWS2. Body site information may be implied by the pre-coordinated SNOMED CT concept used in Observation.code</td></tr>
<tr><td>method</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>device</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>referenceRange</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>related</td><td>A link to any related observations</td></tr>
<tr><td>component</td><td>None of the component elements are required for CareConnect-BodyTemperature-Observation-1</td></tr>
</table>

# Example #

<script src="https://gist.github.com/IOPS-DEV/8c93767ee55af828fcce1b959c0a3409.js"></script>
