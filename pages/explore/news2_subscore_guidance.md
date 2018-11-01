---
title: NEWS2 Sub-score Guidance
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: news2_subscore_guidance.html
summary: Guidance for populating the NEWS2 Sub-score.
toc: false
---

The NEWS2 sub-score observation uses the <a href="https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Subscore-Observation-1">CareConnect-Subscore-Observation-1</a> profile.

# Guidance for Populating a NEWS2 Sub-score Observation #

When an Observation element has guidance "Not needed for NEWS2", this means that systems MAY populate the element (if appropriate) in the NEWS2 Observation.

<table>
<tr><th>CareConnect-Subscore-Observation-1 element</th><th>Population Guidance</th></tr>
<tr><td>identifier</td><td>A unique identifier assigned to this observation (such as a generated universally unique identifier (uuid))</td></tr>
<tr><td>basedOn</td><td>Not needed for NEWS2</td></tr>
<tr><td>status</td><td>Fixed to "final"</td></tr>
<tr><td>category</td><td>Sending a category is optional. Systems may send their own category code (provided a code and system from which the code was picked are available). If no local category code is available, then category code may be fixed to "survey" and system fixed to "http://hl7.org/fhir/observation-category"</td></tr>
<tr><td>code</td><td>The codes for each NEWS2 sub-score are <a href="#code-values-for-news2-sub-scores">here</a>, the system is fixed to "http://snomed.info/sct"</td></tr>
<tr><td>subject</td><td>A link to the Patient</td></tr>
<tr><td>context</td><td>Not needed for NEWS2</td></tr>
<tr><td>effective[x]</td><td>The date and time that the NEWS2 sub-score was confirmed, using effectiveDateTime</td></tr>
<tr><td>issued</td><td>Not needed for NEWS2</td></tr>
<tr><td>performer</td><td>A link to the performer who carried out the NEWS2 observation. This must be a qualified practitioner and associated organisation.</td></tr>
<tr><td>value[x]</td><td>The actual NEWS2 sub-score as a valueQuantity. The NEWS2 sub-score is carried in valueQuantity.value. Optionally a unit may be sent. If sending a unit, the system is fixed to "http://unitsofmeasure.org" and the code fixed to "{score}"</td></tr>
<tr><td>interpretation</td><td>Not needed for NEWS2</td></tr>
<tr><td>comment</td><td>Any additional notes or actions that the performer wishes to convey</td></tr>
<tr><td>method</td><td>Not needed for NEWS2</td></tr>
<tr><td>device</td><td>Not needed for NEWS2</td></tr>
<tr><td>referenceRange</td><td>Not needed for NEWS2</td></tr>
<tr><td>related</td><td>A reference to the observation that has generated the sub-score</td></tr>
<tr><td>component</td><td>None of the component elements are to be populated for a NEWS2 sub-score</td></tr>
</table>

## Code Values for NEWS2 Sub-scores ##
1104301000000104 | Royal College of Physicians National Early Warning Score 2 - respiration rate score  <br/>
1104311000000102 | Royal College of Physicians National Early Warning Score 2 - oxygen saturation scale 1 score <br/>
1104321000000108 | Royal College of Physicians National Early Warning Score 2 - oxygen saturation scale 2 score <br/>
1104331000000105 | Royal College of Physicians National Early Warning Score 2 - air or oxygen score <br/>
1104351000000103 | Royal College of Physicians National Early Warning Score 2 - pulse score <br/>
1104341000000101 | Royal College of Physicians National Early Warning Score 2 - systolic blood pressure score <br/>
1104361000000100 | Royal College of Physicians National Early Warning Score 2 - consciousness score <br/>
1104371000000107 | Royal College of Physicians National Early Warning Score 2 - temperature score

# Example #

<script src="https://gist.github.com/IOPS-DEV/3afd69d2baa1b48bb2cd65d5c8c429f4.js"></script>

