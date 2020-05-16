![Preview](./imgs/gitsyn.jpeg)

# Git Configuring Remotes: on [Github](https://github.com/), [Gitlab](https://about.gitlab.com/), and [Bitbucket](https://bitbucket.org/product/)

This document helps you to know how to synchronize your repositories on Gitlab, Github, and Bitbucket together from one  single repository. This will Keep in synchronizing your Git repos on GitHub, GitLab & Bitbucket.

You can decide to use GitHub, which the most used solution this days, but maybe, just in case of long outages or because you don’t want to be tied to GitHub that much (for political reasons, or just because they had been acquired by Microsoft and you are afraid of the Skype syndrome), you may want to have not-read-only mirrors of your repos somewhere else.

Here is a nice trick to keep in sync real git repos on multiple places like GitLab and BitBucket, that you can pull and push to, without any efforts after a quick initial setup. Not read-only mirrors. Real repos. And this just be relying on git pull and push features.

# Git: pushing to and pulling from multiple remote locations: remote, url and pushurl

When pushing to or pulling from a remote `url` in git, the meaning of `--all` seems to be different between when `git push --all` is invoked and when calling `git pull --all`. Here’s my empirically obtained understanding of how you can configure git to push to and/or pull from multiple remote `urls`.

When `git push --all` is called, git will push all branches to the default remote. When invoking `git pull --all`, git will pull from the first url listed in all remotes.

## Pushing to multiple remote `urls`

If you want to push to multiple remote urls, you need only one remote containing multiple urls, and your `.git/config` should contain something like:

```bash
    [remote "Location1"]
      url   = git@url1.org/code.git
      url   = git@url2.org/code.git
      fetch = +refs/heads/*:refs/remotes/Location1/*
    [ branch "master"]
      remote  = Location1
      merge   = refs/heads/master
```
From the command line, this can be achieved by:

```bash
$> git remote add Location1 git@url1.org/code.git
$> git remote set-url --add Location1 git@url2.org/code.git
$> git push -vu Location1 master
```
and checked by:

```bash
$> git remote -v
Location1  git@url1.org/code.git (fetch)
Location1  git@url1.org/code.git (push)
Location1  git@url2.org/code.git (push)
```
Hence, when issuing `git push`, it will `push` to `url1` and `url2`, when doing `git pull`, the repository will be `pulled` (`fetched`) only from `url1`.

## Pulling from multiple remote `urls`
Since `git pull` will pull only from the first `url` in the `default remote`, and `git pull --all` will pull form the first url of all remotes, you will need to configure one `remote` per `url`:

```bash
    [remote "Location1"]
      url   = git@url1.org/code.git
      fetch = +refs/heads/*:refs/remotes/Location1/*
    [remote "Location2"]
      url   = git@url2.org/code.git
      fetch = +refs/heads/*:refs/remotes/Location2/*
    [ branch "master"]
      remote  = Location1
      merge   = refs/heads/master
```
This is configured by:

```bash
$> git remote add Location1 git@url1.org/code.git
$> git remote add Location2 git@url2.org/code.git
$> git push -vu Location1 master
```
Checking now gives:

```bash
$> git remote -v
Location1  git@url1.org/code.git (fetch)
Location1  git@url1.org/code.git (push)
Location2  git@url2.org/code.git (fetch)
Location2  git@url2.org/code.git (push)
```

which is misleading, since `git push` will not push to `url2`. Git will `pull` from `url1` and `url2` when issuing `git pull --all`, but only `push` to `url1`, since this is the **only** `remote` configured for the master branch (and only the last remote will be used if more than one is listed).

## Pushing to and pulling from multiple remote `urls`
To both push to and pull from multiple remote locations (either the same or different ones for `push` and `pull`) we need one remote per location, and the default remote must contain one `url` per location. The example for two identical `urls` is:

```bash
    [remote "Location1"]
      url   = git@url1.org/code.git
      url   = git@url2.org/code.git
      fetch = +refs/heads/*:refs/remotes/Location1/*
    [remote "Location2"]
      url   = git@url2.org/code.git
      fetch = +refs/heads/*:refs/remotes/Location2/*
    [ branch "master"]
      remote  = Location1
      merge   = refs/heads/master
```

This is configured by:

```bash
$> git remote add Location1 git@url1.org/code.git
$> git remote set-url --add Location1 git@url2.org/code.git
$> git remote add Location2 git@url2.org/code.git
$> git push -vu Location1 master
```

Checking now gives:

```bash
$> git remote -v
Location1  git@url1.org/code.git (fetch)
Location1  git@url1.org/code.git (push)
Location1  git@url2.org/code.git (push)
Location2  git@url2.org/code.git (fetch)
Location2  git@url2.org/code.git (push)
```

Therefore, `git push` will push to both `urls` in **Location1**, while `git pull --all` will pull from `url1` and `url2`, because they are the first ones listed in **Location1** and **Location2**.


# Getting Started with a more Practical Example
Depending on what you want or need, you will have multiple choice to configure your repo.

## `git push`
For a single main repo and simple “mirrors” and you are on the `github` repo, you can use this:
```bash
$> git remote set-url origin --add https://gitlab.com/${GIT_USER_NAME}/${GIT_REPO_NAME}.git
$> git remote set-url origin --add https://bitbucket.org/${GIT_USER_NAME}/${GIT_REPO_NAME}.git
```
You can check that the commands are ok with:

```bash
$> git remote -v
origin	https://github.com/YOU/YOUR-REPO.git (fetch)
origin	https://github.com/YOU/YOUR-REPO.git (push)
origin	https://gitlab.com/YOU/YOUR-REPO.git (push)
origin	https://bitbucket.org/YOU/YOUR-REPO.git (push)
```

Now you can just use git push and it will push on all remote :) .
**Note:** to enforce ssh instead of https here is a simple trick,

```bash
$> git config --global url.ssh://git@github.com/.insteadOf https://github.com/
$> git config --global url.ssh://git@gitlab.com/.insteadOf https://gitlab.com/
$> git config --global url.ssh://git@bitbucket.org/.insteadOf https://bitbucket.org/
```
Or you can add the `ssh` `url` directly in the previous `git remote set-url origin --add`.


## `git pull`
There is inconsitencies with `git push --all` (push all branches to default remote) and `git pull --all` (pull from the first url of the default remote).

we will have to add other remotes to be able to push.

```bash
$> git remote add origin-gitlab https://gitlab.com/${GIT_USER_NAME}/${GIT_REPO_NAME}.git
$> git remote add origin-bitbucket https://bitbucket.org/${GIT_USER_NAME}/${GIT_REPO_NAME}.git
```

You can double check the setup with this command again:

```bash
$> git remote -v
origin	ssh://git@github.com/YOU/YOUR-REPO.git (fetch)
origin	ssh://git@github.com/YOU/YOUR-REPO.git (push)
origin	ssh://git@gitlab.com/YOU/YOUR-REPO.git (push)
origin	ssh://git@bitbucket.org/YOU/YOUR-REPO.git (push)
origin-gitlab	ssh://git@gitlab.com/YOU/YOUR-REPO.git (fetch)
origin-gitlab	ssh://git@gitlab.com/YOU/YOUR-REPO.git (push)
origin-bitbucket	ssh://git@bitbucket.org/YOU/YOUR-REPO.git (fetch)
origin-bitbucket	ssh://git@bitbucket.org/YOU/YOUR-REPO.git (push)
```

Now you can use `git push` to push to all remotes and use `git pull --all` to pull from all remotes.

**Note** Do not forget to `merge` what you pulled in the new barnches e.g `origin-gitlab` or `origin-bitbucket` to the `origin\master` branch, by :

```bash
(master%)$> git pull --all
(master%)$> git merge [origin-gitlab|origin-bitbucket]
```

# More Resources and References
- [Keep in sync your Git repos on GitHub, GitLab & Bitbucket](https://moox.io/blog/keep-in-sync-git-repos-on-github-gitlab-bitbucket/)
- [pushing to and pulling from multiple remote locations](https://astrofloyd.wordpress.com/2015/05/05/git-pushing-to-and-pulling-from-multiple-remote-locations-remote-url-and-pushurl/)
- [The “fatal: refusing to merge unrelated histories” Git error](https://www.educative.io/edpresso/the-fatal-refusing-to-merge-unrelated-histories-git-error)
- [How To Push Git Branch To Remote](https://devconnected.com/how-to-push-git-branch-to-remote/)
- [How To Remove Files From Git Commit](https://devconnected.com/how-to-remove-files-from-git-commit/)
-[How to Synchronize Two Remote Git Repositories.](https://medium.com/@_oleksii_/how-to-synchronize-two-remote-git-repositories-e63b78892901)
-[How to keep two Git repositories in sync](https://www.opentechguides.com/how-to/article/git/177/git-sync-repos.html)
-[Keeping Local Repos in Sync With Open Source GitHub Repos](https://victorops.com/blog/keeping-local-repos-in-sync-with-open-source-github-repos)
-[Syncing repositories](https://backlog.com/git-tutorial/syncing-repositories/)
-[Working with Git remotes and pushing to multiple Git repositories](https://jigarius.com/blog/multiple-git-remote-repositories)
-[git syncing](https://www.atlassian.com/git/tutorials/syncing)






