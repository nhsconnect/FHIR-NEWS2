---
title: NEWS2 ACPVU Guidance
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: news2_acpvu_guidance.html
summary: Guidance for populating the NEWS2 ACPVU Observation.
toc: false
---

The NEWS2 acpvu observation reading uses the <a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-AVCPU-Observation-1">CareConnect-ACPVU-Observation-1</a> profile.

# Guidance for Populating a NEWS2 ACPVU Observation #

When an Observation element has guidance "Not needed for NEWS2", this means that systems MAY populate the element (if appropriate) in the NEWS2 Observation.

<table>
<tr><th>CareConnect-ACPVU-Observation-1 element</th><th>Population Guidance</th></tr>
<tr><td>identifier</td><td>A unique identifier assigned to this observation (such as a generated universally unique identifier (uuid))</td></tr>
<tr><td>basedOn</td><td>Not needed for NEWS2</td></tr>
<tr><td>status</td><td>Fixed to "final"</td></tr>
<tr><td>category</td><td>category holds a categorisation from the sending system (for which the code, system & display MUST be populated). If no suitable categorisation is available,  category may be omitted</td></tr>
<tr><td>code</td><td>code is fixed to "1104441000000107", system is fixed to "http://snomed.info/sct"</td></tr>
<tr><td>subject</td><td>A link to the Patient</td></tr>
<tr><td>context</td><td>Not needed for NEWS2</td></tr>
<tr><td>effective[x]</td><td>The date and time that the ACPVU assessment was made, using effectiveDateTime.</td></tr>
<tr><td>issued</td><td>Not needed for NEWS2</td></tr>
<tr><td>performer</td><td>A link to the performer who carried out this observation. This must be a qualified practitioner and associated organisation.</td></tr>
<tr><td>value[x]</td><td>The ACPVU assessment outcome as a valueCodeableConcept. One of the values in the <a href="https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-ACPVU-1">ACPVU valueSet</a>.</td></tr>
<tr><td>dataAbsentReason</td><td>Not needed for NEWS2 (as only observations with values should be sent for NEWS2).</td></tr>
<tr><td>interpretation</td><td>Not needed for NEWS2</td></tr>
<tr><td>comment</td><td>Any additional notes or actions that the performer wishes to convey</td></tr>
<tr><td>bodySite</td><td>Not needed for NEWS2. Body site information may be implied by the pre-coordinated SNOMED CT concept used in Observation.code</td></tr>
<tr><td>method</td><td>Not needed for NEWS2</td></tr>
<tr><td>device</td><td>Not needed for NEWS2</td></tr>
<tr><td>referenceRange</td><td>Not needed for NEWS2</td></tr>
<tr><td>related</td><td>A link to any related observations.</td></tr>
<tr><td>component</td><td>None of the component elements are required for CareConnect-BodyTemperature-Observation-1</td></tr>
</table>

# Example #

<script src="https://gist.github.com/IOPS-DEV/8c93767ee55af828fcce1b959c0a3409.js"></script>
