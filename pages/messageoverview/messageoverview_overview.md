---
title: Message Design Overview
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: messageoverview_overview.html
summary: An overview of the NEWS 2 message design.
toc: true
---

There are three options within the message design for NEWS2, depending on the data available in the source system. The linkages between resources for the three options are shown below.

# 1. Systems holding the NEWS2 score, sub-scores & observations #

For systems that hold the NEWS2 score, the sub-scores and the associated observations
* the overall NEWS2 score is held in the NEWS2 profile
* the NEWS2 sub-scores are held in NEWS2 sub-score profiles, <a href="https://www.hl7.org/fhir/references.html#contained">**contained**</a> within the NEWS2 profile. The NEWS2 profile links to each sub-score profile using the a related link
* the observations are referenced by the sub-score profiles using the related links

The linkages for systems that hold the NEWS2 score, sub-scores and observations looks like this
<img src="./images/NEWS2AllOfIt.png" alt="NEWS2 score, sub-scores and observations"/>

# 2. Systems holding the NEWS2 score & observations only #

For systems that hold the NEWS2 score and the associated observations (but no sub-scores)
* the overall NEWS2 score is held in the NEWS2 profile
* the observations are referenced by the NEWS2 profile profiles using the related links

The linkages for systems that hold the NEWS2 score and observations looks like this
<img src="./images/NEWS2All.png" alt="NEWS2 score, sub-scores and observations"/>

# 3. Systems holding just the NEWS 2 score #

For systems that hold the NEWS2 score (but no sub-scores or associated observations)
* the overall NEWS2 score is held in the NEWS2 profile
* there are no related links

Systems that only hold the NEWS2 score will only send the NEWS2 profile
<img src="./images/NEWS2JustScore.png" alt="NEWS2 score, sub-scores and observations"/>