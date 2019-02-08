---
title: Message Design Overview
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: messageoverview_overview.html
summary: An overview of the NEWS2 message design.
toc: false
---

The high-level design of NEWS2 based on developing a number of INTEROPen CareConnect Level 2 and level 3 profiles as below: 

<img src="./images/Level2Level3Profiles.png" alt="Level 2 and Level3 profiles"/>

The NEWS specification allows the sending of just the total NEWS2 score or the NEWS2 score with parameter values or the NEWS2 score, parameter values and their corresponding sub-scores.

These three options within the message design for NEWS2, depend on the data available in the source system. The linkages between resources for the three options are shown below.

## 1. Systems holding the NEWS2 score, sub-scores & observations ##

**This is the recommended option to share NEWS2.**

For systems that hold the NEWS2 score, the sub-scores and the associated observations:
* the overall NEWS2 score is held in the NEWS2 profile
* the NEWS2 sub-scores are held in NEWS2 sub-score profiles, <a href="https://www.hl7.org/fhir/references.html#contained" target="_blank">**contained**</a> within the NEWS2 profile. The NEWS2 profile links to each sub-score profile using the related link
* the observations are referenced by the sub-score profiles using the related links

The linkages for systems that hold the NEWS2 score, sub-scores and observations looks like this:
<img src="./images/NEWS2AllOfIt.png" alt="NEWS2 score, sub-scores and observations"/>

The diagram below illustrates this with sample clinical data:

<img src="./images/NEWS2SampleClinicalData.png" alt="NEWS2 with sample clinical data"/>

## 2. Systems holding the NEWS2 score & observations only ##

For systems that hold the NEWS2 score and the associated observations (but no sub-scores):
* the overall NEWS2 score is held in the NEWS2 profile
* the observations are referenced by the NEWS2 profile using the related links

The linkages for systems that hold the NEWS2 score and observations looks like this:
<img src="./images/NEWS2All.png" alt="NEWS2 score, sub-scores and observations"/>

## 3. Systems holding just the NEWS 2 score ##

For systems that hold the NEWS2 score (but no sub-scores or associated observations):
* the overall NEWS2 score is held in the NEWS2 profile
* there are no related links

Systems that only hold the NEWS2 score will only send the NEWS2 profile:
<img src="./images/NEWS2JustScore.png" alt="NEWS2 score, sub-scores and observations"/>