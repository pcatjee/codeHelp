---
sidebar_position: 1
---

# React Native

All code snippets **available at one place in less than 5 minutes**.

## Getting Started

Get started by **creating a new site**.

Or **try Docusaurus immediately** with **[docusaurus.new](https://docusaurus.new)**.

### What you'll need

- [Node.js](https://nodejs.org/en/download/) version 16.14 or above:
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.

## Generate a new project

Generate a new React Native project using built-in **command line interface.** **[Source](https://reactnative.dev/docs/environment-setup)**.

```bash
npx react-native@latest init AwesomeProject
```

## Start your site

Run the development server:

```bash
cd my-website
npm run start
```

The `cd` command changes the directory you're working with. In order to work with your newly created Docusaurus site, you'll need to navigate the terminal there.

The `npm run start` command builds your website locally and serves it through a development server, ready for you to view at http://localhost:3000/.

Open `docs/intro.md` (this page) and edit some lines: the site **reloads automatically** and displays your changes.

## Reset React Native Cache

For React Native Init approach (without expo) use: **[Source](https://stackoverflow.com/questions/46878638/how-to-clear-react-native-cache)**

```bash
npm start -- --reset-cache
```

## Reset React Native Expo Cache

For React Native expo use: **[Source](https://docs.expo.dev/troubleshooting/clear-cache-windows/)**

```bash
npx expo start --clear
```

This restarts the development server and instructs the bundlers (e.g., webpack, Metro) to clear their caches

## React Native stack navigator

## Installation

Install the required packages in your React Native project:

```bash
npm install @react-navigation/native
```

## Installing dependencies into an Expo managed project

In your project directory, run:

```bash
npx expo install react-native-screens react-native-safe-area-context
```

## Installing dependencies into a bare React Native project

In your project directory, run:

```bash
npm install react-native-screens react-native-safe-area-context
```

To use the native stack navigator, we need to install `@react-navigation/native-stack` :

```bash
npm install @react-navigation/native-stack
```

## Creating a native stack navigator

```bash
// In App.js in a new project

import * as React from 'react';
import { View, Text } from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createNativeStackNavigator } from '@react-navigation/native-stack';

function HomeScreen() {
  return (
    <View style={{ flex: 1, alignItems: 'center', justifyContent: 'center' }}>
      <Text>Home Screen</Text>
    </View>
  );
}

const Stack = createNativeStackNavigator();

function App() {
  return (
    <NavigationContainer>
      <Stack.Navigator>
        <Stack.Screen name="Home" component={HomeScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}

export default App;
```
