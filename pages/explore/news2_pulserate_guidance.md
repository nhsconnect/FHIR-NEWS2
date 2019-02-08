---
title: NEWS2 Pulse Rate Guidance
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: news2_pulserate_guidance.html
summary: Guidance for populating the NEWS2 Pulse Rate Observation.
toc: false
---

The NEWS2 pulse rate observation uses the <a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-HeartRate-Observation-1" target="_blank">**CareConnect-HeartRate-Observation-1**</a> profile.

# Guidance for Populating a NEWS2 Pulse Rate Observation #

### Note on heart rate versus pulse rate ###
This specification uses the CareConnect-HeartRate-Observation-1 to carry the NEWS2 Pulse Rate observation. It has been noted that heart rate and pulse rate are different measures, and not necessarily be interchangeable.
<br/><br/>
_‘Heart rate is typically measured electrically and pulse rate physically. If you have two heart beats close together – for example, ectopic beats – you can’t physically discriminate. So the pulse rate would be lower than the heart rate. It is also common in atrial fibrillation – the true heart rate can be much higher than the pulse rate.’_
<br/><br/>
The curation team had to take this into account to create an option of sending an additional specific SNOMED CT code of "78564009 | Pulse rate" in the profile for the NEWS2 use case which will be marked as userSelected value="true" in FHIR.  This allows the sender to specify that a pulse rate was taken which is a refinement of the SNOMED CT concept heart rate. The sender could just send heart rate without the pulse rate if the heart rate was recorded. In the scenario, when the pulse rate is different from heart rate, it is expected only heart rate will be sent as this is more accurate from a clinical perspective. A fuller account of guidance on heart rate versus pulse rate can be found <a href="https://docs.google.com/document/d/1ByZ57nh6ZDjUEfBfPJjLAfSil_svpjBpzbarv7VB5QM/edit?usp=sharing" target="_blank">**here**</a>.
<br/><br/>

_Note that some elements are "Left uncurated as no use case in NEWS2", and are not needed for NEWS2._
<br/><br/>
<table>
<tr><th>CareConnect-HeartRate-Observation-1 element</th><th>Population Guidance</th></tr>
<tr><td>identifier</td><td>A unique identifier assigned to this observation (such as a generated Universally Unique Identifier {UUID})</td></tr>
<tr><td>basedOn</td><td>Not needed for NEWS2</td></tr>
<tr><td>status</td><td>Fixed to "final"</td></tr>
<tr><td>category</td><td>The code is fixed to "vital-signs" <br/>The system is fixed to "http://hl7.org/fhir/observation-category"</td></tr>
<tr><td>code</td><td>The code MUST contain the <a href="https://www.hl7.org/fhir/observation-vitalsigns.html#vitals-table" target="_blank"><b>Magic Code</b></a> as per the HL7 vital signs guidance, MUST also have a SNOMED CT equivalent Magic Code and MAY have a more refined SNOMED CT concept code<br/><br/>For NEWS2 Pulse Rate Magic Code, the code is fixed to "8867-4" and the system is fixed to "http://loinc.org"<br/><br/>For NEWS2 pulse rate SNOMED CT Magic Code, the code is fixed to "364075005" and the system is fixed to "http://snomed.info/sct"<br/><br/>For more refined SNOMED CT codes, the code is from the valueSet defined <a href="#more-refined-snomed-ct-codes-for-pulse-rate"><b>here</b></a> and the system is fixed to "http://snomed.info/sct"<br/><br/>If a more refined SNOMED CT code is used, then the userSelected element for that code MUST be checked<br/><br/><b>Note:</b> If a pulse rate is being sent (rather than heart rate), then a more refined code of "78564009", the system "http://snomed.info/sct" and the userSelected element checked should be sent</td></tr>
<tr><td>subject</td><td>A link to the Patient</td></tr>
<tr><td>context</td><td>Not needed for NEWS2</td></tr>
<tr><td>effective[x]</td><td>The date and time that the pulse rate was taken, using effectiveDateTime</td></tr>
<tr><td>issued</td><td>Not needed for NEWS2</td></tr>
<tr><td>performer</td><td>A link to the performer who carried out this observation. This must be a qualified practitioner and associated organisation</td></tr>
<tr><td>value[x]</td><td>The actual pulse rate reading as a valueQuantity. The unit is fixed to "/min" and the system fixed to UCUM "http://unitsofmeasure.org"</td></tr>
<tr><td>dataAbsentReason</td><td>Not needed for NEWS2 (as only observations with values should be sent for NEWS2)</td></tr>
<tr><td>interpretation</td><td>Not needed for NEWS2</td></tr>
<tr><td>comment</td><td>Any additional notes or actions that the performer wishes to convey</td></tr>
<tr><td>bodySite</td><td>Not needed for NEWS2. Body site information may be implied by the pre-coordinated SNOMED CT concept used in Observation.code</td></tr>
<tr><td>method</td><td>Not needed for NEWS2</td></tr>
<tr><td>device</td><td>Not needed for NEWS2</td></tr>
<tr><td>referenceRange</td><td>Not needed for NEWS2</td></tr>
<tr><td>related</td><td>A link to any related observations</td></tr>
<tr><td>component</td><td>None of the component elements are required for NEWS2 Pulse rate Observation</td></tr>
</table>


## More Refined SNOMED CT Codes for Pulse Rate ##
<<364075005|Heart rate (observable entity)| <br/>
MINUS (<<928001000000104|Baseline heart rate (observable entity)| <br/>
OR <<428420003|Target heart rate (observable entity)| <br/>
OR <<852341000000107|Maximum pulse rate (observable entity)| <br/>
OR <<852351000000105|Minimum pulse rate (observable entity)| <br/>
OR <<852331000000103|Target pulse rate (observable entity)|)

# Example #

<script src="https://gist.github.com/IOPS-DEV/21c81e9f21c1869765cfb52a204d2b47.js"></script>