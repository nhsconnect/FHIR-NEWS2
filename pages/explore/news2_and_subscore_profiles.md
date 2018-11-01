---
title: NEWS2 Profiles
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: news2_and_subscore_profiles.html
summary: NEWS2, Sub-score & Observation Profiles
toc: false
---

# CareConnect NEWS2 Profile #

Sending the CareConnect-NEWS2-Observation-1 is mandatory for any system communicating a NEWS2 score.

[CareConnect-NEWS2-Observation-1](https://fhir.nhs.uk/STU3/StructureDefinition/CareConnect-NEWS2-Observation-1) - The overall NEWS2 score is reported in the NEWS2 Observation profile. If available, the NEWS2 Observation profile will contain the NEWS2 Sub-scores. For further information on contained resources see [here.](https://www.hl7.org/fhir/references.html#contained) Guidance for populating the NEWS2 Observation profile is [here.](news2_observation_guidance.html)


# CareConnect Sub-score Profile #

Sending the CareConnect-SubscoreObservation-1 is not mandated, but if source systems hold the sub-scores, they **SHOULD** be communicated.

[CareConnect-Subscore-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-Subscore-Observation-1) - Used to hold the sub-scores of the observations that go to make up the overall NEWS2 score. For further information on contained resources see [here](https://www.hl7.org/fhir/references.html#contained). There will be a CareConnect-SubscoreObservation-1 per observation. The CareConnect-SubscoreObservation-1 will reference its relevant observation using the Observation.related reference. Guidance for populating the CareConnect-SubscoreObservation-1 profile for NEWS2 is [here](/news2_subscore_guidance.html).


# NEWS2 Observation Profiles #

Sending the NEWS2 Observations is not mandated, but if the Observations are available on the source system they **SHOULD** be included as part of sending a NEWS2 score.

[CareConnect-BloodPressure-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-BloodPressure-Observation-1) - The systolic blood pressure used in generate the NEWS2 score. Guidance for populating the CareConnect-BloodPressure-Observation-1 profile for NEWS2 is [here](/news2_bloodpressure_guidance.html).

[CareConnect-BodyTemperature-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-BodyTemperature-Observation-1) - The body temperature reading used in generate the NEWS2 score. Guidance for populating the CareConnect-BodyTemperature-Observation-1 profile for NEWS2 is [here](/news2_bodytemperature_guidance.html).

[CareConnect-ACPVU-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-AVCPU-Observation-1) - The ACPUV observation used in generate the NEWS2 score. Guidance for populating the CareConnect-ACPUV-Observation-1 profile for NEWS2 is [here](/news2_acpvu_guidance.html).

[CareConnect-HeartRate-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-HeartRate-Observation-1) - The pulse rate reading used in generate the NEWS2 score. Guidance for populating the CareConnect-HeartRate-Observation-1 profile for NEWS2 is [here](/news2_pulserate_guidance.html).

[CareConnect-InspiredOxygen-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-InspiredOxygen-Observation-1) - The inspired oxygen observation used in generate the NEWS2 score. Guidance for populating the CareConnect-InspiredOxygen-Observation-1 profile for NEWS2 is [here](/news2_inspiredoxygen_guidance.html).

[CareConnect-OxygenSaturation-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-OxygenSaturation-Observation-1) - The oxygen saturation reading used in generate the NEWS2 score. Guidance for populating the CareConnect-oxygensaturation-Observation-1 profile for NEWS2 is [here](/news2_oxygensaturation_guidance.html).

[CareConnect-RespiratoryRate-Observation-1](https://fhir.hl7.org.uk/STU3/StructureDefinition/CareConnect-RespiratoryRate-Observation-1) - The respiratory rate reading used in generate the NEWS2 score. Guidance for populating the CareConnect-RespiratoryRate-Observation-1 profile for NEWS2 is [here](/news2_respiratoryrate_guidance.html).
