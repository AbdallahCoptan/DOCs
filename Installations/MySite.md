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



# Setup your personal page on Github Pages

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
sudo apt-get install npm
```

Make sure that you have the Gatsby CLI program installed:

```sh
npm install --global gatsby-cli
```
And run from your CLI:

```sh
gatsby new <acountname.github.io> https://github.com/anubhavsrivastava/gatsby-starter-resume
```

Then you can run it by:

```sh
cd <acountname.github.io>
npm install
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
npm run clean
```




## Adding a develop branch

Adding a new branch for development because you need to make your `index.html` file on the master branch. 
This is will let the website got published on the personal github page of your repo.  

Issuing a new branch by

```sh
git checkout -b develop
```
**All the development should be on the develop branch, and the master will not be touched anymore**

Updating the `package.json` file by adding a new *script* on "scripts" section:

```
"deploymaster": "npm run clean && gatsby build --prefix-paths && gh-pages -d public -b master",
```


### Starting the development:

```sh
gatsby develop
```

## Push changes to the git [optional]

```sh
git push -u origin develop
```

## Building your website

This will let your website is ready for publishing, to do so by:

```sh
gatsby build [or] npm run build
```

### Publishing on the github personal pages

In order to publish the website on the github pages:

```sh
npm run deploymaster
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





# Abdallah Ibrahim, PhD
### Computer Scientist || Cloud Architect || Data Scientist

This was my personal website, and here how to deploy it on the personal page of the github pages: [abdallahcoptan.github.io](https://abdallahcoptan.github.io/)
