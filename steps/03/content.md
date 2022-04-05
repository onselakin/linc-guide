# Virtual Lab Syntax & Configuration

To create virtual labs for LinC, you need to follow a certain folder structure.

## Lab Folder Structure

A virtual lab is basically a Github repository. So you can perform any Git operation while creating a virtual lab, and you can still update your virtual lab even if users add your lab to their list of local lab repositories.

When you update your lab, users following your lab will be notified and have the option to update their local copies. This is also very handy when you create your own virtual lab!

```text
.
├── lab.yaml                        Includes general information about the lab and configuration for the Docker images
├── front.md                        Cover content of the lab
├── back.md                         The content shown when the user completes the lab
└── scenarios/                      Includes a separate folder for each scenario
    ├── 01-first-scenario/
    │   ├── scenario.yaml           Defines the scenario
    │   └── steps/
    │       ├── 01/
    │       │   ├── step.yaml       Includes information about the step and the environment
    │       │   ├── content.md      The content for the step
    │       │   ├── init.sh         The script that will run before the user starts working on the step
    │       │   ├── verify.sh       The script that will run after the user completes the step
    │       │   └── files/          The files that would mounted as a volume into the step container
    │       │       └── ....
    │       └── 02
    └── 02-second-scenario/
        ├── scenario.yaml
        └── steps/
            └── ....
```

Sometimes it seems unnecessary to group content into scenarios (as in this case for the current lab, you see there are no scenarios, only steps). Therefore, it's possible to create labs that directly contain steps and skip scenarios altogether.

This is how the folder structure of a lab without scenarios would look like:

```text
.
├── lab.yaml
├── front.md
├── back.md
└── steps/
    ├── 01/
    │   ├── step.yaml
    │   └── content.md
    ├── 02/
    │   ├── step.yaml
    │   └── content.md
    ├── 03/
    │   ├── step.yaml
    │   └── content.md
    └── 04/
        ├── step.yaml
        └── content.md
```
