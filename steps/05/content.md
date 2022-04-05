# Yaml syntax for steps

The steps are where the magic happens. They provide the interactive learning experience for users.

You can create steps that contain only text (boring!), or you can add interactivity with the included markdown extensions and have users run shell commands or code inside the containers.

There are currently three types of steps:

* Text
* Integrated terminals
* Code editors (WIP)

## Text-only steps

There's nothing special with these. You create the content by using Github flavored markdown.

Here's a sample configuration for a text-only step:

```yaml
title: Lab Folder Structure
layout:
  type: markdown
```

## Steps with integrated terminals

If you want to give your users an interactive learning experience, you can use terminals built into the steps. These terminals are connected to the containers that you've configured for each step and pass the shell commands to the attached container.

Terminals can also be launched in separate containers on different tabs so that users can work on multiple exercises simultaneously.

Here's a sample configuration for a step that launches multiple terminals:

```yaml
title: Packages & Imports
description: This step teaches you how to use packages
layout:
  allowNewTerminals: false
  defaultTerminals:
    - id: some-id
      allowClose: false
      cwd: /root
volumeTarget: /step1
scripts:
  shell: bash
```

## Steps with code editors

The steps can also provide code editors with Intellicode support so that users can create code and run it directly in the containers. This is a work in progress and we hope to complete work on this feature soon!
