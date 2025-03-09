This is [**React Native**](https://reactnative.dev) project cofig repo, build using [`@react-native-community/cli`](https://github.com/react-native-community/cli).

> # Getting Started
>
> **(Before you get startet, make these changes)**

- `android/build.gradle` and replace followint:

```
ext {
        buildToolsVersion = "34.0.0"
        minSdkVersion = 24
        compileSdkVersion = 34
        targetSdkVersion = 34
        ndkVersion = "26.1.10909125"
        kotlinVersion = "1.9.10"
    }
```

- recheck proper code in `android/app/src/main/java/com/<app_name>/MainActivity.kt`

```
package com.personfinder

import android.os.Bundle;
import com.facebook.react.ReactActivity
import com.facebook.react.ReactActivityDelegate
import com.facebook.react.defaults.DefaultNewArchitectureEntryPoint.fabricEnabled
import com.facebook.react.defaults.DefaultReactActivityDelegate
import org.devio.rn.splashscreen.SplashScreen;
```

- In `android/gradle.properties` add following lines

```
android.enableJetifier=true
```

- In `package.json` make sure to **replace versions** of following dependencies

```
"dependencies": {
    "react": "18.3.1",
    "react-native": "^0.76.6",
}

"devDependencies": {
    "@react-native-community/cli": "15.0.1",
    "@react-native-community/cli-platform-android": "15.0.1",
    "@react-native-community/cli-platform-ios": "15.0.1",
    "@react-native/babel-preset": "0.76.6",
    "@react-native/eslint-config": "0.76.6",
    "@react-native/metro-config": "0.76.6",
    "@react-native/typescript-config": "0.76.6",
}
```
