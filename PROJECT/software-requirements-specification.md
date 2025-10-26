# Software Requirements Specification

This Software Requirements Specification (SRS) specifies the work of group 5.
The software and this secification was developed in connection with a university project.

**Author:** Gregor Gottschewski

**Date of last revision:** 26.09.2025

> Read the [IEEE Guide to Software Requirements Specifications](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=278253) or [IEEE Recommended Practice for Software Requirements Specifications](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=720574) before contributing to the SRS.

## Introduction

### Purpose

The purpose of this document is to define user interface extensions for the Mnestix Browser.

The following specification is written for the developer team and the customer.
Secondary readers include computer science students.  
Required for reading this specification is knowledge about the Mnestix Browser and its current features (as of 2025-10-03).

### Definitions and Acronyms

**_SRS_** is the acronym for Software Requirements Specification.  
**_The software_** refers to all software parts specified here.  
**_The developer team_** includes all developers and organizations listed [here](index#software-requirements-specification).  
**_Extensions_** are further developments of the already existing code base of the Mnestix Browser if not stated further.  
**_The customer_** is the supervising lecturer.  
**_UI_** is an acronym for user interface.  
**_Mnestix_** is a short form of Mnestix Browser.  
**_Power users_** are software users that spend a long time using the software.  
**_Regular users_** are software users that use the software sometimes.  
**_Guest_** is a user that is not registered at the Mnestix Browser instance.

This specification uses terms 'modern hardware' and 'stable connection to the backend' often.
The software was tested on a MacBook Pro 2024 (M4 Pro, 48 GB, macOS 15.7.1) with a local Mnestix Browser build.
All loading times etc. refer to this machine and environment.
Note that the repository size influences the loading time.
This software was tested with a 100 item repository.

### Scope

The name of the product specified here is _Project Bisasam_.
Project Bisasam refers only to the extensions specified later.
The name Mnestix is not affected and stays.

Project Bisasam extends the usability and functionality of Mnestix' catalogue feature.
These extensions affect the catalogue/repository dashboard, the product list, the product view and the menu bar.
Project Bisasam covers only the UI extensions specified in this SRS. It does not affect the Mnestix core system.
All changes strictly refer to the UI.

The goal of project Bisasam is to add additional UI features to increase the Mnestix user experience.

### References

* Features requests where made by our supervising lecturer and can be found at the [DHBW-TINF24F GitHub Organization (root/project-5)](https://github.com/DHBW-TINF24F/.github/blob/main/project5_mnestix_product_catalogue.md)
* The structure of this SRS follows the [ISO/IEC/IEEE 29148:2018 standard](https://ieeexplore.ieee.org/document/8559686)
* Information about Mnestix Browser can be found on [Mnestix-Browser GitHub](https://github.com/eclipse-mnestix/mnestix-browser)

### Overview

This SRS does not strictly follow ISO/IEC/IEEE standard 29148:2018.
Some parts of this SRS follow the older standard IEEE 830-1984 because [TODO: but why?]

## Overall description

### Product perspective

Project Bisasam extends the product catalog functionality of the [Mnestix Browser](https://github.com/eclipse-mnestix/mnestix-browser/).
The Mnestix Browser simplifies the implementation and visualization of the Asset Administration Shell (AAS).
The new features are implemented by direct modifications to the Mnestix code base.
All interfaces are integrated with existing Mnestix modules.

#### System interfaces

Communication between Mnestix Browser and Project Bisasam is handled internally.
These APIs are developed by the Mnestix developer team.
Bisasam uses the existing Next.js and TypeScript framework (like Mnestix itself) and does not modify the application architecture.
Project Bisasam requires no other services.

The new feature implementations follow a strict structure:

```mermaid
flowchart TD

A[Implementation structure] --> D[Implementation in Mnestix codebase]
D --> E[Integration with existing Modules]
E --> I[Documentation update]

subgraph Dev["Development process Bisasam"]
    D
    E
end

subgraph Mnestix["Mnestix Browser core"]
    J[Existing modules & APIs]
end

J <-->|Internal Interfaces| E
```

#### User interfaces

Bisasam enhances catalog management, repository configuration, and product visualization.  
All new UI elements are integrated into the existing Mnestix UI.

Users interact with project Bisasam's extension on all views.
Some extensions affect the repository configuration view and the catalog selection view.
The product view, responsible for listing all products, and the product detail view are part of project Bisasam's extensions.
These changes do not affect Mnestix' UI principles.

These changes follow Mnestix’s existing design principles.
All affected elements are configurable and/or selectable by the user.

#### Operations

Project Bisasam does not change administration behaviour.
Some new features add additional log messages to provide information.
These log messages are not specified and will only be added if necessarily need for development or administration.

### Product functions

The software adds new UI elements and features stated in section [User interfaces](#user-interfaces).
The following content adds additional, non UI-features, and refers to user interfaces.

To increase Mnestix Browser's performance, the code base of the product list should be improved.
Thumbnails should only load on the user's visible screen.
Additionally to performance improvements, the user experience should be increased.
These new features cover filtering, sorting and detailed product information.
Some features do not enhance existing features but add new features.
Part of this are eShop interactions and integration of an external nameplate generator.

### User characteristics

Mnestix Browser and the corresponding project Bisasam user group is diverse.

```mermaid
mindmap
    root((Mnestix Users))
        Administrator
            visits Mnestix every day
            spends a lot of time to add new digital twins
            needs fast interface
            manages big repositories
            tasks
                configure repositories
                approve new AAS entries
                manage user permissions
                monitor system performance
        Power User
            frequent product list access
            uses Nameplate Generator
            tasks
                maintain subsets of repositories
                filter and sort product lists
                validate product data
        Regular User
            uses product list
            uses shop frequently
            tasks
                browse catalog
                view product details
                add products to shopping cart
        Guest
            uses shop
            tasks
                view public product lists
                inspect product details
```

Four types of users uses Mnestix Browser: administrators, power users, regular users and guests.
All user groups benefit from project Bisasam's new features.
However, the focus should be the regular and power users as well as the administrator.
These user groups need fast and reliable features.

The cart and shop feature is the most critical part of project Bisasam.
It has to be acessable for every user group and should bring all relevant information about the selected products.

> See [limitations](#limitations) for more information about the shop.
> Project Bisasam assumes that guests are called upon to register before buying a product.

Project Bisasam does not change Mnestix' user management nor user rules/rights.

### Limitations

Project Bisasam covers a shop function with a chart.
It does not implement money transaction or other interfaces to buy a product.

### Assumptions and dependencies

* No second Mnestix Browser version is running at the same time
* No modifications of the core Mnestix Browser are allowed
* The Mnestix Browser fork of project Bisasam is installed correctly

## Specific requirements

### External interface requirements

### Performance requirements

### Software system attributes

#### Reliability

#### Availability

#### Security

#### Maintainability

In order to make the changes of project Bisasam maintainable, the developer team ships a documentation of code and functionality at project hand over.
This document should have two parts:

1. User Instructions
2. Technical Documentation

The user instructions must be written in a understandable way for all types of users defined in the chapter [user characteristics](#user-characteristics).
The technical documentation should cover an overview of project Bisasam written for developers.

To increase development maintainability, new project Bisasam functionalities have to be commented in a proper way.
Project Bisasam adopts official Mnestix' code specification and conventions.

See [Mnestix Code Conventions]() for more information.

### Usability requirements

The product list should load images in less than two seconds on modern hardware and a stable connection to the backend.
See [Definitions and Acronyms](#definitions-and-acronyms) for more information.

#### Functional partitioning

#### Functional description

#### Control description

### Environment characteristics