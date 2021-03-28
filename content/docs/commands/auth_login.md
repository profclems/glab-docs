---
title: "auth login"
description: "Authenticate with a GitLab instance"
lead: "Authenticate with a GitLab instance"
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
Authenticate with a GitLab instance. You can pass in a token on standard input by using –stdin. The minimum required scopes for the token are: “api”, “write_repository”.
```sh
glab auth login [flags]
```

## Examples
```sh
# start interactive setup
$ glab auth login
# authenticate against gitlab.com by reading the token from a file
$ glab auth login --stdin < myaccesstoken.txt
# authenticate with a self-hosted GitLab instance
$ glab auth login --hostname salsa.debian.org
```

## Options
```sh
-h, --hostname string   The hostname of the GitLab instance to authenticate with
    --stdin             Read token from standard input
-t, --token string      Your GitLab access token
```
## Options inherited from parent commands
```
--help   Show help for command
```