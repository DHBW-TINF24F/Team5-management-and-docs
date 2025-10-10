---
layout: default
title: Overall Description
parent: Software Requirements Specification
---

<script src="https://cdn.jsdelivr.net/npm/mermaid@11.12.0/dist/mermaid.min.js"></script>

# Overall description

## Product perspective

Project Bisasam extends the product catalog functionality of the [Mnestix Browser](https://github.com/eclipse-mnestix/mnestix-browser/).
The Mnestix Browser simplifies the implementation and visualization of the Asset Administration Shell (AAS).
The new features are implemented by direct modifications to the Mnestix code base.
All interfaces are integrated with existing Mnestix modules.

### System interfaces

Communication between Mnestix Browser and Project Bisasam is handled internally.
These APIs are developed by the Mnestix developer team.
Bisasam uses the existing Next.js and TypeScript framework (like Mnestix itself) and does not modify the application architecture.
Project Bisasam requires no other services.

The new feature implementations follow a strict structure:

<pre class="mermaid">
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
</pre>

### User interfaces

Bisasam enhances catalog management, repository configuration, and product visualization.
All new UI elements are integrated into the existing Mnestix UI.

#### General

- **Login status:** Visible in the upper bar to inform users about their login state.

#### Repository configuration view

- **Configuration dialog:** Users can enable or disable individual AAS repositories and configure CD repositories.
- **Content display:** Allow inspection of CD repository contents.

#### Catalog selection view

- **Repository count:** Display the number of available products per repository.

#### Product list view

- **Filter and sort options:** Product lists can be filtered and sorted via query parameters.
- **Visible columns:** `ManufacturerName`, `ProductDesignation`, `OrderCode`, `ManufacturerCode`, `GlobalAssetId`, `CreatedAt`.
- **Sorting:** Entries in the product list can be sorted by column.

#### Product detail view

- **Nameplate generator integration (NGI):** NGI accessible from the product context menu.
- **Submodel visualization:** Linked AAS references are navigable and SM TechnicalData and HandoverDocumentation have improved formatting.
- **Shop functions:** Adds `addToCart` and `showCart` actions with small chart overview.

### Operations

Project Bisasam does not change administration bahaviour.
Some new features add additional log messages to provide information.
These log messages are not specified and will only be added if necessarily need for development or administration.

## Product functions

The software adds new UI elements and features stated in section [User interfaces](#user-interfaces).
The following content adds additional, non UI-features, and refers to user interfaces.

To increase Mnestix Browser's performance, the code base of the product list should be improved.
Thumbnails should only load on the user's visible screen.
Additionaly to performance improvements, the user experience should be increased.
These new features cover filtering, sorting and detailed product imformation
Some features do not enhance existing features but add new features.
Part of this are eShop interactions and integration of an external nameplate generator.

## User characteristics

Mnestix Browser and the correspodingly project Bisasam user group is diverse.

<pre class="mermaid">
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
</pre>

Four types of users uses Mnestix Browser: administrators, power users, regular users and guests.
All user groups benefit from project Bisasam's new features.
However, the focus should be the regular and power users as well as the administrator.
These user groups need fast and reliable features.

The cart and shop feature is the most critical part of project Bisasam.
It has to be acessable for every user group and should bring all relevant information about the selected products.

> See [limitations](#limitations) for more information about the shop.
> Project Bisasam assumes that guests are call uponed to register before buying a product.

Project Bisasam does not change Mnestix' user management nor user rules/rights.

## Limitations

Project Bisasam convers a shop function with a chart.
It does not implement money transaction or other interfaces to buy a product.

## Assumptions and dependencies

- No second Mnestix Browser version is running at the same time
- No modifications of the core Mnestix Browser are allowed
- The Mnestix Browser fork of project Bisasam is installed correctly