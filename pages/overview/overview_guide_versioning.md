---
title: Guide Versioning
keywords: guide, versioning
tags: [development]
sidebar: overview_sidebar
permalink: overview_guide_versioning.html
summary: "An overview of how this implementation guide is versioned."
toc: false
---

{% include important.html content="This site is under development by NHS Digital, It is advised not to develop against these specifications until a formal announcement has been made." %}

# Alpha #
This implementation guidance is the Aphla release to support the development of NEWS2.

# Semantic Versioning #
Given a version number MAJOR.MINOR.PATCH, increment the:

MAJOR version when you make incompatible changes,
MINOR version when you add functionality in a backwards-compatible manner, and
PATCH version when you make backwards-compatible bug fixes.
Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

A pre-release version MAY be denoted by appending a hyphen. Refer to Semantic Versioning - Item 9 see <a href="http://semver.org/#spec-item-9">**here**</a>

# Pre-release Labels #
These labels will be taken from the GDS development process stages, and will be one of:

**Experimental**: Early development/POC version of an product for early sight during discovery

**Alpha**: Initial test product, likely to change substantially, or be discontinued as the project develops

**Beta**: APIs that are still under active development and subject to change, but that are likely to progress into a live product

**Release Candidate**: Products that are largely complete, unlikely to change substantially, but still need further testing before becoming live

**Live**: Release live Products

**Discontinued:** APIs which have been discontinued and should not be used for new development.