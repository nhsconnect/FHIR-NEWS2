---
title: NEWS2 Blood Pressure Guidance
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: news2_bloodpressure_guidance.html
summary: Guidance for populating the NEWS2 Blood Pressure Observation.
toc: false
---

The NEWS2 blood pressure observation reading uses the <a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-BloodPressure-Observation-1" target="_blank">CareConnect-BloodPressure-Observation-1</a>.

Only the systolic part of the blood pressure observation is used in the NEWS2 score, but systems should send both the systolic and diastolic blood pressure components.

# Guidance for Populating a NEWS2 Blood Pressure Observation #

_Note that some elements are "Left uncurated as no use case in NEWS2", and are not needed for NEWS2._

<table>
<tr><th>CareConnect-BloodPressure-Observation-1 element</th><th>Population Guidance</th></tr>
<tr><td>identifier</td><td>A unique identifier assigned to this observation (such as a generated universally unique identifier (uuid))</td></tr>
<tr><td>basedOn</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>status</td><td>Fixed to "final"</td></tr>
<tr><td>category</td><td>code is fixed to "vital-signs" <br/>system is fixed to "http://hl7.org/fhir/observation-category"</td></tr>
<tr><td>code</td><td>code MUST contain the <a href="https://www.hl7.org/fhir/observation-vitalsigns.html#vitals-table" target="_blank"><b>Magic Code</b></a> as per the HL7 vital signs guidance, MUST also have a SNOMED CT equivalent Magic Code and MAY have a more refined SNOMED CT concept code<br/><br/>For NEWS2 blood pressure Magic Code, code is fixed to "85354-9", system is fixed to "http://loinc.org"<br/><br/>For NEWS2 blood pressure SNOMED CT Magic Code, code is fixed to "75367002", system is fixed to "http://snomed.info/sct"<br/>For more refined SNOMED CT codes, code is from the valueSet defined <a href="#more-refined-snomed-ct-codes-for-blood-pressure"><b>here</b></a>, system is fixed to "http://snomed.info/sct".<br/><br/>If a more refined SNOMED CT code is used, then the userSelected element for that code MUST be checked. </td></tr>
<tr><td>subject</td><td>A link to the Patient</td></tr>
<tr><td>context</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>effective[x]</td><td>The date and time that the blood pressure was taken, using effectiveDateTime</td></tr>
<tr><td>issued</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>performer</td><td>A link to the performer who carried out this observation. This must be a qualified practitioner and associated organisation.</td></tr>
<tr><td>dataAbsentReason</td><td>Left uncurated as no use case in NEWS2 (as only observations with values should be sent for NEWS2).</td></tr>
<tr><td>interpretation</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>comment</td><td>Any additional notes or actions that the performer wishes to convey</td></tr>
<tr><td>bodySite</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>method</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>device</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>referenceRange</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>related</td><td>A link to any related observations.</td></tr>
<tr><td>component[systolic].code</td><td>code MUST contain the <a href="https://www.hl7.org/fhir/observation-vitalsigns.html#vitals-table" target="_blank"><b>Magic Code</b></a> as per the HL7 vital signs guidance, MUST also have a SNOMED CT equivalent Magic Code and MAY have a more refined SNOMED CT concept code<br/><br/>For NEWS2 systolic blood pressure Magic Code, code is fixed to "8480-6", system is fixed to "http://loinc.org"<br/><br/>For NEWS2 systolic blood pressure SNOMED CT Magic Code, code is fixed to "72313002", system is fixed to "http://snomed.info/sct"<br/>For more refined SNOMED CT codes, code is from the valueSet defined <a href="#more-refined-snomed-ct-codes-for-systolic-blood-pressure">here</a>, system is fixed to "http://snomed.info/sct".<br/><br/>If a more refined SNOMED CT code is used, then the userSelected element for that code MUST be checked. </td></tr>
<tr><td>component[systolic].value[x]</td><td>The actual systolic blood pressure reading as a valueQuantity. The unit is fixed to "mm[Hg]" and the system fixed to UCUM "http://unitsofmeasure.org"</td></tr>
<tr><td>component[systolic].dataAbsentReason</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>component[systolic].interpretation</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>component[systolic].referenceRange</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>component[diastolic].code</td><td>code MUST contain the <a href="https://www.hl7.org/fhir/observation-vitalsigns.html#vitals-table" target="_blank"><b>Magic Code</b></a> as per the HL7 vital signs guidance, MUST also have a SNOMED CT equivalent Magic Code and MAY have a more refined SNOMED CT concept code<br/><br/>For NEWS2 systolic blood pressure Magic Code, code is fixed to "8462-4", system is fixed to "http://loinc.org"<br/><br/>For NEWS2 systolic blood pressure SNOMED CT Magic Code, code is fixed to "1091811000000102", system is fixed to "http://snomed.info/sct"<br/>For more refined SNOMED CT codes, code is from the valueSet defined <a href="#more-refined-snomed-ct-codes-for-diastolic-blood-pressure">here</a>, system is fixed to "http://snomed.info/sct".<br/><br/>If a more refined SNOMED CT code is used, then the userSelected element for that code MUST be checked. </td></tr>
<tr><td>component[diastolic].value[x]</td><td>The actual systolic blood pressure reading as a valueQuantity. The unit is fixed to "mm[Hg]" and the system fixed to UCUM "http://unitsofmeasure.org"</td></tr>
<tr><td>component[diastolic].dataAbsentReason</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>component[diastolic].interpretation</td><td>Left uncurated as no use case in NEWS2</td></tr>
<tr><td>component[diastolic].referenceRange</td><td>Left uncurated as no use case in NEWS2</td></tr>
</table>


