---
title: NEWS2 Body Temperature Guidance
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: news2_bodytemperature_guidance.html
summary: Guidance for populating the NEWS2 Body Temperature Observation.
toc: false
---

The NEWS2 body temperature observation reading uses the <a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-BodyTemperature-Observation-1" "target="_blank">**CareConnect-BodyTemperature-Observation-1**</a> profile.

# Guidance for Populating a NEWS2 Body Temperature Observation #

_Note that some elements are "Left uncurated as no use case in NEWS2", and are not needed for NEWS2._

<table>
<tr><th>CareConnect-BodyTemperature-Observation-1 element</th><th>Population Guidance</th></tr>
<tr><td>identifier</td><td>A unique identifier assigned to this observation (such as a generated universally unique identifier (uuid))</td></tr>
<tr><td>basedOn</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>status</td><td>Fixed to "final"</td></tr>
<tr><td>category</td><td>code is fixed to "vital-signs" <br/>system is fixed to "http://hl7.org/fhir/observation-category"</td></tr>
<tr><td>code</td><td>code MUST contain the <a href="https://www.hl7.org/fhir/observation-vitalsigns.html#vitals-table" target="_blank"><b>Magic Code</b></a> as per the HL7 vital signs guidance, MUST also have a SNOMED CT equivalent Magic Code and MAY have a more refined SNOMED CT concept code<br/><br/>For NEWS2 body temperature Magic Code, code is fixed to "8310-5", system is fixed to "http://loinc.org"<br/><br/>For NEWS2 body temperature SNOMED CT Magic Code, code is fixed to "276885007", system is fixed to "http://snomed.info/sct"<br/>For more refined SNOMED CT codes, code is from the valueSet defined <a href="#more-refined-snomed-ct-codes-for-body-temperature"><b>here</b></a>, system is fixed to "http://snomed.info/sct".<br/><br/>If a more refined SNOMED CT code is used, then the userSelected element for that code MUST be checked. </td></tr>
<tr><td>subject</td><td>A link to the Patient</td></tr>
<tr><td>context</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>effective[x]</td><td>The date and time that the body temperature was taken, using effectiveDateTime</td></tr>
<tr><td>issued</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>performer</td><td>A link to the performer who carried out this observation. This must be a qualified practitioner and associated organisation.</td></tr>
<tr><td>value[x]</td><td>The actual body temperature reading as a valueQuantity. The unit is fixed to "Cel" and the system fixed to UCUM "http://unitsofmeasure.org"</td></tr>
<tr><td>dataAbsentReason</td><td>Left uncurated as no use case in NEWS2 (as only observations with values should be sent for NEWS2).</td></tr>
<tr><td>interpretation</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>comment</td><td>Any additional notes or actions that the performer wishes to convey</td></tr>
<tr><td>bodySite</td><td>Left uncurated as no use case in NEWS2. Body site information may be implied by the pre-coordinated SNOMED CT concept used in Observation.code</td></tr>
<tr><td>method</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>device</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>referenceRange</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>related</td><td>A link to any related observations.</td></tr>
<tr><td>component</td><td>None of the component elements are required for CareConnect-BodyTemperature-Observation-1</td></tr>
</table>


## More Refined SNOMED CT Codes for Body Temperature ##
<<386725007|Body temperature (observable entity)| <br/>
MINUS (<<248458005|Comparative temperature in limbs (observable entity)| <br/>
OR <<852591000000107|Maximum body temperature (observable entity)| <br/>
OR <<852601000000101|Minimum body temperature (observable entity)| <br/>
OR <<852581000000105|Target body temperature (observable entity)| <br/>
OR <<364419004|Temperature of cervical spine (observable entity)| <br/>
OR <<364424001|Temperature of thoracic spine (observable entity)| <br/>
OR <<364429006|Temperature of lumbar spine (observable entity)| <br/>
OR <<248835004|Temperature of breast (observable entity)| <br/>
OR <<250124002|Temperature of joint (observable entity)| <br/>
OR <<431197002|Temperature of digit (observable entity)| <br/>
OR <<364518005|Temperature of foot (observable entity)| <br/>
OR <<363997004|Temperature of pinna (observable entity)| <br/>
OR <<364537001|Temperature of skin (observable entity)|) 

# Example #

<script src="https://gist.github.com/IOPS-DEV/d187d3f2c76a3a0df7404252dfb55764.js"></script>
