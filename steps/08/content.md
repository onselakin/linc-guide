# Mounting files into the container

Each step may contain files that you need to use during the interactive sessions. You can save these files under `/files` in each step.

This folder is automatically mounted as a volume inside the container under the name you specified in the step configuration:

```yaml
title: Packages & Imports
...
volumeTarget: /packages-and-imports
```

With the above configuration, the files in the `/files` folder are accessible from `/packages-and-imports` while the step is executed.