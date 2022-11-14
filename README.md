# Quasar App (noone)

A Quasar Project

## Install the dependencies

```bash
yarn
# or
npm install
```

### Dev Environment

export PATH="$(yarn global bin):$PATH"

install android-studio
export ANDROID_SDK_ROOT=~/Android/Sdk
export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools
export PATH=$PATH:$ANDROID_SDK_ROOT/tools
export PATH=$PATH:$ANDROID_SDK_ROOT/tools/bin

install gradle
export GRADLE_HOME=~/Apps/gradle-7.5.1/
export PATH=${GRADLE_HOME}/bin:${PATH}

install java =-jdk
export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-amd64
export PATH=$PATH:$JAVA_HOME/bin

### Start the app in development mode (hot-code reloading, error reporting, etc.)

```bash
quasar dev
```

## Run on hardware device

Check `adb devices`, add permisions udev:
`sudo usermod -aG plugdev $LOGNAME`

```bash
quasar dev -m cordova -T android --device
```

### Lint the files

```bash
yarn lint
# or
npm run lint
```

### Format the files

```bash
yarn format
# or
npm run format
```

### Change cordova packageName

Edit src-cordova/config.xml

```bash
cordova platform remove android
cordova platform add android
```

### Build the app for production

```bash
quasar build
```

### Customize the configuration

See [Configuring quasar.config.js](https://v2.quasar.dev/quasar-cli-vite/quasar-config-js).
