# GITFIT (pending)

## Introduction

GitFit is a create-react-native-app app, built using the frameworks of [React Native v0.59](https://facebook.github.io/react-native/docs/getting-started.html). Create React Native App (CRNA) uses a library called [Expo](https://expo.io/), Expo is used to help create IOS or Android apps using a Javascript framework. Meaning, you can create code in JS to manipulate with some of the internal workings of a IOS or Android Devices ( ie. Notification, Contacts, Camera etc. ).

---

## Startup

Install VSCode Editor

- Install packages ( Prettier, Formatting Toggle ) These are use to lint our code.
  \*\* Default configuration for both extension packages

\* requires node v11.12.0 (install if needed) \*

```js
npm i
npm run ios
```

Xcode will open up to display the ios emulator

## Work Flow

```
git clone xxxxxxxx
git checkout -b <developer-name-problem_type>
..
* Work on issue / feature / hotfix *
...
git pull origin develop // fetch any updates or changes
git checkout -b <developer-name-problem_type>
git pull --rebase origin develop
git add .
git commit -m ""
git push origin develop
```

## Committing Code

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
```

- \<type> - feature | fix
- \<scope> - The scope could be anything specifying place of the commit change.
- \<body> (optional) - Description of file and details of what the changes were.
- \<subject> - Concise description of the change.

example:

```bash
feature(GitJumpy): added my-new-feature

GitJumpy.js - This is where the logic for xyz happened
GitjumpyStylesheet.js - this is the styling for GitJumpy.js
```

---

## NOTES

#### Styling a component

For React Native (RN) it seems best practice to [style a component](https://facebook.github.io/react-native/docs/style) using javascript. Simply create a `const style` (object) and passing the `style` as a prop.

Create a file: \<Component>Style.js

```js
import { Stylesheet } from "react-native";

const styles = StyleSheet.create({
  bigBlue: {
    color: "blue",
    fontWeight: "bold",
    fontSize: 30
  },
  red: {
    color: "red"
  }
});
```

> \*** The style names and values usually match how CSS works on the web, except names are written using **camel casing\*\*, e.g backgroundColor rather than background-color.

> \*** You can also pass an array of styles - the last style in the array has **precedence\*\*, so you can use this to inherit styles.

One common pattern is to make your component accept a style prop which in turn is used to style subcomponents. You can use this to make styles "cascade" the way they do in CSS.

#### Navigation

Create-React-Native-App (CRNA) uses [react-navigation](https://reactnavigation.org/docs/en/hello-react-navigation.html). **Please take the time to review the linked document (4 min read).**

_Need to know:_ react-navigation uses a function called `createStackNavigator()` it takes in an object which is written like this

```js
 createStackNavigator(
    {
        Home: { // Name of Route
            screen: HomeScreen // Component being called.
        },
        Details: {
            screen: DetailsScreen
        }
    },
    {
        initialRouteName: "Home" // Default route.
    }
   }
)
```

Helpful documentation to understand the stack can be found here:

Backend
https://expo.io/
https://facebook.github.io/react-native/docs/navigation

Icons + Styling
https://facebook.github.io/react-native/docs/style
https://ionicons.com/

Testing JS and Coverage
https://jestjs.io/docs/en/tutorial-react-native.html

Components Manually Installed:

- [React Navigation](https://reactnavigation.org/docs/en/hello-react-navigation.html)
