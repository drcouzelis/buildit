# BuildIt

After configuring your project to use GNU Autotools, these scripts assist with building and running your software project in a development environment.

## Setup

Copy the "buildit.conf.EXAMPLE" file to "buildit.conf" and make any needed change (for example, set the name / path of the project you will be building). A "setup" script is included to create symlinks in the current directory, if desired.

## Scripts

### build

Build the project. I use this one a lot!

### run

Run the application. I also use this one a lot. If the project isn't built or has been modified, this will automatically rebuild it before running.

### debug

Will run the application through the debugger (GDB).

### wipe

Delete all extra files used by both BuildIt and GNU Autotools. This is designed to err on the side of caution and be as safe as possible (it won't delete anything you don't want deleted). Depending on the situation, this can sometimes leave some unwanted files / directories left in your build area, so double check it if necessary.

### clean

Delete all temporary build files. This is very safe to use, but is not usually necessary.

### refresh

Wipe the build area and get it ready to be used again. This is not usually necessary to use.

## Configuration

The "buildit.conf" file is read from the same directory that these build scripts are it. It is responsible for providing these variables:

### BUILDIT_project

The name of the project executable.

### BUILDIT_project_path

Path to the project (where the "configure.ac" file is located).

### BUILDIT_workarea_path

Path to where the project work area, where it will be built and installed. This directory will be created if it doesn't exist.
