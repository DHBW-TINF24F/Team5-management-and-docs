---
layout: default
title: Commit conventions
parent: Conventions
---

# Commit Conventions

All commits have to start with a preamble, followed by a short description and an optional reference to an issue or similar.
The syntax of a commit has to match:

```
<type>(<scope>): <short summary>

<reference to issue or other>
```

Mind the blank line!
Use the same preamble for all commits on a branch.
The simple rule of thumb: if the preamble doesn’t match prior preambles, then it doesn’t belong to the branch.
Example of a correct commit history:

```txt
feat(frontend/menubar): add user icon
feat(frontend/menubar): make user icon resizable
feat(frontend/menubar): add user menu
feat(frontend/menubar): remove legacy implementation
```

## Types

|Type|Description|
|-|-|
|feat|new feature|
|refactor|code change that neither fixes a bug or adds a feature|
|test|add or update test(s)|
|fix|a bug fix|
|docs|updating documentation|
|chore|build, config or dependency change|

## Scope

The scope is the affected part of the project by the change.
Subscopes are separated from parent scopes by using `/`.
Examples:

* `frontend/menubar`
* `database`
* `rest`

When updating the documentation, use the page you’re updating as scope, e.g.: `docs(team overview)`.

## Short summary

Use the summary field to provide a succinct description of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize the first letter
* no dot (.) at the end
