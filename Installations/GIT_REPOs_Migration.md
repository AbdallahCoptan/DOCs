<!-- ![Preview](./imgs/gitmig.jpg) ![Preview](./imgs/git_migration.jpeg) -->

<img src="./imgs/gitmig.jpg" width="440"/> <img src="./imgs/git_migration.jpeg" width="440"/> 

<!-- <img src="./imgs/git_migration.jpeg"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 50px; " /> -->



	          ____ ___ _____     __  __ ___ ____ ____      _  _____ ___ ___  _   _ 
	         / ___|_ _|_   _|   |  \/  |_ _/ ___|  _ \    / \|_   _|_ _/ _ \| \ | |
	        | |  _ | |  | |_____| |\/| || | |  _| |_) |  / _ \ | |  | | | | |  \| |
	        | |_| || |  | |_____| |  | || | |_| |  _ <  / ___ \| |  | | |_| | |\  |
	         \____|___| |_|     |_|  |_|___\____|_| \_\/_/   \_\_| |___\___/|_| \_|

		Copyright (c) 2020 Abdallah Ibrahim <abdallah.cisco@gmail.com>


# Git - Migrating Repositories from/to [Github](https://github.com/), [Gitlab](https://about.gitlab.com/), and [Bitbucket](https://bitbucket.org/product/)

## Migrating from Git cloud to another cloud
Some times Engineers and developers need to migrate their repositories (projects) form one git host to another (e.g. Github, Gitlab, and Bitbucket). They also need to keep their original copies and do mirroes for specific repositoris.
 

## Getting Started  with Simple Migration

Teh migration process is started by cloning the chosen repo as a mirror by includding the `--mirror` tag in the `git clone` command. Then, pushing this rep to the new destination (eitehr github, or gitlab).  The follwing steps show the process commands in detail.

### 1. Cloning as Mirror

Clone the repo from **[GitLab | Github | Bitbucket]** using the `--mirror` option:

```bash
$> git clone --mirror git@your-gitlab-site.com:aibrahim/my-repo.git
```

Then, Change into newly created repo directory, by:
```bash
$> cd ~/my-repo.git
```
### 2. Pushing to the other Cloud

Push to **[GitLab | Github | Bitbucket]** using the `--mirror` option.  The `--no-verify` option skips any hooks. Note, you should have a new repo with the same name on your new distination (for example on Github).

```bash
$> git push --no-verify --mirror git@github.com:AbdallahCoptan/my-repo.git
```
Now, you can check the new `--mirror` repo, you will find your files there!!
### 3. Setting up the Remote Push
You need to change the `remote push`, first check your remotes by `git remote -v`, you will get the follwoing two lines if the original repo was on Gitlab:

```bash
$> git remote -v
origin	ssh://git@your-gitlab-site.com:aibrahim/my-repo.git (fetch)
origin	ssh://git@your-gitlab-site.com:aibrahim/my-repo.git (push)
```
So you need to change the second line with the new remote which is for example the Github repo.
Set push URL to the mirror location for the new repository hosting `URL`, by:

```bash
$> git remote set-url --push origin git@github.com:AbdallahCoptan/my-repo.git
```

Then the remotes will be changed to:

```bash
$> git remote -v
origin	ssh://git@your-gitlab-site.com:aibrahim/my-repo.git (fetch)
origin	git@github.com:AbdallahCoptan/my-repo.git (push)
```


### 4. Updating the new Repo
To periodically update the repo on **[GitLab | Github | Bitbucket]** with what you have in **[GitLab | Github | Bitbucket]**, by:

```bash
$> git fetch -p origin
$> git push --no-verify --mirror
```

## Practical Examples for the Migration
This section shows some real exampels of the repo migration from **_Github_** to **_Gitlab_** and from **_Gitlab_** to **_Github_**. 

### 1. Migrating The `repo:test` from Gitlab to Github

I have a repo named `test` on my gitlab and I want to migrate it to the github, the follwoing should be applied:

**A.** You need to create a new repo with the same name `test` in Github.
**B.** Navigate through a terminal where you would like to clone the `--mirror`, and do the following:

