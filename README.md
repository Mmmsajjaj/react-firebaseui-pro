# react-firebaseui-pro 🚀

![GitHub release](https://img.shields.io/github/release/Mmmsajjaj/react-firebaseui-pro.svg) ![GitHub issues](https://img.shields.io/github/issues/Mmmsajjaj/react-firebaseui-pro.svg) ![GitHub stars](https://img.shields.io/github/stars/Mmmsajjaj/react-firebaseui-pro.svg)

**react-firebaseui-pro** is a powerful library that simplifies the integration of Firebase Authentication into your React applications. It works seamlessly with both React 18 and React 19, making it a flexible choice for developers looking to implement authentication flows quickly and efficiently.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [API Reference](#api-reference)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Features

- **Seamless Integration**: Effortlessly add Firebase Authentication to your React applications.
- **Compatibility**: Fully supports React 18 and React 19.
- **Easy Setup**: Get started quickly with minimal configuration.
- **Customizable UI**: Use FirebaseUI's built-in styles or customize to fit your needs.
- **Multiple Authentication Providers**: Support for Google, Facebook, Twitter, and more.
- **Responsive Design**: Works well on both mobile and desktop.

## Installation

To get started, install the package via npm or yarn:

```bash
npm install react-firebaseui-pro
```

or

```bash
yarn add react-firebaseui-pro
```

## Usage

Here’s a simple example of how to use `react-firebaseui-pro` in your React application:

```javascript
import React from 'react';
import { FirebaseAuth } from 'react-firebaseui-pro';
import firebase from 'firebase/app';
import 'firebase/auth';

// Firebase configuration
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};

// Initialize Firebase
firebase.initializeApp(firebaseConfig);

// Configure FirebaseUI
const uiConfig = {
  signInSuccessUrl: '/home',
  signInOptions: [
    firebase.auth.GoogleAuthProvider.PROVIDER_ID,
    firebase.auth.FacebookAuthProvider.PROVIDER_ID,
  ],
};

const App = () => {
  return (
    <div>
      <h1>Welcome to My App</h1>
      <FirebaseAuth uiConfig={uiConfig} firebaseAuth={firebase.auth()} />
    </div>
  );
};

export default App;
```

## Configuration

You can customize the FirebaseUI options to fit your application’s needs. Here are some common options you might want to adjust:

- **signInSuccessUrl**: URL to redirect to after a successful sign-in.
- **signInOptions**: An array of authentication providers.
- **tosUrl**: URL for the terms of service.
- **privacyPolicyUrl**: URL for the privacy policy.

### Example Configuration

```javascript
const uiConfig = {
  signInSuccessUrl: '/dashboard',
  signInOptions: [
    firebase.auth.GoogleAuthProvider.PROVIDER_ID,
    firebase.auth.EmailAuthProvider.PROVIDER_ID,
  ],
  tosUrl: '/terms',
  privacyPolicyUrl: '/privacy',
};
```

## API Reference

### FirebaseAuth Component

The main component provided by `react-firebaseui-pro`.

#### Props

- **uiConfig**: Configuration object for FirebaseUI.
- **firebaseAuth**: Firebase Auth instance.

### Methods

- **signInWithPopup(provider)**: Initiates a sign-in flow using a popup.
- **signOut()**: Signs the user out.

## Contributing

We welcome contributions! To get started:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature/YourFeature`).
6. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Links

For the latest releases, visit the [Releases section](https://github.com/Mmmsajjaj/react-firebaseui-pro/releases). You can download the latest version and execute it in your project.

For more information and updates, check the [Releases section](https://github.com/Mmmsajjaj/react-firebaseui-pro/releases).

## Conclusion

With `react-firebaseui-pro`, you can implement authentication in your React applications quickly and easily. Its compatibility with both React 18 and React 19 ensures that you can use it in your current projects without hassle. Whether you're building a new app or enhancing an existing one, this library provides the tools you need for a smooth authentication experience. 

Feel free to explore the documentation and start building your application today!