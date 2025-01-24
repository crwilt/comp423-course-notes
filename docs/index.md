# Welcome to Charles' Course Notes

This is my home page. I will use it to organize and share my course notes.

## Prerequisites
#### Before we dive in, make sure you have:

1. **A GitHub account:** If you don’t have one yet, sign up at [GitHub](https://github.com/).
2. **Git installed:** [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) if you don’t already have it.
3. **Visual Studio Code (VS Code):** Download and install it from [here](https://code.visualstudio.com/).
4. **Docker installed:** Required to run the dev container. [Get Docker here](https://www.docker.com/products/docker-desktop/).
5. **Command-line basics:** Your COMP211 command-line knowledge will serve you well here. If in doubt, review the Learn a CLI text!

## Step 1. Create a Local Directory and Initialize Git
(A) Open your terminal or command prompt.

(B) Create a new directory for your project. (Note: Of course, if you'd like to organize this tutorial somewhere else on your machine, go ahead and change into that parent directory first. By default this will be in your user's home directory.):


``` bash 
mkdir directory-for-go
cd directory for go
```

(C) Initialize a new Git repository:


``` bash 
git init
```
## Step 2. Add Development Container Configuration
1. In VS Code, open `directory-for-go`. You can do this via: File > Open Folder.
2.  the **Dev Containers** extension for VS Code.
3. Create a .devcontainer directory in the root of your project with the following file inside of this "hidden" configuration directory:`.devcontainer/devcontainer.json`