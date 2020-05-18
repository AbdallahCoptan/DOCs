![By aibrahim](https://img.shields.io/badge/by-aibrahim-blue.svg) [![gitlab](https://img.shields.io/badge/git-gitlab-lightgray.svg)](https://gitlab.uni.lu/aibrahim/presence) [![Issues](https://img.shields.io/badge/issues-gitlab-green.svg)](https://gitlab.uni.lu/aibrahim/presence/issues)

       Time-stamp: <Fri 2020-05-15 01:07 abdallahcoptan>

                ____  ____  _____ ____  _____        ____ _____
               |  _ \|  _ \| ____/ ___|| ____|_ __  / ___| ____|
               | |_) | |_) |  _| \___ \|  _| | '_ \| |   |  _|
               |  __/|  _ <| |___ ___) | |___| | | | |___| |___
               |_|   |_| \_\_____|____/|_____|_| |_|\____|_____|

                   PeRformance Evaluation of SErvices on the Cloud
       Copyright (c) 2018 A. A.Z.A Ibrahim, <abdallah.cisco@gmail.com>

A Framework for Monitoring and Modelling the Performance Metrics of Mobile Cloud SaaS Web Services.
[PRESEnCE](https://github.com/AbdallahCoptan/presence) repository holds the sources of the prototype implementing the PRESEnCE framework for cloud performance monitoring.

In this file, we show how to install:
1. The repository it-self
2. The PRESEnCE Framework

# Repository Setup
After cloning the repo, either from gitlab or from github, you need to install the `Pyenv` & `Direnv`.

## Pyenv / Direnv
The repository make use of [pyenv](https://github.com/pyenv/pyenv), [virtualenv](https://virtualenv.pypa.io/en/stable/) and [direnv](https://direnv.net/) to offer a [sandboxed python environment](https://varrette.gforge.uni.lu/tutorials/pyenv.html).
See the following files:

* [`.python-version`](.python-version)
* [`.python-virtualenv`](.python-virtualenv)
* [`setup-direnv.sh`](setup-direnv.sh) / `.envrc`

Ensure you have followed [this tutorial](https://varrette.gforge.uni.lu/tutorials/pyenv.html), and in particular that you have install the [global `direnvrc`](https://github.com/Falkor/falkorlib/blob/devel/templates/direnv/direnvrc).

### Installing Pyenv
You can install `Pyenv` either manualy or by using the `Pyenv Installer`.
To install manually, use the [Simple Python Version Management: pyenv](https://github.com/pyenv/pyenv).
To install by using the `Pyenv Installer`, follow the follwoing steps:

#### 1. Installing the Prerequisites
Make sure to follow this guidance for your platform before any troubleshooting.
- Ubuntu/Debian:
 ```bash
 $> sudo apt-get install -y build-essential libssl-dev zlib1g-dev libbz2-dev \
    libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
    xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
```
Alternative of libreadline-dev:
```bash
 $> sudo apt install libedit-dev
```

For other systems please check the [Common build problems](https://github.com/pyenv/pyenv/wiki/Common-build-problems).

#### 2. `pyenv` Installation / Update
Once prerequisites have been installed correctly, use the [`pyenv installer`](https://github.com/pyenv/pyenv-installer) as follow:

```bash
    $> curl https://pyenv.run | bash
```

`pyenv.run` redirects to the install script in this repository and the invocation above is equivalent to:
```bash
    $> curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash
```
Restart your shell so the path changes take effect:
```bash
    $> exec $SHELL
```
You can now begin using `pyenv`.

**Note** try to be sure that the follwing two lines are in your `.bashrc` file:

```bash
    $> echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
    $> echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
```

### Installing `direnv` & `virtualenv`

In oder to install the `direnv`, please refere to [direnv](https://direnv.net/docs/installation.html) installation and for the [virtualenv](https://virtualenv.pypa.io/en/stable/) as well.

## Post-clone configuration

**`/!\ IMPORTANT`**: Once cloned, initiate your local copy of the repository by running:

```bash
    $> cd presence
    
    # Pyenv / Direnv setup
    $> direnv allow .
    $> pyenv install $(head .python-version)
    # [force] install virtualenv by re-entering the directory
    $> cd ..
    $> cd presence
    # Check that current virtualenv is correct
    $> echo $(basename $VIRTUAL_ENV)
```

**If** (and only if) you are in the appropriate virtualenv, you can install the missing packages and configure the repository:

```bash
    $> pip install -r requirements.txt
    $> make setup
```
he last command  will initiate the [Git submodules of this repository](.gitmodules) and setup the [git flow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) layout for this repository.

Later on, you can upgrade the [Git submodules](.gitmodules) to the latest version by running:

```bash
    $> make upgrade
```

If upon pulling the repository, you end in a state where another collaborator have upgraded the Git submodules for this repository, you'll end in a dirty state (as reported by modifications within the `.submodules/` directory). In that case, just after the pull, you **have to run** the following to ensure consistency with regards the Git submodules:

```bash
    $> make update
```

In case of any update of the repository and would like to upgarde, after the pulling from the repo:
```bash
    $> make up
    $> make setup    # include make setup-direnv 
```

Use make `setup-pyenv` to setup... `pyenv`, then you’ll probably need to delete the previous `pyenv-virtualenv` you were using (called `presence` ) created against `python 2.7.15` (an old version for example) using `pyenv virtualenv-delete 2.7.15/envs/presence`.

From this stage, you should direnv allow . the repository directory (to allow the `.envrc`) and re-enter the directory (`cd ..; cd -`) to create automatically the new `pyenv virtualenv`

Then check the current version of `python (should be 3.7.4)`, current `pip list` (should be nearly empty) and `reinstall` the missing dependencies by:
```bash
    $> pip install -r requirements.txt  (or use $> make setup-python)
```
----------------------------------------------

# PRESEnCE Framework Installation

In case you would like to install the framework directly without a `python virtual environment`, 
you should have `pip` and `python` installed, then you can do the follwoing:

## 1. Cloning the repository, where you want !
```bash
     $> git clone ssh://git@gitlab.uni.lu:8022/aibrahim/presence.git
     $> cd presence
```

## 2. Installing the requirements globally through `requirements.txt`
```bash
     $> pip install -r requirements.txt
     $> make setup
```

## 3. Install PRESEnCE
you should be sure that you are in the `presence` repo folder, which containes the `setup.py` file:

```bash
    $> pip install .
    $> sudo python setup.py build
    $> sudo python setup.py install
```

## 4. Checking the installation of PRESEnCE
Open a new terminal, and check if you have the following:

```bash
    $> cd
    $> presence  [or presence --help]
Usage: presence [OPTIONS] COMMAND [ARGS]...
        PRESENCE commandline interface.
        Select the sub-command to execute.
Options:
  -v, --version  Return the version of this script.
  --help         Show this message and exit.
Commands:
  campaign  Prints Presence's campaign test information.
  check     Prints Presence's check servers and tools information.
  config    Prints Presence's config information.
  create    Prints Presence's create command.
  run       Prints Presence's run test information.
  runup     Prints Presence's runUp servers information.
```
**OR**

```bash
    $> presence -v
    This is PRESENCE version 0.1.3
```

## 5. Updating the `click` files or the framework `cmd` configuration
After updating your files or adding more functionality, you can `push` the changes to the repo, and do (each time yu change anything):

```bash
    $> cd ~/presence
    $> sudo python setup.py build
    $> sudo python setup.py install
```

----------------------------------------


# More Resources

- [pyenv installer](https://github.com/pyenv/pyenv-installer)
- [rbenv installer & doctor scripts](https://github.com/rbenv/rbenv-installer)
- [Simple Python Version Management: pyenv](https://github.com/pyenv/pyenv)
- [Python Virtual Environment](https://github.com/AbdallahCoptan/DOCs/blob/master/Installations/pyVirtualEnv.md)
- [Installing packages using pip and virtual environments](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/)
- [venv — Creation of virtual environments](https://docs.python.org/3/library/venv.html#module-venv)
- [A Guide to Python’s Virtual Environments](https://towardsdatascience.com/virtual-environments-104c62d48c54)
- [Pipenv & Virtual Environments](https://docs.python-guide.org/dev/virtualenvs/)
- [Python Virtual Environment | Introduction](https://www.geeksforgeeks.org/python-virtual-environment/)
- [Python Virtual Environments: A Primer](https://realpython.com/python-virtual-environments-a-primer/)
- [virtualenvwrapper 5.0.1.dev2](https://virtualenvwrapper.readthedocs.io/en/latest//)
- [Configuring Python Environment With Virtualenvwrapper](https://medium.com/the-andela-way/configuring-python-environment-with-virtualenvwrapper-8745c2895745)
- [virtualenvwrapper 4.8.4 ](https://pypi.org/project/virtualenvwrapper/)
