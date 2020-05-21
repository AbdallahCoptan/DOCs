
# Installing Node.js and NPM on Ubuntu/Debian


Tagged linux ubuntu debian nodejs devops node npm

This is just short snippet on how to install Node.js (any version) and NPM (Node Package Manager) on your Ubuntu/Debian system.

## Step 1 - Update your system

```
sudo apt-get update
sudo apt-get install git-core curl build-essential openssl libssl-dev python
```

## Step 2 - Install Node.js

First, clone the `Node.js` repository:

```
git clone https://github.com/nodejs/node.git
cd node
```

Now, if you require a specific version of Node:

```
git tag # Gives you a list of released versions
git checkout v13.10.1
```

Then compile and install Node like this:

This might take a while, depending on your hardware.

```
./configure
make
sudo make install
```

Then, check if node was installed correctly:

```
node -v

```

## Step 3 - Install NPM

Simply run the `NPM` install script:

```
curl -L https://npmjs.org/install.sh | sudo sh

```

And then check it works:

```
npm -v

```

That’s all.

Updated 2020-03-11

    Use the new nodejs/node repo
    Install correct dependencies, including python\
    Update example node version to v13.10.1_

