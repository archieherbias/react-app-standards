# Project initialization instructions and tips

### Initializating a React JS Web project

Best recommendation is to use `create-react-app` cli to be able to have a directly working react project without configuring webpack.

You can create a project using: `create-react-app <project-name>`

### Initializating React Native Project

Initializing a react-native project is a bit tricky and needs some undestanding of the project you are trying to create.

There is expo and there is react-native cli tool.

**When to use expo**
You'll want to use expo when:

- You have a slower machine and you have an android/ios phone.
- You don't have any native code dependencies.
- You don't want to deal the hassle of bundling your app. (Expo does this straight-forward).

You should not expo when:

- You will have to deal so much with native code.
- You want to build your project outside expo.

Though there is an `eject` option in expo where you can convert your project to a bare react-native project or using expokit, you will be encountering errors after that because `expo eject` is still a bit problematic. There are libraries that uses native code that doesn't resolved on the go when you eject from expo.

You can create a project using: `expo init <project-name>`

**When to use react-native cli**
You'll want to use react-native cli:

- When you have a faster machine especially a Mac so that you'll be able to run ios and android emulator.
- When you're dealing with many modules that needs native code. (e.g. Firebase SDK).
- When you know how to deal with key certifications of bundling your app.
- Less bundle size than expo.

You can create a project using: `react-native init <project-name>`
