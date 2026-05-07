# Student Guide

## Installing Pixi 
Pixi is a package management tool for Python that we will use throughout the bonus point assignments. It is used to install the required libraries and tools for the assignments. You can imagine it as a more powerful version of `pip` or `conda`, should you be familiar with those. To install Pixi, please follow the instructions on the official Pixi website:

1. Navigate to https://pixi.prefix.dev/latest/installation/
2. Ensure that you install the version for the operating system that you are using

**Note:** on Windows, you might be required to enable the execution of PowerShell scripts. To do so, run the following command in a PowerShell terminal:
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

## Creating a Pixi environment for the assignment
Once you have downloaded pixi, open a terminal in the root directory that contains all the assignment files - specifically, the `pixi.toml` and `pixi.lock` files - and run the following command:

```bash
pixi install --frozen
```

This will create a new Python environment with all the required dependencies. The `--frozen` flag ensures that the exact versions of the dependencies specified in `pixi.lock` are installed, which allows you to reproduce the same environment that will be used for grading later on.

## Activating the Pixi environment
To activate the Pixi environment, run the following command in the terminal:

```bash
pixi shell
```

You should see the name of the environment in your terminal prompt, indicating that you are now working within the Pixi environment.
```bash
(pixi-env) $
```

You can now run Python commands and JupyterLab within this environment, and it will have access to all the libraries and tools that were installed with `pixi install`:

```bash
(pixi-env) $ python --version
Python 3.x.x
```

## Starting JupyterLab
To start JupyterLab, run the following command in the terminal while the Pixi environment is activated:

```bash
jupyter lab
```

This will open JupyterLab in your default web browser. You can navigate to the folder containing the assignment notebooks and start working on them.

## Troubleshooting
We do our best to accommodate different operating systems and setups, but if you encounter any issues during installation or while working on the assignments, please don't hesitate to reach out to the course staff through the bonus point assignment Moodle forum.