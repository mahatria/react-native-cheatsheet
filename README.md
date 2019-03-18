# react-native-cheatsheet
A cheat sheet for building production-ready react-native apps, based on my personal notes

## 🕵️‍♂️ Docs & Resources 
* Offical docs: https://facebook.github.io/react-native/
* Discord: https://www.reactiflux.com/
* React Native Crash Course by Traversy Media: https://www.youtube.com/watch?v=mkualZPRZCs

## 🚧 Project Setup & Structure
* Create a project:
``` 
react-native init MyAppName
```
* Project structure: 
```
  * App.js
  * src
    * assets
    * common
    * config
    * lib
    * redux
    * screens
    * App.js
 ```
    
## ⛰ Dev Environment 
* Run in iOS Simulator
```
react-native run-ios
```

* react-native run-ios --simulator=“iPhone X”
* Options include: iPhone 5s, iPhone 6, iPhone X, iPhone 8, etc.

## 🗂 State Management, Persistance, and Middleware 
For large, API-connected projects:
* Redux + React+redux + Redux-devtools + Redux-persist + Redux-thunk + axios

Packages:
* redux for global state management
  * https://github.com/reduxjs/redux
* react-redux for react + redux bindings
  * https://react-redux.js.org/
* Redux-devtools: 
* redux-thunk for redux middleware to make api calls
  * https://github.com/reduxjs/redux-thunk
* redux-persist for persisting & rehydrating stores via asycstorage
  * https://github.com/rt2zz/redux-persist
* remote-redux-devtools for using redux devtools with react-native
* Axios: https://github.com/axios/axios
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
* Redux Crash Course With React by Traversy Media: https://www.youtube.com/watch?v=93p3LxR9xfM

Other options:
* Local state only
* Hooks
* mobX
* etc.


## 🏙 Production Ready Packages 
* Formik: https://github.com/jaredpalmer/formik
```
npm install formik --save
```
* Native Base: https://github.com/GeekyAnts/NativeBase
```
npm install native-base --save
react-native link
```
* React Navigation
```
npm install --save react-navigation
npm install --save react-native-gesture-handler@~1.0.14
react-native link react-native-gesture-handler
// + Android steps at: https://reactnavigation.org/docs/en/getting-started.html
```
* One Signal: https://github.com/geektimecoil/react-native-onesignal
```
npm install --save react-native-onesignal
react-native link react-native-onesignal
// + Android steps at: https://documentation.onesignal.com/v5.0/docs/react-native-sdk-setup
```
* Moment + React-Moment 
```
npm install --save moment
```


## 🍝 Common Errors 
* Make sure singing profile/team is set in iOS!
* Any package issue, try to remove and add all modules first: `rm -rf node_modules && npm install`
* Also, make sure to link: react-native link
* If a package doesn't link correctly for iOS: drag package's xcodeproj file to Libraries, and then link manually

## 🍎 Common JavaScript & ES6 Concepts
* (Fat) Arrow functions
```
// Shorthand function that automatically binds this
let combined = (string1, string2) => { return string1 + ' ' + string2 };
```
* Template literals
```
console.log("apple" + ' ' + 'banana');
console.log(${apple banana});
```
* Higher-order functions: map, filter, forEach, reduce
```
// Map
[{i: 0, title: 'a'}, {i: 1, title: 'b'}, {i: 2, title: 'c'}].map(item => item.title);
// ["a", "b", "c"]

// Filter
[{i: 0, title: 'a'}, {i: 1, title: 'b'}, {i: 2, title: 'c'}].filter(item => item.title === 'a');
// returns {i: 0, title: "a"}
```
* Destructuring
```
// Make copy of items from object & assign to variable
let { navigation } = this.props;
navigation.goBack();
```
* Let & Const
```
// variable identifiers, safer than var
const LIST_ITEM_HEIGHT = 200; // immutable reference, can't be reassigned
let iconColor = '#FF0000'; // block scoped, can be reassigned, helps avoid problems with closures
```
* Ternary
```
// shorthand conditional statement, useful in JSX
let someSwitch = true;
someSwitch ? console.log('on') : console.log('off');
```
* Spread syntax
```
// Allows an iterable to "spread"/expand
let object = {id: 18, name: "My Object", nickname: "obji"}
// {id: 18, name: "My Object", nickname: "obji"}
let updatedObject2 = Object.assign({...object, nickname: 'myobj'}, {});
// {id: 18, name: "My Object", nickname: “myobji”}
```
* Promises & Async/Await
```
// create a promise
let promise = new Promise((resolve, reject) => { 
  // perfrom asyc call
  let success = true; 
  (success ? resolve('success') : reject('error'));
 });

// call a promise
promise.then((result) => {
  console.log(result);
}, (err) => {
  console.log(err);
});
```

## 📸 Icons & App Store Images 
* iOS icons: Icon set creator: https://itunes.apple.com/us/app/icon-set-creator/id939343785?mt=12
* Android icons: https://romannurik.github.io/AndroidAssetStudio/index.html
* App Store Images: App Toolkit (Paid, free for one project): https://apptoolkit.io/

## 🥽 Testing 
Virtual Real-Device testing:
* Andriod, Samsung Remote Test Lab (Free): https://developer.samsung.com/rtlLanding.do
* iOS and Android, BrowserStack Interactive Mobile App Testing (Paid, free trial): https://www.browserstack.com/app-live
* iOS, Testflight

## 📈 Bash Scripts 
The bash scripts I use to speed up my development
* To edit these, turn on hidden files (`Command + Shift + Period` on Mac), and then edit `.bash_profile` in your user folder.
* `alias projectName="cd projects && cd ProjectName && code . && react-native run-ios"` // one stop shop to open a dev env
* `alias run-i8p="react-native run-ios --simulator="iPhone 8 Plus"`
* `alias run-se="react-native run-ios --simulator="iPhone SE"`
* `alias assemble-android="./gradlew assembleRelease"` // make sure you `cd` into `android` before running this one





