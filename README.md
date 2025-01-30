# vscode-nvda: Visual Studio Code project for the NVDA source repository

This repository contains a `.vscode` directory preconfigured for the [NVDA project repository](https://github.com/nvaccess/nvda).
It is included as a submodule in NVDA.

The following settings are configured in this project:

* Accessibility support is enabled
* Auto complete extra paths are added for the several external submodules
* When saving a file, a final new line is added to it, and extra new lines are trimmed from the end of the file when applicable. This ensures a uniform style across the project
* The default indentation is set to use tabs instead of spaces
* Testing within Code is enabled using the unittest framework

## Linting

Linting is enabled based on the Flake8 configuration bundled with the NVDA repository.
The NVDA repository contains several big modules, such as the gui.settingsDialogs module.
In order for linting to work throughout the complete file, the maximum number of problems has been increased from 100 to 10000.

## Python interpreter

The current NVDA build environment is set up in such a way that it doesn't require a virtual Python environment.
This VSCode project does not define the python interrpetter setting by default.
If you want to use the global python interpretter with this project, you are advised to set the interpretter in your user settings.
Note that, if you override the interpretter in your workspace settings, it will mark the `settings.json` file within this repository as dirthy, and might cause conflicts if this repository is ever updated.
