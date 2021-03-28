---
title: "auth status"
description: "View authentication status"
lead: "View authentication status."
date: 2021-03-16T08:43:34+01:00
lastmod: 2021-03-16T08:43:34+01:00
draft: false
images: []
menu:
  docs:
    parent: "commands"
weight: 200
toc: true
---

## Synopsis
Verifies and displays information about your authentication state.

This command tests the authentication states of all known GitLab instances in the config file and reports issues if any
```sh
glab auth status [flags]
```

## Options
```sh
-h, --hostname string   Check a specific instance's authentication status
-t, --show-token        Display the auth token
```
## Options inherited from parent commands
```
--help   Show help for command
```