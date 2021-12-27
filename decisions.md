# Decisions

Decisions require a lot of energy to make, and if the reasoning for a decision is forgotten, we have to spend the energy again to find out why. Hence, a decision log.

## 1. Decision log

### Options

- One file per decision, like Architectural Decision Records
- One file for all decisions, one heading per decision.

### Decision

One file for all decisions, one heading per decision.

### Reasoning

Creating a file each time a decision is made, and referencing it, seems slightly labourious. If this single file becomes cumbersome we can refactor it into separate files at that time.

## 2. CSS Preprocessor

### Options
- Plain CSS
- Sass

### Decision

Plain CSS

### Reasoning

- Plain CSS allows the greatest number of potential contributors
- A preprocessor would mean running a task during development
- Because CSS is global, it makes sense to reason about it with a single file anyway.

### Consequences

- Organisation of so many parts in a single obsidian.css file is difficult.
- CSS variables are cumbersome to write.
- We miss out on interesting preprocessor features, such as mixins, functions, and simpler calculations.