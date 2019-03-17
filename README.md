# react-native-cheatsheet
A cheat sheet for building production-ready react-native apps, based on my personal notes
* 🔥 Note: This is a work in progress 🔥

## Docs & Resources 🕵️‍♂️
* Offical docs: https://facebook.github.io/react-native/
* Discord: https://www.reactiflux.com/
* React Native Crash Course by Traversy Media: https://www.youtube.com/watch?v=mkualZPRZCs

## Project Setup 🚧
* Create a project:
``` 
react-native init MyAppName
```

## Dev Environment ⛰
* Run in iOS Simulator
```
react-native run-ios
```

* react-native run-ios --simulator=“iPhone X”
* Options include: iPhone 5s, iPhone 6, iPhone X, iPhone 8, etc.

## State Management, Persistance, and Middleware 🗂
* For large, API-connected projects: 
* Redux + React+redux + Redux-devtools + Redux-persist + Redux-thunk + axios:
* Redux: https://github.com/reduxjs/redux
* React-redux: https://react-redux.js.org/
* Redux-devtools: 
* Redux-persist: https://github.com/rt2zz/redux-persist
* Redux-thunk: https://github.com/reduxjs/redux-thunk
* Axios: https://github.com/axios/axios
* redux for global state management
* react-redux for react + redux bindings
* redux-thunk for redux middleware to make api calls
* redux-persist for persisting & rehydrating stores via asycstorage
* remote-redux-devtools for using redux devtools with react-native
```
npm install redux --save
npm install react-redux --save
npm install --save-dev redux-devtools
npm install redux-persist --save
npm install redux-thunk --save
npm install axios --save
```

Redux resources: 
* What is Redux? https://code-cartoons.com/a-cartoon-intro-to-redux-3afb775501a6 

* Other options include: Local state only, hooks, mobx

## Production Ready Packages 🏙
* Formik: https://github.com/jaredpalmer/formik
```
npm install formik --save
```
* Native Base: https://github.com/GeekyAnts/NativeBase
```
npm install native-base --save
react-native link
```

## Common Errors
* Make sure singing profile/team is set in iOS!
* Any package issue, try to remove and add all modules first: `rm -rf node_modules && npm install`
* Also, make sure to link: react-native link
* If a package doesn't link right for iOS: drag packages xcodeproj file to Libraries, and then link manually

## JavaScript & ES6, Most used concepts 🍎
* Higher-order functions: Map, filter, forEach and reduce
* Destructuring
* Let & Const
* The ternary

## Icons & App Store Images 📸
* iOS icons: Icon set creator: https://itunes.apple.com/us/app/icon-set-creator/id939343785?mt=12
* Android icons: https://romannurik.github.io/AndroidAssetStudio/index.html
* App Store Images: App Toolkit (Paid, free for one project): https://apptoolkit.io/

## Testing 🥽
Virtual Real-Device testing:
* Andriod, Samsung Remote Test Lab (Free): https://developer.samsung.com/rtlLanding.do
* iOS and Android, BrowserStack Interactive Mobile App Testing (Paid, free trial): https://www.browserstack.com/app-live
* iOS, Testflight





