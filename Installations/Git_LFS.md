# Git - Large File Systems ([git-lfs](https://git-lfs.github.com/)): For [Github](https://github.com/), [Gitlab](https://about.gitlab.com/), and [Bitbucket](https://bitbucket.org/product/)

### An open source Git extension for versioning large files
Git Large File Storage (LFS) replaces large files such as audio samples, videos, datasets, and graphics with text pointers inside Git, while storing the file contents on a remote server like GitHub.com or GitHub Enterprise. [Git LFS](https://packagecloud.io/github/git-lfs) keeps a file pointer for the files greater than 100 Mb, and keep the source of theses files on the cloud. These pointers are refereing to the location for these files and once the repository is cloned, they are downloaded directly as normal.

## Installation 

### Requirements 
- `git >= 1.8.2`

### Installing
The details instructions for the instullation for different operating systems are listed in the `git-lfs` [wiki page on github](https://github.com/git-lfs/git-lfs/wiki/Installation) and the [packagecloud](https://packagecloud.io/github/git-lfs/install). You can also [download](https://github.com/git-lfs/git-lfs) the source of `git-lfs`. 

#### Debian and Ubuntu 
Ubuntu 18.04, Debian 10, and newer versions of those OSes offer a `git-lfs` package. If you'd like to use that and don't need the latest version, skip step 1 below.

```bash
$> curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash
$> sudo apt-get install git-lfs
$> git lfs install
```
#### Mac OSX

1. You may need to brew update to get all the new formulas
2. `brew install git-lfs`
3. `git lfs install`

#### Windows

1. Download the windows installer from [here](https://github.com/git-lfs/git-lfs/releases)
2. Run the windows installer
3. Start a command prompt/or git for windows prompt and run `git lfs install`


### Verify on the installtion

You can verify on the installation by checking the version of `git-lfs` and the `--help`:

```bash
$> git lfs -v
git-lfs/2.10.0 (GitHub; linux amd64; go 1.13.4)
```

**OR**

```bash
$> git lfs --help
GIT-LFS(1)
NAME
       git-lfs - Work with large files in Git repositories

SYNOPSIS
       git lfs command [args]

DESCRIPTION
       Git LFS is a system for managing and versioning large files in association with a Git repository. Instead of storing the large files within the Git repository as blobs, Git LFS stores special
       "pointer files" in the repository, while storing the actual file contents on a Git LFS server. The contents of the large file are downloaded automatically when needed, for example when a  Git
       branch containing the large file is checked out.

       Git  LFS  works by using a "smudge" filter to look up the large file contents based on the pointer file, and a "clean" filter to create a new version of the pointer file when the large file´s
       contents change. It also uses a pre-push hook to upload the large file contents to the Git LFS server whenever a commit containing a new large file version is about to be pushed to the corre‐
       sponding Git server.

COMMANDS
       Like Git, Git LFS commands are separated into high level ("porcelain") commands and low level ("plumbing") commands.

   High level commands (porcelain)
       git-lfs-env(1)
              Display the Git LFS environment.

       git-lfs-checkout(1)
              Populate working copy with real content from Git LFS files.

       git-lfs-fetch(1)
              Download Git LFS files from a remote.

       git-lfs-fsck(1)
              Check Git LFS files for consistency.

       git-lfs-install(1)
              Install Git LFS configuration.

       git-lfs-lock(1)
              Set a file as "locked" on the Git LFS server.

       git-lfs-locks(1)
              List currently "locked" files from the Git LFS server.

       git-lfs-logs(1)
              Show errors from the Git LFS command.

       git-lfs-ls-files(1)
              Show information about Git LFS files in the index and working tree.

       git-lfs-migrate(1)
              Migrate history to or from Git LFS

       git-lfs-prune(1)
              Delete old Git LFS files from local storage

       git-lfs-pull(1)
              Fetch Git LFS changes from the remote & checkout any required working tree files.

       git-lfs-push(1)
              Push queued large files to the Git LFS endpoint.
       git-lfs-status(1)
              Show the status of Git LFS files in the working tree.

       git-lfs-track(1)
              View or add Git LFS paths to Git attributes.

       git-lfs-uninstall(1)
              Uninstall Git LFS by removing hooks and smudge/clean filter configuration.

       git-lfs-unlock(1)
              Remove "locked" setting for a file on the Git LFS server.

       git-lfs-untrack(1)
              Remove Git LFS paths from Git Attributes.

       git-lfs-update(1)
              Update Git hooks for the current Git repository.

       git-lfs-version(1)
              Report the version number.

   Low level commands (plumbing)
       git-lfs-clean(1)
              Git clean filter that converts large files to pointers.

       git-lfs-pointer(1)
              Build and compare pointers.

       git-lfs-pre-push(1)
              Git pre-push hook implementation.

       git-lfs-filter-process(1)
              Git process filter that converts between large files and pointers.

       git-lfs-smudge(1)
              Git smudge filter that converts pointer in blobs to the actual content.
```

## Getting Started

On all operating systems, once `git-lfs` is downloaded, `git lfs install` must be run. Each user that intends to use git lfs must run this command, but they only ever need to run it once. `git-lfs` can be disabled by running `git lfs uninstall`, in which case that user would have to run `git lfs install` again, before `git-lfs` features work again.

Some users may wish to only enable git-lfs on specific repositories instead of always having it on for all of the repositories. Instead of running `git lfs install` and enabling `git-lfs` for that entire user, `git lfs install --local` can be used instead on a per repository basis.

**Note:** If `git-lfs` is installed without `--local`, then `git lfs uninstall --local` would not disable it for a specific repository.

An additional option of `--skip-smudge` can be added to skip automatic downloading of objects on `clone` or `pull`. This requires a manual `git lfs pull` every time a new commit is checked out on your repository. This is more useful for cases where you don't always want to download/checkout every large file.

You should start by the following steps:

1. Once downloaded and installed, set up `Git LFS` for your user account by running: 

```bash
$> git lfs install
```
You only need to run this once per user account.

2. In each Git repository where you want to use Git LFS, select the file types you'd like Git LFS to manage (or directly edit your `.gitattributes`). You can configure additional file extensions at anytime.

```bash
$> git lfs track "*.psd"
```
Now make sure .gitattributes is tracked:

```bash
$> git add .gitattributes
```

Note that defining the file types Git LFS should track will not, by itself, convert any pre-existing files to Git LFS, such as files on other branches or in your prior commit history. To do that, use the [`git lfs migrate[1]`](https://github.com/git-lfs/git-lfs/blob/master/docs/man/git-lfs-migrate.1.ronn?utm_source=gitlfs_site&utm_medium=doc_man_migrate_link&utm_campaign=gitlfs) command, which has a range of options designed to suit various potential use cases.


3. There is no step three. Just commit and push to GitHub as you normally would.

```bash
$> git add file.psd
$> git commit -m "Add design file"
$> git push origin master
```


### EXAMPLES
To get started with Git LFS, the following commands can be used.
1. Setup Git LFS on your system. You only have to do this once per repository per machine:

```bash
$> git lfs install
```

2. Choose the type of files you want to track, for examples all ISO images, with git-lfs-track(1):

```bash
$> git lfs track "*.iso"
```

3. The above stores this information in gitattributes(5) files, so that file need to be added to the repository:

```bash
$> git add .gitattributes 
```

4.  Commit, push and work with the files normally:

```bash
$> git add file.iso
$> git commit -m "Add disk image"
$> git push
```

### Git LFS [Documentation](https://github.com/git-lfs/git-lfs/tree/master/docs?utm_source=gitlfs_site&utm_medium=docs_link&utm_campaign=gitlfs)

#### Reference Manual

Each Git LFS subcommand is documented in the official [man pages](https://github.com/git-lfs/git-lfs/tree/master/docs/man). Any of these can also be viewed from the command line:

```bash
$> git lfs help <command>
$> git lfs <command> -h
```

#### Example

```bash
$> git lfs push -h
git lfs push [options] <remote> [<ref>...]
git lfs push <remote> [<ref>...]
git lfs push --object-id <remote> [<oid>...]

Upload Git LFS files to the configured endpoint for the current Git remote.  By
default, it filters out objects that are already referenced by the local clone
of the remote.

Options:

* --dry-run:
    Print the files that would be pushed, without actually pushing them.
  
* --all:
    This pushes all objects to the remote that are referenced by any commit
    reachable from the refs provided as arguments. If no refs are provided, then
    all refs are pushed.
  
* --object-id:
    This pushes only the object OIDs listed at the end of the command, separated
    by spaces.
```

#### Videos

- [How to Work with Big Files](https://www.youtube.com/watch?v=uLR1RNqJ1Mw) - Quick intro to Git LFS.

#### Developer Docs

- Details of how the Git LFS client works are in the [official specification](https://github.com/git-lfs/git-lfs/blob/master/docs/spec.md).

- Details of how the GIT LFS server works are in the [API specification](https://github.com/git-lfs/git-lfs/tree/master/docs/api).

## More resources

- [Handling Large Files with LFS](https://www.git-tower.com/learn/git/ebook/en/command-line/advanced-topics/git-lfs)
- [Git LFS Tutorial](https://github.com/git-lfs/git-lfs/wiki/Tutorial)

