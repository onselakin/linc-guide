# What is a Virtual Lab?

A virtual lab is simply a combination of Markdown and some Docker container configurations.

As a lab creator, you're responsible for defining the interaction between the content (markdown) and the code / instructions that get executed inside the containers.

Before you go any further, I recommend you take a look at the virtual lab [here](https://github.com/onselakin/linc-guide).

## Scenarios

Each virtual lab consists of one or more scenarios. You can think of the scenarios like chapters in a book. So they only serve to group related concepts together, nothing more.

## Steps

Each scenario involves one or more steps. It's in the steps that the exciting things happen.

The steps can either be simple Markdown content that users read at will, or they can be interactive and allow users to execute commands, create and compile code, or manage a Kubernetes cluster.

Since each step can be configured to run in containers, you can do just about anything with them.