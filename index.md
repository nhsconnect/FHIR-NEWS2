---
title: National Early Warning Score (NEWS)2
keywords: homepage
tags: [getting_started]
sidebar: overview_sidebar
permalink: index.html
toc: true
summary: A brief introduction to getting started.
---

This is the Implementation Guide for developing NEWS2 interoperability.

Possible use cases where this Implementation Guide should be followed include:

* A vital signs app to an Electronic Patient Record in a hospital
* Ambulance to Emergency Department
* Hospital to hospital patient transfers
* Hospital look up of observations in GP systems (they have an integrated record which includes obs recorded in GP systems which can be viewed by hospital doctors in his Trust).  
* Ambulance recording on remote devices and communicating to central ambulance record
* GP to ambulance

# Quick Links #
* The Message Design options for NEWS2 implementation are documented <a href="/messageoverview_overview.html">here</a>

* The FHIR resources used in a NEWS2 exchange are documented <a href="/news2_and_subscore_profiles.html">here</a>

# How NEWS2 Works #
The NEWS is based on a simple aggregate scoring system in which a score is allocated to physiological measurements, already recorded in routine practice, when patients present to, or are being monitored in hospital. Six simple physiological parameters plus an inspired oxygen observation form the basis of the scoring system:

1. respiration rate
2. oxygen saturation
3. systolic blood pressure
4. pulse rate
5. level of consciousness or new confusion*
6. temperature.
7. inspired oxygen

_*The patient has new-onset confusion, disorientation and/or agitation, where previously their mental state was normal – this may be subtle. The patient may respond to questions coherently, but there is some confusion, disorientation and/or agitation. This would score 3 or 4 on the GCS (rather than the normal 5 for verbal response), and scores 3 on the NEWS system._

A score is allocated to each parameter as they are measured, with the magnitude of the score reflecting how extremely the parameter varies from the norm. The score is then aggregated and uplifted by 2 points for people requiring supplemental oxygen to maintain their recommended oxygen saturation.

This is a pragmatic approach, with a key emphasis on system-wide standardisation and the use of physiological  parameters that are already routinely measured in NHS hospitals and in pre-hospital care, recorded on a standardised clinical chart – the NEWS2 chart.

A full description of NEWS2 is available from the Royal College of Physicians <a href="https://www.rcplondon.ac.uk/projects/outputs/national-early-warning-score-news-2">here</a>.

