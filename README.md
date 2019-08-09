# vscode-nvda: Visual Studio Code project for the NVDA source repository

This repository contains a .vscode directory preconfigured for the [NVDA project repository](https://github.com/nvaccess/nvda]. In the NVDA repository, it is included as a submodule.

The following settings are configured in this project:

* Accessibility support is enabled
* Linting is enabled based on the Flake8 configuration bundled with the NVDA repository
* Auto complete extra paths are added for the several external submodules
* When saving a file, a final new line is added to it, and extra new lines are trimmed from the end of the file when applicable. This ensures a uniform style across the project
* De default indentation is set to use tabs instead of spaces
* Testing within Code is enabled using the unittest framework

## Python interpretter

The current NVDA build environment is set up in such a way that it doesn't require a virtual Python environment.
This VSCode project does not define the python interrpetter setting by default.
If you want to use the global python interpretter with this project, you are advised to set the interpretter in your user settings.
Note that, if you override the interpretter in your workspace settings, it will mark the `settings.json` file within this repository as dirthy, and might cause conflicts if this repository is ever updated.

## Linting

Linting is enabled based on the Flake8 configuration bundled with the NVDA repository