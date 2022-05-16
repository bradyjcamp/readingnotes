# React Native

## Introduction

- **React Native** is used to create mobile application on one's phone and is used by IOS devs and beginners alike!

- Install on your local terminal and run command `npm install --global expo-cli && expo init my-project`

- Open in up on your code Editor of choice and you should have a App.js with the following.

```js
import React from 'react';
import { Text, View } from 'react-native';

const YourApp = () => {
  return (
    <View style={{ flex: 1, justifyContent: "center", alignItems: "center" }}>
      <Text>
        Try editing me! 🎉
      </Text>
    </View>
  );
}

export default YourApp;
```

- Using React Native and creating an app with it still uses *class components* and *function components* with hooks.
- `Text` and `View` are components from react-native and are used instead of HTML `<p> </p>` tags.
- You can still use other react features such as `useState` and `useEffect` just to name a couple.  

See example from [React Native Docs](https://reactnative.dev/docs/tutorial)

```js
// ReactJS Counter Example using Hooks!

import React, { useState } from 'react';



const App = () => {
  const [count, setCount] = useState(0);

  return (
    <div className="container">
      <p>You clicked {count} times</p>
      <button
        onClick={() => setCount(count + 1)}>
        Click me!
      </button>
    </div>
  );
};


// CSS
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

## Expo

- This is a common framework for creating react apps.
- This allows you to also download the Expo Go app on your smartphone for local development and testing.

[ExpoKit is deprecated](https://docs.expo.dev/expokit/eject/?redirected)
