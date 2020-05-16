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

**For more information, please check [Configuring remotes](https://moox.io/blog/keep-in-sync-git-repos-on-github-gitlab-bitbucket/).**

### 2. Migrating The `repo:DOCs` from Github to Gitlab

**You need to follow the same instructions, by just switching between names and directions, this also can be used to migrate from or to Bitbucks!!**