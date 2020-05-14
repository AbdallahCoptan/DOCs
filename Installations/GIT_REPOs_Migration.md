![Preview](./imgs/git_migration.jpeg)

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

Push to **[GitLab | Github | Bitbucket]** using the `--mirror` option.  The `--no-verify` option skips any hooks. 

```bash
$> git push --no-verify --mirror git@github.com:AbdallahCoptan/my-repo.git
```

### 3. Setting up the Remote Push

Set push URL to the mirror location for the new repository hosting `URL`, by:

```bash
$> git remote set-url --push origin git@github.com:AbdallahCoptan/my-repo.git
```

### 4. Updating the new Repo
To periodically update the repo on **[GitLab | Github | Bitbucket]** with what you have in **[GitLab | Github | Bitbucket]**, by:

```bash
$> git fetch -p origin
$> git push --no-verify --mirror
```

