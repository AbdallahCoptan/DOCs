```
		                    _____     _ _              _     _ _
		                   |  ___|_ _| | | _____  _ __| |   (_) |__
		                   | |_ / _` | | |/ / _ \| '__| |   | | '_ \
		                   |  _| (_| | |   < (_) | |  | |___| | |_) |
		                   |_|  \__,_|_|_|\_\___/|_|  |_____|_|_.__/

	 Installation Copyright @ 2020 Abdallah Ibrahim aka AbdallahCoptan <abdallah.cisco@gmail.com>

```

Falkor is a Common library to share Ruby code and {rake,cap} tasks.

* [Official Gem site](https://rubygems.org/gems/falkorlib)
* [GitHub Homepage](https://github.com/Falkor/falkorlib)

# Installing Falkor Library

In order to install the library in your machine, there are some pre-requisites are nedded to be installed before starting the main library installation.

## Pre-requisites 

You need to install first:

 1. the [ruby](https://linuxize.com/post/how-to-install-ruby-on-ubuntu-18-04/) development environment by:

 
 ```bash
 $> sudo apt update
 $> sudo apt-get install ruby-dev [ruby]
 $> sudo apt install ruby-full
 ```

To verify that the installation it was successful run the following command which will print the Ruby version:

```
 
 $> ruby --version


```

The output will look something like this:

```output

$> ruby 2.5.1p57 (2018-03-29 revision 63029) [x86_64-linux-gnu]

```



 2. The ruby [bundler](https://bundler.io/):

 Getting started with bundler is easy! In the terminal:

 ```

$> sudo apt-get install ruby-bundler 
$> sudo gem install bundler

 ```

 3. Initiate a `Gemfile` which will help you to install the dependencies, by:

 ``` 

 $> bundle init 

 ```

 4. Specify your dependencies in a [Gemfile](https://bundler.io/gemfile.html): 

 ```

# A sample Gemfile
source "https://rubygems.org"

# gem "rails"
gem 'falkorlib', '~> 0.8.6'

 ```

5. Install all of the required gems from your specified sources (installing the Flakor Lib):

``` 

$> bundle install 

``` 

or only 

``` 

$> bundle 

```



## Manually Installation 


Or install it yourself as:

``` 

$> sudo gem install falkorlib

```


To verify that the installation it was successful run the following command which will print the `falkor` libarary version:

``` 

$> falkor --version 

```

The output will look something like this:

```output

$> Falkor[Lib] version 0.8.6

```


# Falkor Usage


## Falkor lib Commands

Here it is a summary of the commands:

```
$> falkor
Falkor[Lib] commands:
  falkor --version, -V              # Print the version number
  falkor commands                   # Lists all available commands
  falkor config [option] [KEY]      # Print the current configuration of FalkorLib
  falkor gitcrypt <PATH> [options]  # Initialize git-crypt for the current repository
  falkor help [COMMAND]             # Describe available commands or one specific command
  falkor init <PATH> [options]      # Bootstrap a Git Repository
  falkor link <TYPE> [<path>]       # Initialize a special symlink in <path> (the current directory by default)
  falkor make <type> [<path>]       # Initialize one of Falkor's Makefile, typically bring as a symlink
  falkor mkdocs [options]           # Initialize mkdocs for the current project
  falkor motd <PATH> [options]      # Initiate a 'motd' file - message of the day
  falkor new <type> [<path>]        # Initialize the directory PATH with one of FalkorLib's template(s)
  falkor vagrant [options]          # Initialize vagrant for the current project

Options:
  -h, --help, [--help], [--no-help]  
  -v, [--verbose], [--no-verbose]    # Enable verbose output mode
          [--debug], [--no-debug]    # Enable debug output mode
  -n, [--dry-run], [--no-dry-run]    # Perform a trial run with (normally) no changes made

```

## Overview of the `falkor` CLI

This library comes with a CLI `falkor`, providing the following [sub] commands.

__Base commands__

| Command                            | Description                                                       |
|------------------------------------|-------------------------------------------------------------------|
| `falkor --version, -V`             | Print the version number of Falkor[Lib]                           |
| `falkor help [COMMAND]`            | Describe available commands or one specific command               |
| `falkor gitcrypt <PATH> [options]` | Initialize git-crypt for the current repository                   |
| `falkor init <PATH> [options]`     | Bootstrap a Git[flow] Repository                                  |
| `falkor mkdocs [options]`          | Initialize mkdocs for the current project                         |
| `falkor motd <PATH> [options]`     | Initiate a 'motd' file - message of the day                       |
| `falkor vagrant [options]`         | Initialize vagrant for the current project                        |

__`falkor link <type> [path]`__

Initialize a special symlink in `<path>` (the current directory by default)

| Command                         | Description                                                                                               |
|---------------------------------|-----------------------------------------------------------------------------------------------------------|
| `falkor link help [COMMAND]`    | Get help on the corresponding sub command                                                                 |
| `falkor link make [options]`    | Create a symlink to one of [Falkor's Makefile](https://github.com/Falkor/Makefiles), set as Git submodule |
| `falkor link rootdir [options]` | Create a symlink `.root` which targets the root of the repository                                         |

__`falkor new <stuff> [path]`__

Initialize the directory `<path>` (the current directory by default) with one of FalkorLib's template(s)

| Command                                 | Description                                                    |
|-----------------------------------------|----------------------------------------------------------------|
| `falkor new help [COMMAND]`             | Describe subcommands or one specific subcommand                |
| `falkor new article [options]`          | Bootstrap a LaTeX Article                                      |
| `falkor new letter [options]`           | LaTeX-based letter                                             |
| `falkor new license [options]`          | Generate an Open-Source License for your project               |
| `falkor new make [options]`             | Initiate one of Falkor's Makefile                              |
| `falkor new pyenv PATH [options]`       | Initialize pyenv/direnv                                        |
| `falkor new readme PATH [options]`      | Initiate a README file in the PATH directory ('./' by default) |
| `falkor new repo NAME [options]`        | Bootstrap a Git Repository                                     |
| `falkor new rvm PATH [options]`         | Initialize RVM                                                 |
| `falkor new slides [options]`           | Bootstrap LaTeX Beamer slides                                  |
| `falkor new trash PATH`                 | Add a Trash directory                                          |
| `falkor new versionfile PATH [options]` | initiate a VERSION file                                        |

__`falkor make <type> [path]`__

| Command                     | Description                                           |
|-----------------------------|-------------------------------------------------------|
| `falkor new help [COMMAND]` | Describe subcommands or one specific subcommand       |
| `falkor make generic`       | Symlink to Generic Makefile for sub directory         |
| `falkor make gnuplot`       | Symlink to a Makefile to compile GnuPlot scripts      |
| `falkor make latex`         | Symlink to a Makefile to compile LaTeX documents      |
| `falkor make repo`          | Create a root Makefile piloting repository operations |


A ZSH completion files is also maintained for this command, you'll find it in [`completion/_falkor`](completion/_falkor)

