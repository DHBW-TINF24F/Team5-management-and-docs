# Customer Requirements Specification (CRS)


## Project: Eclipse Mnestix Product Catalog
**Version:** 1.1  
**Author:** Julian Schumacher  
**Date:** 24.10.2025  
**Institution:** [DHBW or Course Name]  

---

## Document Version History
| Version | Date | Author | Description |
|----------|------|---------|-------------|
| 1.0 | 18.10.2025 | Julian Schumacher | Initial Version |
| 1.1 | 24.10.2025 | Julian Schumacher | Update structure and navigation |
| 1.2 | 24.10.2025 | Julian Schumacher | restructure requirements |

---

## Table of Contents
1. [Purpose and Objectives  ](#1-purpose-and-objectives)
2. [Project Context  ](#2-project-context)
3. [Stakeholder Analysis  ](#3-stakeholder-analysis)
4. [Current Situation and Problem Statement  ](#4-current-situation-and-problem-statement)
5. [General Requirements  ](#5-general-requirements)
6. [Functional Requirements  ](#6-functional-requirements)
7. [Non-Functional Requirements  ](#7-non-functional-requirements)
8. [System Context and Interfaces  ](#8-system-context-and-interfaces)
9. [Constraints and Assumptions  ](#9-constraints-and-assumptions)
10. [Acceptance Criteria  ](#10-acceptance-criteria)
11. [Glossary  ](#11-glossary)
12. [References  ](#12-references)

---

## 1. Purpose and Objectives
The purpose of this Customer Requirements Specification (CRS) is to define the business-oriented needs and expectations for the enhancement of the Eclipse Mnestix Product Catalog, a web-based application designed for the visualization and management of Asset Administration Shells (AAS) within Industry 4.0 environments.

The project aims to improve usability, performance, and functional completeness of the Mnestix Product Catalog by addressing existing shortcomings and implementing new features that make the platform more accessible to non-technical users such as engineers, product managers, and customers in said industrial settings.

This document does not include technical implementation details but focuses on the requirements from a customer and stakeholder perspective.

### Objectives
- Enhance the user interface (UI) for improved clarity and responsiveness.  
- Introduce configuration flexibility for connected repositories.  
- Improve data visualization and filtering capabilities within product listings.  
- Integrate external tools such as the Nameplate Generator directly into the user workflow.  
- Ensure compatibility with existing BaSyx and AAS infrastructures.

---

## 2. Project Context

### 2.1 Background
Eclipse Mnestix is an open-source project that provides a web-based interface for exploring and managing Asset Administration Shells — the digital representations of industrial assets defined under the Industry 4.0 standard.  
The project aligns with initiatives from the Industrial Digital Twin Association (IDTA) and integrates with infrastructures such as Eclipse BaSyx.

Current Mnestix implementations primarily target developers and technical users. The usability and visual clarity of its product catalog are limited, leading to a steep learning curve for less technical stakeholders.
In order to provide a much simpler and more efficient user experience, this project focuses on enhancing the Mnestix Product Catalog to better serve a broader audience such as product managers and customers.

### 2.2 Project Scope
The scope of this project includes:
- Enhancement of the Mnestix Product Catalog web interface.
- Integration of usability improvements and visual redesigns.
- Implementation of asynchronous data loading and advanced filtering.
- Connection with the Nameplate Generator for generating product labels.
- Validation of the improved catalog against multiple AAS servers.

---

## 3. Stakeholder Analysis

| Stakeholder | Role / Interest | Expectations | Influence |
|--------------|----------------|---------------|-----------|
| **End Users (Engineers, Product Managers)** | Daily users of the catalog | Simple navigation, clear data presentation, stable performance | High |
| **Developers / Maintainers** | Implement new features and fix issues | Clean modular architecture, minimal technical debt, good documentation | High |
| **Eclipse & IDTA** | Ecosystem coordinators | Alignment with Industry 4.0 standards | Medium |
| **Academic Supervisors / Project Sponsors** | Oversight and evaluation | Comprehensive documentation, measurable improvement and requirement satisfaction | Medium |
| **Community Contributors** | Potential future maintainers | Clear contribution guidelines, usable interface, understandable codebase | Low |

---

## 4. Current Situation and Problem Statement

### 4.1 Existing System
The current Mnestix Product Catalog provides:
- Access to AAS repositories through a technical interface.
- Visualization of AAS data and associated submodels.
- Basic configuration of connected repositories.

### 4.2 Identified Problems
- **Usability issues:** Non-intuitive interface layout, limited user guidance.
- **Performance issues:** Repository loading can take long and blocks the UI. Loading of Thumbnails for all products at once causes delays.
- **Lack of configurability:** Repositories cannot be selectively enabled or disabled.
- **Poor data visibility:** Insufficient support for filtering, sorting, and previewing data.
- **Visual inconsistencies:** Misaligned formatting and table rendering in submodel views.
- **Limited integration:** No seamless access in the user flow to related tools such as the Nameplate Generator.
- **Missing eShop functionality:** Users cannot interactively add products to a cart or view selected items.

### 4.3 Business Impact
These issues limit the adoption of the Mnestix Product Catalog in industrial contexts, particularly by non-developers. Improving usability and accessibility is crucial for broader acceptance and alignment with Industry 4.0 usability expectations.
Completing this project will enhance user satisfaction and will therefore increase the user base. It will also increase productivity and promote the use of digital twins in industrial applications.

---

## 5. General Requirements

1. The application shall display the **user login status** permanently in the header section.
2. The system shall provide an **improved configuration view** to manage connected repositories.  
3. The catalog shall be **visually modernized** to improve readability and information density.  
4. The overall **performance** and **responsiveness** of the application must be improved.  
5. The system must remain **open-source** and compatible with existing Mnestix and BaSyx ecosystems.
6. The application shall support related tools such as the **Nameplate Generator** directly from the product view.  
7. The system shall implement **eShop-like features** for product selection and cart management.
8. In the product overview, related AAS entities shall be **clickable links** for easy navigation. 

---

## 6. Functional Requirements

### 6.1 Configuration View
- The user shall be able to **add, modify, or remove repositories** through a configuration dialog.  
- The user shall be able to **disable specific repositories** temporarily without deleting them.  
- The user shall be able to **view the contents** of each connected repository (Concept Descriptions, AAS entries).  

### 6.2 Catalog Overview
- The catalog shall display the **number of products** contained in each repository.  
- Users shall be able to identify which repositories are currently active.  
- The catalog shall support **searching and filtering** across all repositories.  

### 6.3 Product List
- 
- Only **AAS objects of type `AssetKind == Type`** shall be displayed by default.  
- The list shall include columns for:
  - `ManufacturerName`
  - `ProductDesignation`
  - `OrderCode`
  - `ManufacturerCode`
  - `globalAssetId`
  - `createdAt`
- Users shall be able to **sort** the list by any of the above attributes.  
- Thumbnails and images shall load only for **visible entries** to optimize performance.  
- Users shall be able to **apply filtering parameters** through query options in the UI.  

### 6.4 Product Detail View
- Users shall be able to view **detailed submodels** such as:
  - Technical Data
  - Bill of Materials (BOM)
  - Handover Documentation
- The **Nameplate Generator** shall be directly accessible through the product action menu.  
- Submodels containing links to other AAS entities shall be **clickable** for easy navigation.  
- The **Handover Documentation** view shall be reformatted for better readability.  
- The system shall include **eShop-like features** such as:
  - `Add to Cart`
  - `View Cart`
  - `Remove Item from Cart`

---

## 7. Non-Functional Requirements

| Category | Requirement | Description |
|-----------|--------------|-------------|
| **Usability** | The system must provide a modern, responsive, and intuitive UI suitable for both technical and non-technical users. | Focus on clarity, simplicity, and accessibility. |
| **Performance** | The system shall load large repository data sets asynchronously and efficiently. | No blocking operations during data retrieval. |
| **Reliability** | The system must handle missing or corrupt AAS data gracefully. | Error messages should be informative and non-intrusive. |
| **Compatibility** | The system shall remain fully compatible with the BaSyx infrastructure and standard AAS REST APIs. | Conformance to IDTA specifications. |
| **Security** | User authentication and session management must prevent unauthorized access. | Adhere to Eclipse Foundation security guidelines. |
| **Extensibility** | The architecture shall support future enhancements such as new filters or additional data types. | Use modular, component-based design. |

---

## 8. System Context and Interfaces

### 8.1 System Overview
The enhanced Mnestix Product Catalog operates as a **web-based frontend** that communicates with multiple **AAS repositories** and **BaSyx servers** using standardized REST APIs.  

**High-Level Architecture:**

+—————————+

|     User Interface        |

| (Mnestix Product Catalog) |

+———––+———––+

|

v

+———––+———––+

|   Application Layer       |

|  (Filtering, Sorting, UI) |

+———––+———––+

|

v

+———––+———––+

|  AAS Server / Repository  |

| (BaSyx, AASX, etc.)       |

+—————————+

### 8.2 Interfaces
- **AAS REST API**: For fetching AAS data and submodels.  
- **Nameplate Generator API**: For label creation from AAS data.  
- **Authentication API**: For user login status management.  

---

## 9. Constraints and Assumptions

### Constraints
- The system must remain open-source under the **Eclipse Public License (EPL)**.  
- All developments must align with the **Eclipse Mnestix architecture**.  
- Dependencies must be compatible with **modern browsers (Chrome, Firefox, Edge)**.  
- Development shall use the existing **Node.js + React** technology stack.

### Assumptions
- AAS repositories are accessible via stable network connections.  
- The user environment provides sufficient computational resources for asynchronous operations.  
- Future integration with external tools (e.g., Nameplate Generator) will use compatible API endpoints.

---

## 10. Acceptance Criteria

| ID | Description | Verification Method |
|----|--------------|----------------------|
| AC-01 | Login status is always visible in the header. | Manual UI Test |
| AC-02 | Repositories can be added, disabled, and viewed. | Functional Test |
| AC-03 | Product list supports filtering and sorting. | Integration Test |
| AC-04 | Nameplate Generator is accessible via the product view. | Functional Test |
| AC-05 | Non-blocking repository loading confirmed. | Performance Test |
| AC-06 | eShop features (cart, add/remove items) function as expected. | User Acceptance Test |
| AC-07 | System runs stably with multiple AAS servers. | System Test |

---

## 11. Glossary

| Term | Definition |
|------|-------------|
| **AAS (Asset Administration Shell)** | Digital representation of an industrial asset in the context of Industry 4.0. |
| **BaSyx** | Eclipse framework providing middleware for Industry 4.0 systems. |
| **IDTA** | Industrial Digital Twin Association — maintains AAS specifications. |
| **Repository** | A data source containing AAS objects. |
| **Nameplate Generator** | External service generating standardized digital nameplates for products. |
| **SM (Submodel)** | A specific subset of AAS data describing one aspect of an asset. |
| **Mnestix** | Open-source browser and visualization tool for AAS data. |

---

## 12. References
1. [Eclipse Mnestix Project](https://github.com/eclipse-mnestix/mnestix-browser)  
2. [AASX Package Explorer](https://github.com/eclipse-aaspe/package-explorer)  
3. [Eclipse BaSyx](https://basyx.org/get-started/introduction)  
4. [IDTA Specifications](https://industrialdigitaltwin.org/content-hub/downloads)  
5. Platform Industrie 4.0: *Details of the Asset Administration Shell, Part 1, Version 3* (2023)
