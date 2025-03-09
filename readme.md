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

- Before `npx react-native run-android`, Clean graldew by running following in terminal:
```
cd android
gradlew clean (in Powershell) 
(OR ./gradlew clean in Terminal)

cd ..
npx react-native run-android
```