## More Refined SNOMED CT Codes for Blood Pressure ##
<<75367002|Blood pressure (observable entity)| <br/>
MINUS (<<271650006|Diastolic blood pressure (observable entity)| <br/>
OR <<271649006|Systolic blood pressure (observable entity)| <br/>
OR <<928021000000108|Baseline blood pressure (observable entity)|<br/> 
OR <<87541000000108|Highest brachial systolic pressure (observable entity)| <br/>
OR <<723235005|Maximum blood pressure (observable entity)| <br/>
OR <<723236006|Minimum blood pressure (observable entity)| <br/>
OR <<314453003|Average diastolic blood pressure (observable entity)| <br/>
OR <<314440001|Average systolic blood pressure (observable entity)| <br/>
OR <<251073000|Invasive diastolic arterial pressure (observable entity)| <br/>
OR <<251071003|Invasive systolic arterial pressure (observable entity)| <br/>
OR <<276781007|Left ventricular end-diastolic pressure (observable entity)| <br/>
OR <<276780008|Left ventricular systolic pressure (observable entity)| <br/>
OR <<1036571000000105|Non-invasive central diastolic blood pressure (observable entity)| <br/>
OR <<1036551000000101|Non-invasive central systolic blood pressure (observable entity)| <br/>
OR <<174255007|Non-invasive diastolic arterial pressure (observable entity)| <br/>
OR <<251070002|Non-invasive systolic arterial pressure (observable entity)| <br/>
OR <<276772001|Right ventricular systolic pressure (observable entity)| <br/>
OR <<276774000|Right ventricular end-diastolic pressure (observable entity)| <br/>
OR <<399023006|Right ventricular peak systolic pressure (observable entity)| <br/>
OR <<276773006|Right ventricular diastolic pressure (observable entity)|)


## More Refined SNOMED CT Codes for Systolic Blood Pressure ##
<<271649006|Systolic blood pressure (observable entity)| <br/>
MINUS (<<716579001|Baseline systolic blood pressure (observable entity)| <br/>
OR <<814101000000107|Systolic blood pressure centile (observable entity)| <br/>
OR <<315612005|Target systolic blood pressure (observable entity)|)


## More Refined SNOMED CT Codes for Diastolic Blood Pressure ##
<<271650006|Diastolic blood pressure (observable entity)| <br/>
MINUS (<<716632005|Baseline diastolic blood pressure (observable entity)| <br/>
OR <<315613000|Target diastolic blood pressure (observable entity)| <br/>
OR <<814081000000101|Diastolic blood pressure centile (observable entity)|)

# Example # 

<script src="https://gist.github.com/IOPS-DEV/a6486833f180ee3ff10355fe059b96bf.js"></script>