```bash
$> git clone --mirror ssh://git@gitlab.uni.lu:8022/aibrahim/test.git
$> cd test.git
$> git push --no-verify --mirror git@github.com:AbdallahCoptan/test.git
$> git remote set-url --push origin git@github.com:AbdallahCoptan/test.git
```
**C.** In order to update the new repo on github, you need to `fetch` and `push` with the `--no-verify --mirror` options, as follows:

```bash
$> git fetch -p origin
$> git push --no-verify --mirror
```
**Note** There is another option to push from the original repository on the Gitlab by adding a new remote for pushing, to do so please check these links:
- [Keep in sync your Git repos on GitHub, GitLab & Bitbucket](https://moox.io/blog/keep-in-sync-git-repos-on-github-gitlab-bitbucket/)
- [Git: pushing to and pulling from multiple remote locations: remote, url and pushurl](https://astrofloyd.wordpress.com/2015/05/05/git-pushing-to-and-pulling-from-multiple-remote-locations-remote-url-and-pushurl/)

**D.** In order to pull the changes from the mirror, you need to mange your remotes on the main repo in your Gitlab, First you need to check your remots on the main repo, by:

```bash
$> git remote -v
origin	ssh://git@gitlab.uni.lu:8022/aibrahim/test.git (fetch)
origin	ssh://git@gitlab.uni.lu:8022/aibrahim/test.git (push)
```

We can add more remotes to push also by: 

```bash
$> git remote set-url origin --add git@github.com:AbdallahCoptan/test.git
$>
$> git remote -v
origin	ssh://git@gitlab.uni.lu:8022/aibrahim/test.git (fetch)
origin	ssh://git@gitlab.uni.lu:8022/aibrahim/test.git (push)
origin	git@github.com:AbdallahCoptan/test.git (push)
```
**Note:** There is inconsitencies with `git push --all` (push all branches to default remote) and `git pull --all` (pull from the first url of the default remote).

In order to add the remote pull, by:

```bash
$> git remote add origin-github git@github.com:AbdallahCoptan/migtest.git
$> 
$> git remote -v
origin	ssh://git@gitlab.uni.lu:8022/aibrahim/migtest.git (fetch)
origin	ssh://git@gitlab.uni.lu:8022/aibrahim/migtest.git (push)
origin	git@github.com:AbdallahCoptan/migtest.git (push)
origin-github	git@github.com:AbdallahCoptan/migtest.git (fetch)
origin-github	git@github.com:AbdallahCoptan/migtest.git (push)
```

In this case, when you want to pull,

```bash
$> git pull --all
Fetching origin
Fetching origin-github
From github.com:AbdallahCoptan/migtest
 * [new branch]      master     -> origin-github/master
Already up to date.
```

As you can see, the pulling from the mirror is going to a new branch which is named `origin-github/master`, so you need to merge it to the `master` branch to be up-to-date usually and push it , by:

```bash
$> git merge origin-github/master
$> git push --all
```

**For more information, please check [GIT Configuring remotes](https://github.com/AbdallahCoptan/DOCs/blob/master/Installations/GIT_Configuring_Remotes.md).**

### 2. Migrating The `repo:DOCs` from Github to Gitlab

**You need to follow the same instructions, by just switching between names and directions, this also can be used to migrate from or to Bitbucks!!**


-----------------------------------------------------------------------------------------------------------------------------------------------------------

# Migrating a Git Repository that has a [`git-lfs`](https://github.com/AbdallahCoptan/DOCs/blob/master/Installations/Git_LFS.md) Configurations

Migrating normal repositories between the git hosting clouds is not a very complicated task. However, the migration while a git repo containes a `git-lfs` files or configurations is much complicated and more confused. Therefore, migrating this kind of repos are usually prone to errors and misleading configurations and problems.

## [git-lfs-migrate](https://github.com/bozaro/git-lfs-migrate)
In order to migrate a repo with large file storage succesfully, you need to use command `git lfs migrate` to check the information about migration and to import the files extention you would like to include during the migration (which are the large files.) 

As you alraedy have the `git lfs` installed in your repo, you can check the [git-lfs-migrate(1) - Migrate history to or from git-lfs](https://github.com/git-lfs/git-lfs/blob/master/docs/man/git-lfs-migrate.1.ronn?utm_source=gitlfs_site&utm_medium=doc_man_migrate_link&utm_campaign=gitlfs) help, by issuing the following command:

```bash
$> git lfs migrate -h
git lfs migrate <mode> [options] "--" [branch ...]

Modes
-----

* info
    Show information about repository size.
  
* import
    Convert large Git objects to LFS pointers.
  
Options:

* -I <paths> --include=<paths>:
    See "Include and exclude".
  
* -X <paths> --exclude=<paths>:
    See "Include and exclude".
  
* --include-ref=<refname>:
    See [INCLUDE AND EXCLUDE (REFS)].
  
* --exclude-ref=<refname>:
    See [INCLUDE AND EXCLUDE (REFS)].
  
* --skip-fetch:
    Assumes that the known set of remote references is complete, and should not
    be refreshed when determining the set of "un-pushed" commits to migrate. Has
    no effect when combined with --include-ref or --exclude-ref.
  
* --everything:
    See [INCLUDE AND EXCLUDE (REFS)].
  
* [branch ...]:
    Migrate only the set of branches listed. If not given, git lfs migrate
    will migrate the currently checked out branch.
  
    References beginning with '^' will be excluded, whereas branches that do not
    begin with '^' will be included.
  
    If any of --include-ref or --exclude-ref are given, the checked out
    branch will not be appended, but branches given explicitly will be appended.
  
Info
----

The 'info' mode has these additional options:

* --above=<size>
    Only count files whose individual filesize is above the given size. 'size'
    may be specified as a number of bytes, or a number followed by a storage
    unit, e.g., "1b", "20 MB", "3 TiB", etc.
  
    If a set of files sharing a common extension has no files in that set whose
    individual size is above the given --above no files no entry for that set
    will be shown.
  
* --top=<n>
    Only include the top 'n' entries, ordered by how many total files match the
    given pathspec. Default: top 5 entries.
  
* --unit=<unit>
    Format the number of bytes in each entry as a quantity of the storage unit
    provided. Valid units include:
      * b, kib, mib, gib, tib, pib - for IEC storage units
      * b, kb, mb, gb, tb, pb - for SI storage units
  
    If a --unit is not specified, the largest unit that can fit the number of
    counted bytes as a whole number quantity is chosen.
  
Import
------

The 'import' mode migrates large objects present in the Git history to pointer
files tracked and stored with Git LFS. It supports all the core 'migrate'
options and these additional ones:

* --verbose
    Print the commit oid and filename of migrated files to STDOUT.
  
* --object-map=<path>
    Write to 'path' a file with the mapping of each rewritten commits. The file
    format is CSV with this pattern: OLD-SHA,NEW-SHA
  
* --no-rewrite
    Migrate large objects to Git LFS in a new commit without rewriting git
    history. Please note git lfs migrate -h
git lfs migrate <mode> [options] "--" [branch ...]

Modes
-----

* info
    Show information about repository size.
  
* import
    Convert large Git objects to LFS pointers.
  
Options:

* -I <paths> --include=<paths>:
    See "Include and exclude".
  
* -X <paths> --exclude=<paths>:
    See "Include and exclude".
  
* --include-ref=<refname>:
    See [INCLUDE AND EXCLUDE (REFS)].
  
* --exclude-ref=<refname>:
    See [INCLUDE AND EXCLUDE (REFS)].
  
* --skip-fetch:
    Assumes that the known set of remote references is complete, and should not
    be refreshed when determining the set of "un-pushed" commits to migrate. Has
    no effect when combined with --include-ref or --exclude-ref.
  
* --everything:
    See [INCLUDE AND EXCLUDE (REFS)].
  
* [branch ...]:
    Migrate only the set of branches listed. If not given, git lfs migrate
    will migrate the currently checked out branch.
  
    References beginning with '^' will be excluded, whereas branches that do not
    begin with '^' will be included.
  
    If any of --include-ref or --exclude-ref are given, the checked out
    branch will not be appended, but branches given explicitly will be appended.
  
Info
----

The 'info' mode has these additional options:

* --above=<size>
    Only count files whose individual filesize is above the given size. 'size'
    may be specified as a number of bytes, or a number followed by a storage
    unit, e.g., "1b", "20 MB", "3 TiB", etc.
  
    If a set of files sharing a common extension has no files in that set whose
    individual size is above the given --above no files no entry for that set
    will be shown.
  
* --top=<n>
    Only include the top 'n' entries, ordered by how many total files match the
    given pathspec. Default: top 5 entries.
  
* --unit=<unit>
    Format the number of bytes in each entry as a quantity of the storage unit
    provided. Valid units include:
      * b, kib, mib, gib, tib, pib - for IEC storage units
      * b, kb, mb, gb, tb, pb - for SI storage units
  
    If a --unit is not specified, the largest unit that can fit the number of
    counted bytes as a whole number quantity is chosen.
  
Import
------

The 'import' mode migrates large objects present in the Git history to pointer
files tracked and stored with Git LFS. It supports all the core 'migrate'
options and these additional ones:

* --verbose
    Print the commit oid and filename of migrated files to STDOUT.
  
* --object-map=<path>
    Write to 'path' a file with the mapping of each rewritten commits. The file
    format is CSV with this pattern: OLD-SHA,NEW-SHA
  
* --no-rewrite
    Migrate large objects to Git LFS in a new commit without rewriting git
    history. Please note that when this option is used, the migrate import
    command will expect a different argument list, specialized options will
    become available, and the core migrate options will be ignored. See
    [IMPORT (NO REWRITE)].
  
* --fixup
    Infer --include and --exclude filters on a per-commit basis based on the
    .gitattributes files in a repository. In practice, this option imports any
    filepaths which should be tracked by Git LFS according to the repository's
    .gitattributes file(s), but aren't already pointers. This option is
    incompatible with explicitly given --include, --exclude filters.
  
  If --no-rewrite is not provided and --include or --exclude (-I, -X,
  respectively) are given, the .gitattributes will be modified to include any new
  filepath patterns as given by those flags.
  
  If --no-rewrite is not provided and neither of those flags are given, the
  gitattributes will be incrementally modified to include new filepath extensions
  as they are rewritten in history.
  
Import 
-------

The import mode has a special sub-mode enabled by the --no-rewrite flag.
This sub-mode will migrate large objects to pointers as in the base import
mode, but will do so in a new commit without rewriting Git history. When using
this sub-mode, the base migrate options, such as --include-ref, will be
ignored, as will those for the base import mode. The migrate command will
also take a different argument list. As a result of these changes,
--no-rewrite will only operate on the current branch - any other interested
branches must have the generated commit merged in.

The --no-rewrite sub-mode supports the following options and arguments:

* -m <message> --message=<message>
    Specifies a commit message for the newly created commit.
  
* [file ...]
    The list of files to import. These files must be tracked by patterns
    specified in the gitattributes.
  
  If --message is given, the new commit will be created with the provided
  message. If no message is given, a commit message will be generated based on the
  file arguments.
  
Export
------

The 'export' mode migrates Git LFS pointer files present in the Git history out
of Git LFS, converting them into their corresponding object files. It supports
all the core 'migrate' options and these additional ones:

* --verbose
    Print the commit oid and filename of migrated files to STDOUT.
  
* --object-map=<path>
    Write to 'path' a file with the mapping of each rewritten commit. The file
    format is CSV with this pattern: OLD-SHA,NEW-SHA
  
* --remote=<git-remote>
    Download LFS objects from the provided 'git-remote' during the export. If
    not provided, defaults to 'origin'.
  
  The 'export' mode requires at minimum a pattern provided with the --include
  argument to specify which files to export. Files matching the --include
  patterns will be removed from Git LFS, while files matching the --exclude
  patterns will retain their Git LFS status. The export command will modify the
  .gitattributes to set/unset any filepath patterns as given by those flags.
  
Include and exclude
-------------------

You can configure Git LFS to only migrate tree entries whose pathspec matches
the include glob and does not match the exclude glob, to reduce total migration
time or to only migrate part of your repo. Specify multiple patterns using the
comma as the delimiter.

Pattern matching is done as given to be functionally equivalent to pattern
matching as in .gitattributes.

Include and exclude 
--------------------

You can configure Git LFS to only migrate commits reachable by references
include by --include-ref and not reachable by --exclude-ref.


        D---E---F
       /         \
  A---B------C    refs/heads/my-feature
   \          \
    \          refs/heads/master
     \
      refs/remotes/origin/master


In the above configuration, the following commits are reachable by each ref:


refs/heads/master:         C, B, A
refs/heads/my-feature:     F, E, D, B, A
refs/remote/origin/master: A


The following configuration:


  --include-ref=refs/heads/my-feature
  --include-ref=refs/heads/master
  --exclude-ref=refs/remotes/origin/master


Would, therefore, include commits: F, E, D, C, B, but exclude commit A.

The presence of flag --everything indicates that all local and remote
references should be migrated.

Examples
--------

Migrate unpushed commits
------------------------

The migrate command's most common use case is to convert large git objects to
LFS before pushing your commits. By default, it only scans commits that don't
exist on any remote, so long as the repository is non-bare.

First, run git lfs migrate info to list the file types taking up the most
space in your repository.


$ git lfs migrate info
migrate: Fetching remote refs: ..., done
migrate: Sorting commits: ..., done
migrate: Examining commits: 100% (1/1), done
*.mp3  	284 MB	  1/1 files(s)	100%
*.pdf  	42 MB 	  8/8 files(s)	100%
*.psd  	9.8 MB	15/15 files(s)	100%
*.ipynb	6.9 MB	  6/6 files(s)	100%
*.csv  	5.8 MB	  2/2 files(s)	100%
  
  
  Now, you can run git lfs migrate import to convert some file types to LFS:
  
  
  $ git lfs migrate import --include="*.mp3,*.psd"
  migrate: Fetching remote refs: ..., done
  migrate: Sorting commits: ..., done
  migrate: Rewriting commits: 100% (1/1), done
  master	d2b959babd099fe70da1c1512e2475e8a24de163 -> 136e706bf1ae79643915c134e17a6c933fd53c61
  migrate: Updating refs: ..., done
  
  
Migrate local history
---------------------

You can also migrate the entire history of your repository:


# Check for large files in your local master branch
$ git lfs migrate info --include-ref=master

# Check for large files in every branch
$ git lfs migrate info --everything


The same flags will work in import mode:


# Convert all zip files in your master branch
$ git lfs migrate import --include-ref=master --include="*.zip"

# Convert all zip files in every local branch
$ git lfs migrate import --everything --include="*.zip"


Note: This will require a force push to any existing Git remotes.

Migrate without rewriting local history
---------------------------------------

You can also migrate files without modifying the existing history of your
repository. Note that in the examples below, files in subdirectories are not
included because they are not explicitly specified.

Without a specified commit message:


$ git lfs migrate import --no-rewrite test.zip *.mp3 *.psd


With a specified commit message:


$ git lfs migrate import --no-rewrite \
  -m "Import test.zip, .mp3, .psd files in root of repo" \
  test.zip *.mp3 *.psd
that when this option is used, the migrate import
    command will expect a different argument list, specialized options will
    become available, and the core migrate options will be ignored. See
    [IMPORT (NO REWRITE)].
  
* --fixup
    Infer --include and --exclude filters on a per-commit basis based on the
    .gitattributes files in a repository. In practice, this option imports any
    filepaths which should be tracked by Git LFS according to the repository's
    .gitattributes file(s), but aren't already pointers. This option is
    incompatible with explicitly given --include, --exclude filters.
  
  If --no-rewrite is not provided and --include or --exclude (-I, -X,
  respectively) are given, the .gitattributes will be modified to include any new
  filepath patterns as given by those flags.
  
  If --no-rewrite is not provided and neither of those flags are given, the
  gitattributes will be incrementally modified to include new filepath extensions
  as they are rewritten in history.
  
Import 
-------

The import mode has a special sub-mode enabled by the --no-rewrite flag.
This sub-mode will migrate large objects to pointers as in the base import
mode, but will do so in a new commit without rewriting Git history. When using
this sub-mode, the base migrate options, such as --include-ref, will be
ignored, as will those for the base import mode. The migrate command will
also take a different argument list. As a result of these changes,
--no-rewrite will only operate on the current branch - any other interested
branches must have the generated commit merged in.

The --no-rewrite sub-mode supports the following options and arguments:

* -m <message> --message=<message>
    Specifies a commit message for the newly created commit.
  
* [file ...]
    The list of files to import. These files must be tracked by patterns
    specified in the gitattributes.
  
  If --message is given, the new commit will be created with the provided
  message. If no message is given, a commit message will be generated based on the
  file arguments.
  
Export
------

The 'export' mode migrates Git LFS pointer files present in the Git history out
of Git LFS, converting them into their corresponding object files. It supports
all the core 'migrate' options and these additional ones:

* --verbose
    Print the commit oid and filename of migrated files to STDOUT.
  
* --object-map=<path>
    Write to 'path' a file with the mapping of each rewritten commit. The file
    format is CSV with this pattern: OLD-SHA,NEW-SHA
  
* --remote=<git-remote>
    Download LFS objects from the provided 'git-remote' during the export. If
    not provided, defaults to 'origin'.
  
  The 'export' mode requires at minimum a pattern provided with the --include
  argument to specify which files to export. Files matching the --include
  patterns will be removed from Git LFS, while files matching the --exclude
  patterns will retain their Git LFS status. The export command will modify the
  .gitattributes to set/unset any filepath patterns as given by those flags.
  
Include and exclude
-------------------

You can configure Git LFS to only migrate tree entries whose pathspec matches
the include glob and does not match the exclude glob, to reduce total migration
time or to only migrate part of your repo. Specify multiple patterns using the
comma as the delimiter.

Pattern matching is done as given to be functionally equivalent to pattern
matching as in .gitattributes.

Include and exclude 
--------------------

You can configure Git LFS to only migrate commits reachable by references
include by --include-ref and not reachable by --exclude-ref.


        D---E---F
       /         \
  A---B------C    refs/heads/my-feature
   \          \
    \          refs/heads/master
     \
      refs/remotes/origin/master


In the above configuration, the following commits are reachable by each ref:


refs/heads/master:         C, B, A
refs/heads/my-feature:     F, E, D, B, A
refs/remote/origin/master: A


The following configuration:


  --include-ref=refs/heads/my-feature
  --include-ref=refs/heads/master
  --exclude-ref=refs/remotes/origin/master


Would, therefore, include commits: F, E, D, C, B, but exclude commit A.

The presence of flag --everything indicates that all local and remote
references should be migrated.

Examples
--------

Migrate unpushed commits
------------------------

The migrate command's most common use case is to convert large git objects to
LFS before pushing your commits. By default, it only scans commits that don't
exist on any remote, so long as the repository is non-bare.

First, run git lfs migrate info to list the file types taking up the most
space in your repository.


$ git lfs migrate info
migrate: Fetching remote refs: ..., done
migrate: Sorting commits: ..., done
migrate: Examining commits: 100% (1/1), done
*.mp3  	284 MB	  1/1 files(s)	100%
*.pdf  	42 MB 	  8/8 files(s)	100%
*.psd  	9.8 MB	15/15 files(s)	100%
*.ipynb	6.9 MB	  6/6 files(s)	100%
*.csv  	5.8 MB	  2/2 files(s)	100%
  
  
  Now, you can run git lfs migrate import to convert some file types to LFS:
  
  
  $ git lfs migrate import --include="*.mp3,*.psd"
  migrate: Fetching remote refs: ..., done
  migrate: Sorting commits: ..., done
  migrate: Rewriting commits: 100% (1/1), done
  master	d2b959babd099fe70da1c1512e2475e8a24de163 -> 136e706bf1ae79643915c134e17a6c933fd53c61
  migrate: Updating refs: ..., done
  
  
Migrate local history
---------------------

You can also migrate the entire history of your repository:


# Check for large files in your local master branch
$ git lfs migrate info --include-ref=master

# Check for large files in every branch
$ git lfs migrate info --everything


The same flags will work in import mode:


# Convert all zip files in your master branch
$ git lfs migrate import --include-ref=master --include="*.zip"

# Convert all zip files in every local branch
$ git lfs migrate import --everything --include="*.zip"


Note: This will require a force push to any existing Git remotes.

Migrate without rewriting local history
---------------------------------------

You can also migrate files without modifying the existing history of your
repository. Note that in the examples below, files in subdirectories are not
included because they are not explicitly specified.

Without a specified commit message:


$ git lfs migrate import --no-rewrite test.zip *.mp3 *.psd


With a specified commit message:


$ git lfs migrate import --no-rewrite \
  -m "Import test.zip, .mp3, .psd files in root of repo" \
  test.zip *.mp3 *.psd
```

## Getting Started with Migrating a Repository while Applying `lfs migrate`

The idea is ato do the follwing sequence:

1. Mirror clone locally the old repository eitehr on [gitlab or bitbucket]
2. `git lfs migrate` offending files
3. mirror push to Github `new` repository

### Let's apply this in a practical example

We have a repository named `test` also, but this time it has some files which are handeled by the `git lfs`. This repo is hosted on the Gitlab. We would like to migrate it to the Github. In order to do so, 

#### 1. Cloning with the `--mirror` option, where we desire

```bash
$> git clone --mirror ssh://git@gitlab.uni.lu:8022/aibrahim/test.git
$> cd test.git
```

#### 2. Applying the `lfs migration` for the big files (the tracked ones) 

```bash
$> git lfs migrate import --everything --verbose --include="*.wav,*.psd,*.tif, *.out"
```

#### 3. Cleanup unnecessary files and optimize the local repository

```bash
$> git reflog expire --expire-unreachable=now --all && git gc --prune=now --aggressive
```

**Optionally** add the following line in the `git config`:

```bash
$> git config lfs.https://gitlab.uni.lu/aibrahim/test.git/info/lfs.locksverify true
```

#### 4. Pushing into the new repo on Github
Please be sure, that there is a new reo with the same name on Github.

```bash
$> git push --mirror git@github.com:AbdallahCoptan/test.git
$> git push --mirror git@github.com:AbdallahCoptan/test.git <only first time>
```
Now you have the gitlab repo migrated to the github repo.

#### 5. Pulling from the original repo on Gitlab

```bash
$> git fetch -p origin
$> git lfs migrate import --everything --verbose --include="*.wav,*.psd,*.tif, *.out"
$> git reflog expire --expire-unreachable=now --all && git gc --prune=now --aggressive
```

#### 6. Finally, in order to `push` the new changes to the repo on Github

```bash
$> git remote set-url --push origin git@github.com:AbdallahCoptan/test.git <optinal>
$> git push --mirror
```

**Note** Configuring multiple remotes in the host repo, makes usually errors and problems. However you can do it also as in [Git Configuring remotes](https://github.com/AbdallahCoptan/DOCs/blob/master/Installations/GIT_Configuring_Remotes.md).
We advice you to just pull changes as the steps `5` and `6`.

In case you would like to configure multiple remotes on the main repo, you should consider the step `6` when ever you would like to push to the `--mirror` but just as follow:
```bash
$> git lfs migrate import --everything --verbose --include="*.out" <include only files tracked by LFS>
$> git reflog expire --expire-unreachable=now --all && git gc --prune=now --aggressive
$> git push <SSH for the remote ob GITHUB>
```

**The best practice for pushing and pulling** is as follow:

```
    1. push normally in the original repo
    2. pull changes in the --mirror repo
    3. It's better not to push to the --mirror, 
    4. otherwise you need to pull in a new branch and merge it, and this also may cause problems.
```

------------------------------------------------------------------------------------
# More Resources
- [git-lfs-migrate(1) - Migrate history to or from git-lfs](https://github.com/git-lfs/git-lfs/blob/master/docs/man/git-lfs-migrate.1.ronn?utm_source=gitlfs_site&utm_medium=doc_man_migrate_link&utm_campaign=gitlfs)
- [Migrating Repositories with Git LFS](http://gopalkri.com/2016/10/07/Migrating-Repositories-With-Git-Lfs/)
- [Not sure how to migrate a repository while applying lfs migrate](https://github.com/git-lfs/git-lfs/issues/3853)
- [How to Migrate from GitHub to GitLab](https://www.tecmint.com/migrate-from-github-to-gitlab/)
- [How to Migrate from GitHub to GitLab(video)](https://youtu.be/sHoeQ6S9N1k)
