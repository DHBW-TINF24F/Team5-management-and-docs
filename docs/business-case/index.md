---
title: Business Case
nav_order: 1
---

# LOOK AT WORD VERSION AGAIN
| Version | Date       | Author         | Comment                                      |
|:--------:|:-----------:|:---------------:|:---------------------------------------------|
| 1.0 | 09.10.2025 | Nils Schäffner | Initialize BC and document structure          |
| 1.1  | 10.10.2025 | Nils Schäffner | Formulate Introduction, Scope and Benefits |
| 1.2 | 12.10.2025 | Nils Schäffner | Initialzie BC as Markdown in GitHub Docs |
| 1.3 | 14.10.2025 | Nils Schäffner | Add Gantt diagram and cost calculation |


# TABLE OF CONTENTS
Intro
Was ist zu verbessern, implementieren
Warum ist das gut
GANTT
RISIKOMATRIX
Kostenrechnungen
Angebot

# Introduction
This document outlines the business case for the upcoming software project. The project team has successfully collaborated on multiple projects in the past, continuously developing strong web engineering expertise to deliver high-quality digital products.
In the following sections, the customer’s order will be presented in detail, with a particular focus on the value and benefits our solution will provide to the client. Furthermore, this document serves as the formal business proposal submitted to the customer. It includes a comprehensive time and risk analysis, followed by a detailed cost estimation required to successfully complete the project.

# Scope
Mnestix Product Catalogue is a web-based open-source software designed to simplify the implementation of the Asset Administration Shell (AAS). Its main purpose is to support the creation and management of digital product catalogues, offering various features for browsing and organizing catalogue data.
However, several important usability and functionality aspects are still missing from a user perspective. The planned improvements will mainly focus on enhancing the application’s usability and integrating additional services such as the Nameplate Generator. Furthermore, eShop functionalities (e.g., Add to Cart, Show Cart) will be introduced, and the presentation of documentation and technical data will be refined.
The project also aims to improve product search, filtering, and data visualization while ensuring smoother interaction with repositories. In addition, the team will analyze existing features, evaluate the current usability concept, and implement targeted improvements to increase overall efficiency and user satisfaction.
#For detailed requirements see CRS


# Qualitative and quantitative benefits of development

The enhancement of the Mnestix Product Catalogue brings measurable functional and economic value by improving usability, efficiency, and interoperability within the AAS ecosystem.

| Qualitative Benefits |
|:---------------------|
| Improved Usability and User Experience
A clearer interface, faster navigation, and better data presentation reduce user effort and increase acceptance. |
| Enhanced Integration and Interoperability
Stronger AAS standard compliance enables smoother interaction with external systems and future extensions. |
| Higher Customer Satisfaction
Added features such as the Nameplate Generator and eShop functionality expand the system’s usefulness and market appeal. |
| Knowledge and Community Value
The project strengthens the open-source Mnestix ecosystem and the team’s expertise in digital twin technologies. |


| Quantitative Benefits |
|:----------------------|
| Time Efficiency – Up to 30–40% faster product search and data operations through optimized loading and filtering. |
| Lower Maintenance Costs – A more modular and documented codebase reduces long-term effort by 20–25%. |
| Improved Data Quality – More consistent repository handling reduces input errors by around 15–20%. |
| Future Scalability – A unified architecture supports cost-effective integration of future modules and services. |

#### Business Impact
Overall, the development increases productivity, reduces operational costs, and strengthens Mnestix’s position as a modern, user-friendly platform for AAS-based product catalogue management.

```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       Project Phase 1 Overview
    excludes    weekends

    section Docs
    BC                          :a1, 2025-09-26, 2025-11-01
    SAS                         :a2, 2025-09-26, 2025-11-01
    CRS                         :a3, 2025-09-26, 2025-11-03
    SRS                         :a4, 2025-09-26, 2025-11-04
    PM                          :a5, 2025-09-26, 2025-11-07
    Meeting Protocols            :a6, 2025-09-26, 2025-11-07

    section Analysis
    Test Mnestix and AAS         :b1, 2025-09-26, 2025-10-08
    Formulate Documentation Issues :b2, 2025-09-26, 2025-10-10
    Formulate Implementation Issues :b3, 2025-09-26, 2025-10-17
    Assign Implementation Issues :b4, 2025-10-10, 2025-10-24

    section Implementation
    Initialize GitHub Repository :c1, 2025-09-26, 2025-10-06
    Implement UI Features        :c2, 2025-10-18, 2025-11-14
    Implement Sorting Features   :c3, 2025-10-20, 2025-11-14
    Implement Filter Options     :c4, 2025-10-22, 2025-11-14
    Add eShop Features           :c5, 2025-10-24, 2025-11-14

    section Presentation
    Presentation                 :d1, 2025-10-17, 2025-11-07
```
```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       Project Phase 2 Overview
    excludes    weekends

    section Docs
    Meeting Minutes                 :a1, 2026-03-09, 2026-05-22
    STP (System Test Plan)          :a2, 2026-03-09, 2026-04-05
    STR (System Test Report)        :a3, 2026-04-16, 2026-05-14
    User Documentation              :a4, 2026-04-15, 2026-05-15
    Developer Documentation         :a5, 2026-04-18, 2026-05-17

    section Implementation
    Finish 3rd Semester Tasks       :c1, 2026-03-09, 2026-05-20
    Implement Product-View Features :c2, 2026-04-06, 2026-05-10
    Rework Submodel Usability       :c3, 2026-04-03, 2026-05-06
    Implement Performance Upgrades  :c4, 2026-04-02, 2026-05-13
    

    section Testing
    Develop Test Strategy           :d1, 2026-03-16, 2026-03-31
    Test Application                :d2, 2026-04-27, 2026-05-13
    Fix Errors                      :d3, 2026-05-04, 2026-05-20

    section Presentation & Handover
    Design Presentation             :e1, 2026-04-15, 2026-05-15     
    Present to Mnestix Team         :e2, 2026-05-15, 2026-05-21
    Final Presentation              :e4, 2026-05-20, 2026-05-22
    Project Handover                :e5, 2026-05-22, 2026-05-22
```




