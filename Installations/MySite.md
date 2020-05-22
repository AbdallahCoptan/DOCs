[![By abdallahcoptan](https://img.shields.io/badge/by-AbdallahCoptan-blue)](https://abdallahCoptan.github.io) [![git](https://img.shields.io/badge/git-github-lightgrey)](https://github.com/AbdallahCoptan) ![licence](https://img.shields.io/badge/license-Apache-brightgreen)


       Time-stamp: <Fri 2020-05-15 01:07 abdallahcoptan>

          _    _         _       _ _       _      ____            _              
         / \  | |__   __| | __ _| | | __ _| |__  / ___|___  _ __ | |_ __ _ _ __  
        / _ \ | '_ \ / _` |/ _` | | |/ _` | '_ \| |   / _ \| '_ \| __/ _` | '_ \ 
       / ___ \| |_) | (_| | (_| | | | (_| | | | | |__| (_) | |_) | || (_| | | | |
      /_/   \_\_.__/ \__,_|\__,_|_|_|\__,_|_| |_|\____\___/| .__/ \__\__,_|_| |_|
                                                           |_|                   
              My personal website (https://abdallahCoptan.github.io) 
           Copyright (c) 2018 A. A.Z.A Ibrahim, <abdallah.cisco@gmail.com>                                                           



# **Setup your personal page on Github Pages**

## Install

You should have a new git repo (exactly on your acountname.github.io):
 - do it on github.com, then
 - clone it:

```sh
$> git clone <your git repo directory>.<acountname.github.io>
```

Make sure that you have the `npm` installed:
Check this [link](https://www.devroom.io/2011/10/24/installing-node-js-and-npm-on-ubuntu-debian/) for installing the last version of Nodejs and NPM, Or check the page locally [here](https://github.com/AbdallahCoptan/abdallahcoptan.github.io/blob/develop/nomInstall.md).

```sh
$> sudo apt-get install npm
```

Make sure that you have the Gatsby CLI program installed:

```sh
$> npm install --global gatsby-cli
```
And run from your CLI:

```sh
$> gatsby new <acountname.github.io> https://github.com/anubhavsrivastava/gatsby-starter-resume
```

Then you can run it by:

```sh
$> cd <acountname.github.io>
$> npm install
```

## Personalization & editing files

Edit `config.js` to put up your details

```javascript
module.exports = {
  siteTitle: 'Abdallah Ibrahim Resume', // <title>
  ...
  pathPrefix: `/`,
  firstName: 'Abdallah',
  lastName: 'Ibrahim',
  // social
  socialLinks: [
    {
      icon: 'fa-github',
      name: 'Github',
      url: 'https://github.com/abdallahcoptan',
    }
    ...
  ],
};
```

**Do Not forget** to change the path prefix to root folder:

The template should be in the directory 'root' on your repository.

```
pathPrefix: `/`,
```

### Cleaning the repository by:

```sh
$> npm run clean
```


## Adding a develop branch

Adding a new branch for development because you need to make your `index.html` file on the master branch. 
This is will let the website got published on the personal github page of your repo.  

Issuing a new branch by

```sh
$> git checkout -b develop
```
**All the development should be on the develop branch, and the master will not be touched anymore**

Updating the `package.json` file by adding a new *script* on "scripts" section:

```
"deploymaster": "npm run clean && gatsby build --prefix-paths && gh-pages -d public -b master",
```


### Starting the development:

```sh
$> gatsby develop
```

## Push changes to the git [optional]

```sh
$> git push -u origin develop
```

## Building your website

This will let your website is ready for publishing, to do so by:

```sh
$> gatsby build [or] npm run build
```

### Publishing on the github personal pages

In order to publish the website on the github pages:

```sh
$> npm run deploymaster
```

The final index.html file will be on the master branch and with this you can access the website by:

[https://abdallahcoptan.github.io/](https://abdallahcoptan.github.io/)

# Note

In case you will add a new device for deployment, you should have a .gitignore file, this file should have the folllowing:

```
# Project dependencies
.cache
node_modules
yarn-error.log
package-lock.json
yarn.lock

# Build directory
/public
.DS_Store

```
This will ignore all the `npm install` files and the `.cache` files.  

# **Adding New Devices for Development** 

Now, your website is already online, and you want to add a new device or a new `developer` to start developing and `push` to the main repository.

## 1. Start by installing the `npm` and `nodejs`
Please, consider visiting `npm` [installation](https://github.com/AbdallahCoptan/DOCs/blob/master/Installations/Npm_and_NodeJS.md).

## 2. Verify on the `npm` and `nodejs` installation

```sh
$> npm -v
6.14.5
$> node -v
v14.3.0
```

## 3. Installing the `gatsby` Framework
This by using the `npm` to install the `gatsby-cli`, and it shoukld be `--globally`, like:

```sh
$> sudo npm install --global gatsby-cli
```
In order to check the installation, try:

```sh
$> sudo gatsby -h
Usage: gatsby <command> [options]
Commands:
  gatsby develop                   Start development server. Watches files, rebuilds, and hot reloads if something changes
  gatsby build                     Build a Gatsby project.
  gatsby serve                     Serve previously built Gatsby site.
  gatsby info                      Get environment information for debugging and issue reporting
  gatsby clean                     Wipe the local gatsby environment including built assets and cache
  gatsby repl                      Get a node repl with context of Gatsby environment, see (https://www.gatsbyjs.org/docs/gatsby-repl/)
  gatsby recipes [recipe]          [EXPERIMENTAL] Run a recipe
  gatsby new [rootPath] [starter]  Create new Gatsby project.
  gatsby plugin                    Useful commands relating to Gatsby plugins
  gatsby telemetry                 Enable or disable Gatsby anonymous analytics collection.

Options:
  --verbose                Turn on verbose output       [boolean] [default: false]
  --no-color, --no-colors  Turn off the color in output [boolean] [default: false]
  --json                   Turn on the JSON logger      [boolean] [default: false]
  -h, --help               Show help                    [boolean]
  -v, --version            Show the version of the Gatsby CLI and the Gatsby package in the current project  [boolean]
```

## 4. Using `git` to `clone with https` the source code of your site
In the directory you would like to clone the project (you have to clone `https`), do:

```sh
$> git clone https://github.com/AbdallahCoptan/abdallahcoptan.github.io.git
$> cd abdallahcoptan.github.io/
```
please check the global git configuration file `nano ~/.gitconfig`, and be sure that you can clone with `https` and `ssh` together in the same time.
After cloning, Check the remotes to be sure, by (it has to be like this):

```sh
$> git remote -v
origin	https://github.com/AbdallahCoptan/abdallahcoptan.github.io.git (fetch)
origin	https://github.com/AbdallahCoptan/abdallahcoptan.github.io.git (push)
```

## 5. Check the `develop` branch
To checkout to other branches in the `master` branch, use:

```sh
$> git checkout
develop          HEAD             master           origin/develop   origin/HEAD      origin/master
$> git checkout develop 
Branch 'develop' set up to track remote branch 'develop' from 'origin'.
Switched to a new branch 'develop'
```
The `develop` branch is the development branch which you shoukd use usually for developing and all the `push` operations have only to be processed here, and **do not touch the `master` branch**.

## 6. Installing the Website locally
This step will allow you to develop locally first and pushing the finals later on, so to install by using the `npm` inside the repo in the `develop` branch:

```sh
$> sudo npm install
```
In order to fix any valurnabilities use:
```sh
$> sudo npm audit fix
```
After installing you will find a folder named `node_modules` which containes all the setups.

## 7. Cleaning the new development directory

Use `npm` to clean the `develop` branch and make it ready for the `development`, by:
```sh
$> sudo npm run clean
```

## 8. Starting the deployment `locally`

Start developing, by:
```sh
$> sudo gatsby develop #or 
$> sudo npm run develop
```
Then you can access the website from local browser through `http://localhost:8000/`

For building the site:
```sh
$> sudo gatsby build #or
$> sudo npm run build
```

For Serving the production build locally
```sh
$> sudo gatsby serve #or
$> sudo npm run serve
```
Then you can access the website from local browser through `http://localhost9000/`

## 9. Publish your developments to the `master` branch
Once you finished the deployments, you need to push them to the `develop branch` and then publish them to the `master`. **Note**, you can publish directly without pushing to the `git` repo. Pushing will keep the local changes also in the remote source.

### Publishing
```sh
$> sudo npm run deploymaster
```
### Pushing
```sh
$> git push -u origin develop
```

## 10. Check the web page online
After a while (aprox 10 min) refresh the page [abdallahcoptan.github.io](https://abdallahcoptan.github.io/). 

-----------------------------------------------------------------------
# Abdallah Ibrahim, PhD
### Computer Scientist || Cloud Architect || Data Scientist

This was my personal website, and here how to deploy it on the personal page of the github pages: [abdallahcoptan.github.io](https://abdallahcoptan.github.io/)

