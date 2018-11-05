---
title: Search for NEWS2 Score
keywords: explore, design, reference
tags: [design,explore]
sidebar: overview_sidebar
permalink: news2_get_score.html
summary: Guidance for populating the NEWS2 Sub-score.
toc: false
---

{% include important.html content="Site under development by NHS Digital, It is advised not to develop against these specifications until a formal announcement has been made." %}

## Use case ##

A system needs the NEWS2 of a patient that is held on another system.


## Security ##

- utilises TLS Mutual Authentication for system level authorization
- utilises a JSON Web Token (JWT) to transmit clinical Consumer system identity and authorisation details

## Search parameters ##

Provider systems SHALL support the following search parameters:

<table>
<th><td>Name</td><td>Type</td><td>Description</td><td>Paths</td></tr></th>
<tr><td>`nhs number`</td><td>identifier</td><td>The NHS Number</td><td></td></tr>
<tr><td>`code`</td><td></td><td>token</td><td></td>Observation code for NEWS2</tr>
<tr><td>`start`</td><td></td><td>dateTime</td>NEWS2 from date<td></td></tr>
<tr><td>`end`</td><td></td><td>dateTime</td><td>NEWS2 end date</td></tr>
</table>

{% include note.html content="The supported search parameters should be included in the FHIR Capability Statement." %}

## _include parameters ##

Provider systems SHALL support the following include parameters: