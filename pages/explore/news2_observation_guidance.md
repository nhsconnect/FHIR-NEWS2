---
title: NEWS2 Observation Guidance
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: news2_observation_guidance.html
summary: Guidance for populating the NEWS2 Observation.
toc: false
---

The NEWS2 observation the <a href="https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-NEWS2-Observation-1">CareConnect-NEWS2-Observation-1</a> profile.

# Guidance for Populating a NEWS2 Observation #

When an Observation element has guidance "Not needed for NEWS2", this means that systems MAY populate the element (if appropriate) in the NEWS2 Observation.

<table>
<tr><th>CareConnect-NEWS2-Observation-1 element</th><th>Population Guidance</th></tr>
<tr><td>identifier</td><td>A unique identifier assigned to this observation (such as a generated universally unique identifier (uuid))</td></tr>
<tr><td>basedOn</td><td>Not needed for NEWS2</td></tr>
<tr><td>status</td><td>Fixed to "final"</td></tr>
<tr><td>category</td><td>Sending a category is optional. Systems may send their own category code (provided a code and system from which the code was picked are available). If no local category code is available, then category code may be fixed to "survey" and system fixed to "http://hl7.org/fhir/observation-category"</td></tr>
<tr><td>code</td><td>code is fixed to "1104051000000101" system is fixed to "http://snomed.info/sct"</td></tr>
<tr><td>subject</td><td>A link to the Patient</td></tr>
<tr><td>context</td><td>Not needed for NEWS2</td></tr>
<tr><td>effective[x]</td><td>The date and time that the NEWS2 score was confirmed, using effectiveDateTime.</td></tr>
<tr><td>issued</td><td>Not needed for NEWS2</td></tr>
<tr><td>performer</td><td>A link to the performer who carried out the NEWS2 score. This must be a qualified practitioner and associated organisation.</td></tr>
<tr><td>value[x]</td><td>The actual NEWS2 score as a valueQuantity. The NEWS2 score is carried in valueQuantity.value. Optionally a unit may be sent. If sending a unit, the system is fixed to "http://unitsofmeasure.org" and the code fixed to "{score}"</td></tr>
<tr><td>interpretation</td><td>Not needed for NEWS2</td></tr>
<tr><td>comment</td><td>Any additional notes or actions that the performer wishes to convey</td></tr>
<tr><td>method</td><td>Not needed for NEWS2</td></tr>
<tr><td>device</td><td>Not needed for NEWS2</td></tr>
<tr><td>referenceRange</td><td>Not needed for NEWS2</td></tr>
<tr><td>related</td><td>If NEWS2 sub-scores are being sent in the message, related will point to the contained CareConnect-SubScore-Observation-1 resources. For further information about referencing a contained resource see <a href="https://www.hl7.org/fhir/references.html#contained">here</a>. <br/><br/>If no NEWS2 sub-score are being sent, but supporting observations are being sent, then the related element will point to the supporting observations. Supporting observations are not contained withing the CareConnect-NEWS2-Observation-1 resource. The related links will reference the observations within the NEWS2 bundle. <br/><br/>If no sub-scores and no observations are being sent along with the NEWS2 score, then the related element is omitted.</td></tr>
</table>

# Examples #

## NEWS2 Score ##
<script src="https://gist.github.com/IOPS-DEV/6b6091d78652b9b0e2bc18c65b6b1543.js"></script>

## NEWS2 Score with Links to Observations ##
<script src="https://gist.github.com/IOPS-DEV/13227123b301b11144a57747d6e531e6.js"></script>

## NEWS2 Score with Links to Sub-scores ##
<script src="https://gist.github.com/IOPS-DEV/d00ad80060bfc315ebd38a4207da51ab.js"></script>
