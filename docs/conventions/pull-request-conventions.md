---
layout: default
title: Pull request conventions
parent: Conventions
---

# Pull Requests

Title of issue follows this syntax: `<type>(<scope>): short description`.

## Types

Must be one of the following:

|Type|Description|
|-|-|
|`feat`|new feature|
|`refactor`|code change that neither fixes a bug or adds a feature|
|`test`|add or update test(s)|
|`fix`|a bug fix|
|`docs`|updating documentation|
|`chore`|build, config or dependency change|

## Scope

See [convention definitions](/conventions#definitions) for more information about scopes.
Note that the scope is not optional.

## Body

The body of a pull request explains changes precisely. Give references if needed.

## Example

```
feat(frontend/menubar): rework menubar

change the menubar icon arrangement and add new settings-button.

fixes #1 and #2
```

## GitHub tags

Use GitHub tags when creating a new pull request.
Use the correct GitHub tag for your scope.
If a tag for your scope doesn’t exist, create a new tag.