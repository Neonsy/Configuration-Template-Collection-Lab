# Project-Config-Template

Welcome to the Project-Config-Template repository. This repository is a collection of configuration templates intended for use in future projects. It serves as a testing ground to ensure configurations are ready and optimized for production use.

## Table of Contents

- [Project-Config-Template](#project-config-template)
  - [Table of Contents](#table-of-contents)
  - [Required Labels](#required-labels)
  - [Dependabot](#dependabot)
  - [Workflows](#workflows)
    - [General-CI](#general-ci)
      - [Permissions](#permissions)
      - [Steps](#steps)

## Required Labels

- composer: A package manager for PHP projects
- dependabot: This PR has been created by dependabot
- dependencies: Has something to do with dependencies
- nodejs: NodeJS related stuff
- php: PHP related stuff
- prettier-error: Prettier check has failed on file changes
- prettier-auto-fix: Prettier write got automatically triggered

## Dependabot

This section contains example configurations for managing dependencies using Dependabot. Supported package managers include:

- **NPM / PHP**

Key configuration features:

- **Schedule**
  - Weekly updates (Can be manually triggered [here](https://github.com/Neonsy/Configuration-Template-Collection-Lab/network/dependencies))
  - Time and timezone settings
- **Assignees**
- **Labels**
- **Versioning strategy**
- **Target branch**
- **Groups**
  - Group-specific settings:
    - Dependency type
    - Pattern matching for dependencies (e.g., `*dependencyName*`)

## Workflows

### General-CI

![CI Workflow](https://github.com/Neonsy/Configuration-Template-Collection-Lab/actions/workflows/general-ci.yml/badge.svg)

This workflow manages pull requests created by Dependabot. It triggers on changes made by Dependabot or [Me :)](https://github.com/Neonsy).

#### Permissions

- **contents**: `write`

- **issues**: `write`

- **pull-requests**: `write`

#### Steps

1. **Checkout the repository**

2. **Setup PNPM**

3. **Install Node.js**

4. **Install dependencies**

5. **Run format:check** (Prettier check script)

6. **Add label(s) when Prettier check fails**

7. **Remove label(s) when Prettier check succeeds**

8. **Run format:fix if needed**

9. **Check for changes made by the workflow**

10. **Commit and push changes (if there are any)**
