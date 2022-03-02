# How to setup Appium on Mac

## 1. Prerequisites

- [ ] Xcode  
    ### Download via the Developer site for a specific version  

    1. Head to the "more" section of the Apple developer website
    2. Sign in with your iTunes account id
    3. Type in the version that you'd like, and download the Xcode_x_x_x.xip file. Keep in mind that Xcode 11.4.1 is 8 gigabytes, so this will take awhile depending on your internet connection.
    4. Once the file is downloaded, click on .xip to extract it. Your laptop will extract it to the same folder you downloaded it to. This extraction process is automatic. You don't need to do anything more after you click on the .xip file. This step will take a few minutes.
    5. [Optional] Once extracted, rename the application to “Xcode11.x.x” if you are using multiple versions.
    6. Drag application to the Applications folder
    7. [Optional] Set the new Xcode version as the default. Open Terminal and type sudo xcode-select -switch /Applications/Xcodex.x.x.app . Replace x.x.x with the version number. For example: Xcode11.4.1.app. You will need to enter in your computer admin password. I'm pretty sure this will update the default Xcode version for all users on your computer, so best to check with other users first  
- [ ] Xcode Command Line Tools
    ```
    xcode-select --install
    ```
- [ ] Homebrew
    ```
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
- [ ] Carthage
    ```
    brew install carthage
    ```
- [ ] asdf
    ```
    brew install asdf
    ```

## 2. Appium
- [ ] Node.js
    ```
    brew install node
    ```
- [ ] nvm
    ```
    brew install nvm
    ```
- [ ] Appium Server
    ```
    npm install -g appium
    ```
- [ ] Appium Desktop  
https://github.com/appium/appium-desktop/releases

## 3. Appium-doctor
```
npm install -g appium-doctor
```

## 4. Android Studio Setup
- [ ] Java
    ```
    brew install openjdk
    ```
- [ ] Configure JAVA_HOME
    ```
    open ~/.zshrc
    ```

    Add the following commands in ```.zshrc```
    ```
    export JAVA_HOME=/Library/Java/Home
    ```

- [ ] Configure ANDROID_HOME
    ```
    open ~/.zshrc
    ```

    Add the following commands in ```.zshrc```
    ```
    export ANDROID_HOME=/YOUR_PATH_TO/android-sdk
    export PATH=$ANDROID_HOME/platform-tools:$PATH
    export PATH=$ANDROID_HOME/tools:$PATH
    ```
- [ ] Android Emulator  

    To create an Android Emulator in Android Studio:  
Configure > AVD Manager > Create Virtual Device

## 5. iOS Setup
- [ ] iOS Simulator

    To download iOS simulator:  
Xcode > Preferences > Components > Downloading a iOS Simulator version  

    To open iOS simulator:   
Xcode > Open Developer Tool > Simulator

## References
1. https://medium.com/tauk-blog/quick-start-guide-for-setting-up-appium-on-an-m1-mac-a629a70a40cb

2. https://www.youtube.com/watch?v=7APcLr-cBM8&list=PLhW3qG5bs-L8npSSZD6aWdYFQ96OEduhk&index=4

3. https://www.freecodecamp.org/news/how-to-download-and-install-xcode/

4. https://stackoverflow.com/questions/19986214/setting-android-home-enviromental-variable-on-mac-os-x