---
layout: default
title: Issue conventions
parent: Conventions
---

# Issue conventions

Title of issue follows this syntax: `<type>(<scope>): short description`.

## Types

Must be one of the following:

|Type|Description|
|-|-|
|`bug`|Report a problem in the software|
|`feature`|Request a new feature|
|`rework`|Request code refactoring|
|`docs`|Code documentation related|

The idea behind these types is that commit types are "answers" to issue types:

* `bug` - `fix`
* `feature` - `feat`
* `rework` - `refactor`

## Scope

The scope is optional if the scope isn't clear.
See [convention definitions](/conventions#definitions) for more information about scopes.

## Level

Set the level of the issue importance by setting the level label in GitHub.
Three levels exist:

* **Level 1 "Crucial":** Fundamental implementation or dangerous bug
* **Level 2 "Major":** Mandatory feature or bug
* **Level 3 "Minor":** Nice to have
