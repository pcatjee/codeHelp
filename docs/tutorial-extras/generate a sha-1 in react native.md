---
sidebar_position: 3
---

# Generate SHA-1 in React Native CLI project

To generate a SHA-1 hash in a React Native CLI project, you can use the **react-native** command line interface along with the **keytool** command from the Java Development Kit (JDK). Here are the general steps to follow:

1. Open a command prompt or terminal window and navigate to your project directory.

2. Run the following command to generate a debug keystore:

```bash
keytool -genkey -v -keystore debug.keystore -storepass android -alias androiddebugkey -keypass android -keyalg RSA -keysize 2048 -validity 10000
```

This will generate a debug keystore file named `debug.keystore` in your project directory. The keystore password is set to `android` by default, and the key alias is set to `androiddebugkey`.

3. Run the following command to extract the SHA-1 fingerprint from the debug keystore:

```bash
keytool -list -v -keystore debug.keystore -alias androiddebugkey -storepass android -keypass android
```

This will output the certificate details, including the SHA-1 fingerprint.

4. Copy the SHA-1 fingerprint and use it as needed, such as for configuring Google API credentials.

**Note** that if you are building a release version of your app, you will need to generate a release keystore and use it to sign your app. You can use the same **keytool** command to generate a release keystore, but you will need to provide your own values for the keystore password, key alias, and validity period. Additionally, you may need to configure your build settings to use the release keystore for signing.
