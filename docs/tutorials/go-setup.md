# Setting up a dev container for Go

* Primary author: Charles Wilt (https://github.com/crwilt)
* Reviewer: James McNell (https://github.com/jamesbmc1)

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

Paste the following into `.devcontainer/devcontainer.json`:
``` bash 
{
  "name": "Go-time",
  "image": "mcr.microsoft.com/vscode/devcontainers/go",
  "customizations": {
    "vscode": {
      "settings": {},
      "extensions": ["golang.go"]
    }
}}
```
Reopen the project in the container by pressing `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac), typing "Dev Containers: Reopen in Container," and selecting the option. This may take a few minutes while the image is downloaded and the requirements are installed.


## Step 3: Using Your Container
Once your dev container setup completes, close the current terminal tab (trash can), open a new terminal pane within VSCode, and try running `go version` to see your dev container is running a recent version of Go without much effort! (go1.23.4 as of writing this)

Next run `go mod init hello-world` in order to create a mod file that tracks dependencies

Next make a file in the root directory called `main.go`. This will contain the code for your Hello, World! program. Once created paste the code below into it:
```go
package main

import "fmt"

func main() {
	fmt.Println("Hello, World!")
}
```
In order to actually run your program put `go run main.go` in the terminal. You should see the output of your Hello, World! program. 

An alternative way to run your program is by entering 
```bash
go build -o hello-world main.go
./hello-world```

!!! note "Distinction"
    Although both `go build` and `go run` both output Hello, World! They do very different things. `go build` creates an executable file with your go code, and needs `./hello world` to run it. `go run` compiles and runs the program in one step.