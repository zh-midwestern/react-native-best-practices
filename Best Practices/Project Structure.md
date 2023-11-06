# Project Structure

*React Native allows you to set up projects in different workflows, each with its own characteristics and use cases. The two primary workflows are the "Expo" or "Managed" workflow and the "Bare" workflow. Here's an overview of each:*

### Expo (Managed) Workflow
- This is the easiest and fastest way to get started with React Native. It's perfect for smaller apps or when you want to quickly prototype an idea.
- Expo provides a set of pre-built components and APIs, allowing you to develop without having to deal with the native code (Java, Swift, Objective-C).
- It includes a development environment and tools, such as the Expo Client app, which makes it easy to test your app on physical devices without the need for a Mac (iOS development typically requires a Mac).
- However, it comes with some limitations, as you can only use the Expo APIs and components. If your app requires custom native modules or dependencies that are not available through Expo, you may need to eject to the "Bare" workflow.

### Bare workflow
- The "Bare" workflow gives you full control over your React Native project and access to the native code of both iOS and Android platforms.
- It's suitable for larger or more complex apps that require custom native modules or when you need to integrate third-party native libraries.
- When using the "Bare" workflow, you'll have to set up and configure the native development environments (Android Studio for Android and Xcode for iOS) on your machine.
- You can add native modules and dependencies manually, which allows for a high degree of customization.
- Migrating from the "Expo" to the "Bare" workflow is possible, but it's often a complex process and may require rewriting parts of your codebase.
In addition to these two primary workflows, there are also other tools and configurations to consider, such as:

### ExpoKit (Legacy)
- ExpoKit is a way to eject an Expo project partially, allowing you to add custom native modules or dependencies to an Expo project.
- It's not recommended for new projects, as the Expo team has deprecated it in favor of the "Bare" workflow.

### CRNA (Create React Native App)
- CRNA was a tool for generating simple React Native apps with a limited set of features.
- It was a precursor to the Expo workflow and is now considered deprecated.


## FILE STRUCTURE
### Bare Workflow
```
project-name/
  ├── __tests__/                  // Unit and integration tests
  ├── android/                    // Android platform-specific files
  ├── ios/                        // iOS platform-specific files
  ├── node_modules/               // Dependencies
  ├── src/                        // Application source code
  │   ├── App.js                  // The main entry point for the app
  │   ├── assets/                 // Images, fonts, and other static assets
  │   ├── components/             // Reusable UI components
  │   ├── config/                 // Build environment variables
  │   ├── constants/              // Global constants
  │   ├── screens/                // Application screens or pages
  │   ├── navigation/             // Navigation setup (e.g., React Navigation)
  │   ├── utils/                  // Utility functions and helper files
  │   ├── services/               // API services and other external integrations
  │   ├── index.js                // The entry point for React Native
  ├── package.json                // Node.js project configuration
  ├── package-lock.json           // Lock file for Node.js dependencies
  ├── .babelrc                    // Babel configuration
  ├── .eslintrc.js                // ESLint configuration
  ├── .prettierrc                 // Prettier configuration
  ├── .gitignore                  // List of files and directories to ignore in Git
  ├── README.md                   // Project documentation
  ├── CHANGELOG.md                // Project documentation

```

## FEATURE FLAGGING
*Feature flagging is a powerful technique that allows you to control the release and visibility of features in your React Native projects. This can be useful for A/B testing, phased rollouts, and enabling or disabling features without the need for code deployments.*
1. **LaunchDarkly**: LaunchDarkly is a popular feature flagging platform that offers a React Native SDK. It provides feature management, experimentation, and personalization capabilities. LaunchDarkly is known for its reliability and developer-friendly interface.
2. **Split.io**: Split.io is a feature flagging and experimentation platform that offers a React Native SDK. It allows you to manage feature flags, conduct A/B tests, and track user behavior. Split.io is known for its real-time capabilities and easy integration.
3. **Optimizely**: Optimizely is a well-established experimentation platform that offers feature flagging as one of its capabilities. They provide a React Native SDK to integrate feature flags into your mobile app.
4. **Flagsmith**: Flagsmith is an open-source feature flagging and remote configuration platform. It has a React Native SDK that allows you to control feature flags, remote configurations, and manage feature toggles.
5. **Rollout.io**: Rollout.io is a feature flagging and remote configuration service designed specifically for mobile apps, including React Native. It allows you to manage feature flags and configuration settings.
6. **Unleash**: Unleash is an open-source feature flagging and experimentation framework. It provides a React Native SDK for managing feature flags and running experiments. You can host Unleash on your own infrastructure for data control.
7. **Flipper**: Flipper is Facebook's mobile development platform, and it includes a feature flagging and experimentation framework. It's well-suited for React Native apps and provides the ability to manage feature flags and experiments.

## MESSAGING
1. **Firebase Cloud Messaging (FCM)**: Firebase Cloud Messaging is a cloud solution from Google for delivering messages and push notifications to iOS, Android, and web apps. It is known for its reliability and scalability. Firebase can be integrated into React Native using various libraries or the Firebase JavaScript SDK.
2. **Twilio**: Twilio provides a messaging API that allows you to add SMS and chat functionality to your React Native app. It's known for its developer-friendly platform and robust features, making it a good choice for various messaging needs.
3. **Pusher Chatkit (now part of MessageBird)**: Pusher Chatkit is a messaging API that offers features for real-time chat, in-app messaging, and user presence. It provides a React Native SDK for easy integration. Note that Pusher Chatkit was acquired by MessageBird, so you might want to check the latest offerings and pricing.
4. **SendBird**: SendBird is a comprehensive chat and messaging platform that offers a React Native SDK. It provides features like real-time chat, in-app messaging, and push notifications. SendBird is known for its flexibility and scalability.
5. **Socket.io**: Socket.io is a real-time web socket library that can be used to implement real-time messaging in React Native. It allows you to create custom real-time communication features, and it's well-suited for scenarios where you need full control over messaging.
6. **OneSignal**: OneSignal is primarily a push notification service that also offers in-app messaging capabilities. It provides a React Native SDK for both push notifications and in-app messaging, making it a convenient choice for a range of messaging needs.