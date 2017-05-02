# Setting up Appium on Mac

## Install HomeBrew
`HomeBrew` is a package manager for OS X. Once installed it can help to install other packages that we will need during our setup.

- Visit [HomeBrew Home Page](http://brew.sh/).
- Use the command to install HomeBrew which is given on the above page.
```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
- Now you can install any package with following.
```
brew install <package>
```

## Install NodeJS
`Node.js` is a JavaScript runtime built on Chrome's V8 JavaScript engine. It is required to run appium on your machine.

- To install `NodeJS` use `brew`.
```
brew install node
```
- Now you have `node` and `npm` installed you your machine. `npm` is Node Package Manager that can help install any node module.
- There are other ways to install node using an insatller provided on [NodeJS Home Page](https://nodejs.org/en/) as well or [NVM](https://github.com/creationix/nvm).

## Install Appium
- Install appium using the installer provided on their [home page](http://www.appium.io).
- You may also install `appium` using `npm`
```
npm install -g appium
```
This will install appium globally on your machine and you can use `appium` command from your commandline anywhere to start the server.

## Install Android SDK
Android SDK is a set of tools and core libraries that is needed to setup and run android tests. You do not need full `Android Studio` which is an IntelliJ IDEA based IDE for app development.

- Download the [android-sdk standalone version](https://developer.android.com/sdk/installing/index.html).
- Extract the content
```
cd ~/Downloads
tar -xvf <android-sdk-archive>
```
- Move it to a location of your choice. I do it in /opt
```
mv <android-sdk-folder> /opt/
```
- Most of the commands for android are in `<android-sdk>/tools` and `<android-sdk>/platform tools` directories. So we should add these to our path.
- Use your favorite editor to add the following to your profile (.zshrc or .bash_profile depending whether you use zsh or bash). Do not forget to change the android-sdk directory.
```
export PATH="$PATH:/opt/<android-sdk>/tools:/opt/<android-sdk>/platform-tools"
```

## Add SDK Packages
- Launch terminal and start android
```
adnroid
```
- Select the following (if not already installed. If already installed do not check them or they will be marked for uninstallation.)
  - Android SDK Tools
  - Android SDK Platform-tools
  - Android SDK Build-tools 
  - SDK Platform (Choose the version that you have on your device)
  - Android Support Repository
  - Android Support Library
  - Google Repository
  - Google Play services

- Click `Install X packages`. It takes quite some time to get completed.



