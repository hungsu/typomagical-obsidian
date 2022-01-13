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

## 3. File watcher and mover

I need some form of file watcher to move CSS from this repo to my vault anyway during development. Doing this manually was causing significant errors, such as CRLF in my source control because I had copied back from my Windows machine. In general it was also becoming hard to track the difference between what was in source and what I was experimenting with in my Obsidian vault.
### Options

- Nothing - continue copy manually
- Grunt
- Sass
- Research more options

### Decision

Sass

### Reasoning

- The Sass builder already provides an option to copy files where I want. This means I also get Sass preprocessing.

### Consequences

- Outside developers must know Sass and have it installed to contribute.
- var intellisense no longer works
