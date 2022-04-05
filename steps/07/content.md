# Initialization and verification scripts for steps

## Initializatin scripts

You can use initialization scripts to do some cleanup or prepare the step for the user's session. The initialization script is executed just before the step is initialized.

Verification scripts are run right after, when the user clicks the Next Step button. You can run some checks before the user proceeds to the next step, and enable or disable the transition.

This is especially useful when a step depends on the previous step.

### init.sh

This file contains the script used for initialization. If an error occurs when running the script or if you return an error code to the shell, the initialization will fail.

### verify.sh

This script contains the verification commands and is executed before the user proceeds to the next step. Again, if the script fails or an error code is returned, navigation fails and the user cannot continue.