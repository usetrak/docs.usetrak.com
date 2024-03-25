---
title: Quick Start
description: Start here your journey with Trak
sidebar:
  order: 1
---

### A note about updates to this documentation

The documentation may undergo continuous changes since the project is under active development.
There isn't yet an automatic documentation creation pipeline—for now.
Any help is appreciated!

This page will be a moment behind what you can find in the [README on GitHub](https://github.com/lcfd/trak#readme).

## Installation

### Pypi

[On Pypi](https://pypi.org/project/trakcli/) you can find the package under the `trakcli` name.

You can install it with pip:

```bash
pip install trakcli
```

or with pipx:

```bash
pipx install trakcli
```

### Brew

TBA

### Try the code locally

If you want to try the latest unpublished changes you can install locally the code in the repository by using `Poetry` and `pipx`.

Run `poetry build` and then

```bash
# x.x.x = The version you have used to do the build.
pipx install ./dist/trakcli-x.x.x-py3-none-any.whl
```

to install `trak` using the wheel file.

## Usage

The package has the useful `--help` command that will explain all the commands.

The CLI will guide you anyway through what you should and must do with messages with specific messages.

### Basic commands

To start using you can use those basic commands.
They will create a project, run a session, get how is going, stop the session.

```bash
# Create a project
trak create project <project-id>

# Start a session for a project
trak start <project-id>

# Check how the session is going on
trak status

# Stop the session
trak stop
```

Start tracking a billable project:

`trak start pasta -b`

Start tracking a project on a specific category/topic:

`trak start pasta -c rigatoni`

### But there is a lot more than that

All the commands are described in the help command:

`trak --help`

## Starship

There is a dedicated command that ouputs clean strings for tools like Starship:

`trak status -s` or `trak status --starship`

To see the status in your terminal line open `$HOME/.config/starship.toml`
and put this snippet inside of it:

```bash
[custom.trak]
command = """ trak status -s """
when = "trak status"
shell = "sh"
```
