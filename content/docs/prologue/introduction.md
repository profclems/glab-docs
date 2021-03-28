---
title: "Introduction"
description: "GLab is an open source GitLab CLI tool bringing GitLab to your terminal next to where you are already working with git and your code."
lead: "GLab is an open source GitLab CLI tool bringing GitLab to your terminal next to where you are already working with git and your code."
date: 2020-10-06T08:48:57+00:00
lastmod: 2020-10-06T08:48:57+00:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 100
toc: true
---

## Main features
* Expressive and intuitive syntax
* Interactive and beginner friendly
* Multiple instances authentication support
* Customizable and aliases support
* Formatted and colorized terminal output
* Linux, macOS and Windows support

## Installation
You can find installation instructions on our [README](https://github.com/profclems/glab#installation).

### Authentication
Run `glab` auth login to authenticate with your GitHub account. `glab` will respect tokens set using `GITLAB_TOKEN`.

### Self-Hosted Instances
`glab` supports all self-hosted instances. To authenticate with a self-hosted GitLab instance, run:

`glab` auth login --hostname <hostname>
You will be prompted to either authenticate using your browser, or to paste a token.

### Setting an editor
To set your preferred editor, you can use `glab` config set editor <editor>. Read more about `glab` config.

Additionally if the above is not set, for macOS and Linux, `glab` will respect editor environment variables based on your OS and shell setup.

On macOS and Linux, the default editor is Nano. On Windows, the default editor is Notepad.

### Setting your git protocol
To set your preferred git protocol, you can use `glab` config set git_protocol { ssh | https | http}. Read more about [`glab config`](/docs/commands/config).

### Disable interactivity
To disable interactive prompts, you can use `glab` config set prompt disabled. Read more about [`glab config`](/docs/commands/config).

### Extending the CLI
There are several ways you can make `glab` your own.

1. Create shorthands using `glab alias set`
1. Make custom API queries using `glab api`
1. Use environment variables

### Feedback
Thank you for checking out GitHub CLI! Please open an [issue](https://github.com/profclems/glab/issues/new) to send us feedback. We're looking forward to hearing it.
