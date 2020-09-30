# MAAV Computer Vision Repository

## Contents

This repository containc Python files that will implement and test our computer
vision algorithms that we intend to use on our vehicle for Mission 9 of IARC.

While our code base is written in C++ primarily, we are composing our algorithms
in Python because the OpenCV library is available for both languages, and Python
allows an easy way to test code and import the OpenCV library while avoiding the
hassles that come with including OpenCV using CMake, ROS with catkin_ws, etc.

Additionally, this gives members of our team experience working with Python.

## Getting Started

This walkthrough was intended for either native Ubuntu / Linux, or Windows WSL2.
If you are running Mac, one significant change would be going from
`sudo apt-get install ...` to `brew install`. Please reach out if you encounter
other difficulties working on a Mac, or feel free to commit advice into this
README for Mac users based on your experience.

First, clone this repository. You can either use HTTPS or SSH with a key setup
through your account.
```
git clone <link>
cd maav-cv
```

Next, we recommend setting up a Python virtual environment to manage your
project dependencies so that you don't have 238 libraries installed in your
generic directories.
```
# Make sure python3 and python3-venv are installed
sudo apt-get update
sudo apt-get install python3 python3-venv python3-pip

# Verify you are in the correct folder
git status
  On branch master
  ...

# Setup the Virtual Environment
python3 -m venv env

# Source / Activate the Virtual Environment
source env/bin/activate
```

**NOTE: You MUST source the activate file everytime you begin any testing or
development!! That lets your terminal know what package install directory to
use for the code.**

We have included `requirements.txt` to install OpenCV and any other required
Python libraries. To install these requirements,
run the following command:
```
pip install -r requirements.txt
```

## Development Etiquette

**UPDATE 9/30/20: We will use forks for developing, and committing to this
official repo will happen through the website, where a pull request can be
created. The README will be updated with info on how to fork later.**

This section is subject to change throughout the course of development.
At times, Google can be your friend with Git, but reach out to us with
any help you may need!

When in doubt, [check out "Oh Shit! Git!"](https://ohshitgit.com) 

### Git Identity

Make sure your identity through Git is setup well.

```
# List current global config, which may contain identity info
git config --global -l
  user.name=Jacob Minock
  user.email=jaminock@umich.edu
  core.editor=vim
  ...

# Set or Change some things (for any repository you use)
# Omit --global to just make it for THIS repository
git config --global user.name "Jacob Minock"
git config --global user.email "jaminock@umich.edu"
```

### Git Branches

When developing a specific, new feature or set of changes, we suggest making
a branch for new files or the modifications of existing files. This will
allow your `master` branch to stay clean and organized in terms of commit
history and other qualities. Generally changes to the `master` branch only
happen with very small fixes - like updating a `README.md` or one doc.

```
# List branches
git branch

# Create a new branch
git checkout -b <branch>

# Switch to a branch
git checkout <branch>
```

### Git Repository Fork

TODO

## Appendix A: Helpful Resources and Links

OpenCV in Python Tutorials Page:

https://docs.opencv.org/master/dc/d4d/tutorial_py_table_of_contents_gui.html

Intel RealSense Python Wrapper Docs:

https://github.com/IntelRealSense/librealsense/tree/master/wrappers/python