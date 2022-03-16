# sampler-box 101

In this section, we present some basic instruction to start developing code for `sampler-box`.

* [Development Tools](#Developer-Tools)
* sampler-box Project

## Developer Tools

Here we present the tools used for `sampler-box` development.

* [Operational System](#Operational-System)
* [Programming Language](#Programming-Language)
* [IDE](#IDE)

### Operational System

Linux id the operational system used to develop `sampler-box` tools. You can use any distribution you are familiar to start coding and testing `sampler-box`. Ubuntu is the preferred one. All instructions described in this document are applied to Ubuntu (or Debian like distro).

### Programming Language

`sampler-box` is being developed using Python version 3.8.x.

To install Python in your machine, run the following command:

```shell
$ sudo apt install python3 python3-dev python3-pip
```

#### Virtual Environment for Python - `virtualenvwrapper`

The tool `virtualenvwrapper` created virtual environments for Python development in your local machine. To install it, run the following commands:

```shell
$ sudo -H pip install virtualenvwrapper
$ export WORKON_HOME=~/.virtualenvs
$ mkdir -p $WORKON_HOME
```

When the installation process finishes, you should configure `BASH` to load the tool (dependencies) every time you log in or open a new terminal. Open the `.bashrc` file in an editor:

```shell
$ vim ~/.bashrc
```

And add the following lines at the end of the file:

```shell
export WORKON_HOME=~/.virtualenvs
export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
export VIRTUALENVWRAPPER_VIRTUALENV=/usr/local/bin/virtualenv
source /usr/local/bin/virtualenvwrapper.sh
```

After completing this step, restart your terminal instance and you will be ready to create a new virutal environment.

```shell
$ mkvirtualenv <env_name> --python=python3
```

You can check you are running into this new environment in the terminal:

```shell
(env_name) user@ubuntu:~/proj$
```

To exit the virtual environment:

```shell
(env_name) user@ubuntu:~/proj$ deactivate
```

To reload the environment created previously, call the command `workon` followed by the virtual environment name. You can also click on `tab` twice to autocomplete the virtual environment name.

```shell
$ workon <env_name>
```

### IDE

Currently, Visual Studio Code is used as IDE for `sampler-box` development.

Extensions to be installed:

* ms-python.python
* njpwerner.autodocstring

Once they are installed. Configure `VSCode`

1. Press `Ctrl + Shift + P` to and type `Python: Select Interpreter` and choose the one of virtual environment created.
