---
title: NEWS2 Inspired Oxygen Guidance
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: news2_inspiredoxygen_guidance.html
summary: Guidance for populating the NEWS2 Inspired Oxygen Observation.
toc: false
---

The NEWS2 inspired oxygen observation observation uses the <a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-InspiredOxygen-Observation-1" target="_blank">**CareConnect-InspiredOxygen-Observation-1**</a> profile.

# Guidance for Populating a NEWS2 Inspired Oxygen Observation #

_Note that some elements are "Left uncurated as no use case in NEWS2", and are not needed for NEWS2._

<table>
<tr><th>CareConnect-InspiredOxygen-Observation-1 element</th><th>Population Guidance</th></tr>
<tr><td>identifier</td><td>A unique identifier assigned to this observation (such as a generated Universally Unique Identifier {UUID})</td></tr>
<tr><td>basedOn</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>status</td><td>Fixed to "final"</td></tr>
<tr><td>category</td><td>The category holds a categorisation from the sending system (for which the code, system & display MUST be populated). If no suitable categorisation is available,  category may be omitted</td></tr>
<tr><td>code</td><td>The code MUST contain one of the values from the <a href="https://fhir.hl7.org.uk/STU3/ValueSet/CareConnect-InspiredOxygen-1" target="_blank"><b>CareConnect-InspiredOxygen-1 valueSet</b></a><br/><br/><b>Note:</b> The inspired oxygen profile is a "code-only" observation, and does not contain a value element</td></tr>
<tr><td>subject</td><td>A link to the Patient</td></tr>
<tr><td>context</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>effective[x]</td><td>The date and time that the pulse rate was taken, using effectiveDateTime</td></tr>
<tr><td>issued</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>performer</td><td>A link to the performer who carried out this observation. This must be a qualified practitioner and associated organization</td></tr>
<tr><td>dataAbsentReason</td><td>Left uncurated as no use case in NEWS2 (as only the observations with values should be sent for NEWS2)</td></tr>
<tr><td>interpretation</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>comment</td><td>Any additional notes or actions that the performer wishes to convey</td></tr>
<tr><td>bodySite</td><td>Left uncurated as no use case in NEWS2. Body site information may be implied by the pre-coordinated SNOMED CT concept used in Observation.code</td></tr>
<tr><td>method</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>device</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>referenceRange</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>related</td><td>A link to any related observations</td></tr>
<tr><td>component</td><td>None of the component elements are required for NEWS2 Pulse rate Observation</td></tr>
</table>

# Example #

<script src="https://gist.github.com/IOPS-DEV/56895bbe5368669ab4207b0477d7064d.js"></script>
