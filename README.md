<!--

    Copyright (c) 2019-present Sonatype, Inc. All rights reserved.
    Includes the third-party code listed at http://links.sonatype.com/products/clm/attributions.
    "Sonatype" is a trademark of Sonatype, Inc.

-->

# Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Development](#development)
- [Build/Deploy](#builddeploy)
- [Dependencies](#dependencies)

## Overview

**NOTE:** When modifying repo permissions, you will need to update
[this file](https://github.com/sonatype/github-admin/blob/master/exclusion.yml)
to prevent them reverting when admin tasks run.

This template codifies a number of useful practices for new repos at Sonatype.
Once you create a new project from this template:

- Click the "cog" icon and enter `Topics` to control IQ classification
- Update `.github/CODEOWNERS` with a pointer to your team, or anyone you want to review PRs 
- Go to `Settings` > `Branches` > `Branch protection rules` and add rules as needed
- Go to `Settings` > `Manage access` and invite teams or people you want to collaborate

It is suggested to invite the `Engineering` and `Ops` teams with `Write` access,
then enable `Branch protection` for your `main` branch with `Require pull request
reviews before merging` (select the number of reviews your team requires) and
`Require review from Code Owners`. This makes PR-driven cross-team collaboration
easy, and automatically keeps reviewers in the loop.

Add your team/project-specific contributing guidelines in `.github/CONTRIBUTING.md`.

Lastly, don't forget to HAVE FUN!

## Architecture

Architecture diagram.

High level overview.

## Development

How to make changes...

## Build/Deploy

How to deploy...

## Dependencies

Internal or external dependency links/docs...
