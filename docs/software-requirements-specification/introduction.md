---
layout: default
title: Introduction
parent: Software Requirements Specification
---

# Introduction
{: .no_toc }

1. TOC
{:toc}

## Purpose

The purpose of this document is to define user interface extensions for the Mnestix Browser.

The following specification is written for the developer team and the customer.
Secondary readers include computer science students.  
Required for reading this specification is knowledge about the Mnestix Browser and its current features (as of 2025-10-03).

## Definitions and Acronyms

**_SRS_** is the acronym for Software Requirements Specification.  
**_The software_** refers to all software parts specified here.  
**_The developer team_** includes all developers and organizations listed [here](index#software-requirements-specification).  
**_Extensions_** are further developments of the already existing code base of the Mnestix Browser if not stated further.  
**_The customer_** is the supervising lecturer.  
**_UI_** is an acronym for user interface.
**_Mnestix_** is a short form of Mnestix Browser.  
**_Power users_** are software users that spend a long time using the software.  
**_Regular users_** are software users that use the software sometimes.
**_Fast loading time_** refers to software loading times in a approrpiate time (less than 2 seconds) on a small repository (less than thousand entries) with a local installation of Mnestix on modern hardware.
**_Guest_** is a user that is not registered at the Mnestix Browser instance.

## Scope

The name of the product specified here is _Project Bisasam_.
Project Bisasam refers only to the extensions specified later.
The name Mnestix is not affected and stays.

Project Bisasam extends the usability and functionality of Mnestix' catalogue feature.
These extensions affect the catalogue/repository dashboard, the product list, the product view and the menu bar.
Project Bisasam covers only the UI extensions specified in this SRS. It does not affect the Mnestix core system.
All changes strictly refer to the UI.

The goal of project Bisasam is to add additional UI features to increase the Mnestix user experience.

## References

* Features requests where made by our supervising lecturer and can be found at the [DHBW-TINF24F GitHub Organization (root/project-5)](https://github.com/DHBW-TINF24F/.github/blob/main/project5_mnestix_product_catalogue.md)
* The structure of this SRS follows the [ISO/IEC/IEEE 29148:2018 standard](https://ieeexplore.ieee.org/document/8559686)
* Information about Mnestix Browser can be found on [Mnestix-Browser GitHub](https://github.com/eclipse-mnestix/mnestix-browser)

## Overview

This SRS does not strictly follow ISO/IEC/IEEE standard 29148:2018.
Some parts of this SRS follow the older standard IEEE 830-1984 because [TODO: but why?]
