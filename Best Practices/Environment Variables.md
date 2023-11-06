# ENVIRONMENT VARIABLES

## Bare Minimum
- **Security**: Ensure that sensitive information like API keys, credentials, and private settings are stored securely in environment variables, protecting them from accidental exposure in the source code or version control repositories.
- **Environment Consistency**: Utilize environment variables to maintain a consistent configuration across different deployment environments (development, testing, production) to avoid configuration-related issues and ensure the app behaves consistently.
- **Ease of Configuration**: Make it straightforward for developers to configure and manage environment variables by providing clear documentation and tools for setting and accessing these variables in the development workflow.

## Best Practices
- **Sensitive Data Isolation**: Store sensitive information such as API keys, passwords, and tokens in environment variables to keep them separate from the source code and prevent accidental exposure.
- **Configuration Management**: Use environment variables to manage configuration settings that may vary between development, testing, and production environments, allowing for consistent behavior across different stages.
- **Version Control Exclusion**: Exclude environment variable files or values from version control systems to prevent unintentional exposure of sensitive data and to maintain the security of your application.
- **Centralized Configuration**: Implement a centralized configuration approach that enables easy access and modification of environment variables, ensuring consistency and simplifying maintenance.
- **Fallback Values**: Provide default or fallback values for environment variables to ensure that your app can function gracefully even when certain variables are not set or available.
- **Validation and Documentation**: Validate environment variables to ensure they adhere to expected formats and provide comprehensive documentation for developers regarding the purpose and usage of each variable.
- **Environment-Specific Files**: Create separate environment-specific configuration files that load the appropriate environment variables. This can help manage settings for different deployment stages.
- **Secure Storage**: Use tools or libraries that offer secure storage mechanisms for environment variables, especially when dealing with sensitive information.
- **Continuous Integration/Continuous Deployment (CI/CD) Integration**: Integrate environment variables seamlessly into your CI/CD pipeline to automate configuration management for different deployment stages.
- **Encrypted Variables**: For added security, consider encrypting sensitive environment variables at rest, making them accessible only with appropriate decryption keys.

## Tools
- **react-native-config**: This library enables you to define environment variables in separate files (e.g., `.env`, `.env.development`, `.env.production`) and access them in your React Native code. It's a popular choice for managing environment variables in React Native applications.
- **Dotenv**: Dotenv is a simple package that loads environment variables from a `.env` file into the app's environment, making them accessible in your JavaScript code. It's widely used for handling configuration settings.
- **Platform-Specific Methods**: React Native allows you to use platform-specific methods to set and access environment variables. For example, on Android, you can use `BuildConfig` to define variables, and on iOS, you can use `.xcconfig` files to manage environment-specific configuration.
- **CI/CD Systems**: Some Continuous Integration/Continuous Deployment (CI/CD) systems, like Jenkins, CircleCI, or GitHub Actions, allow you to set and manage environment variables for different stages of the development and deployment process.
- **Platform-Specific Environment Files**: You can create platform-specific configuration files (e.g., `android/app/src/debug/res/values/config.xml` for Android or `.xcconfig` files for iOS) to set environment-specific variables. 

	*For an average React Native application, using the `react-native-config` library is recommended. It provides a straightforward way to manage environment variables across different deployment environments and is well-documented.*

## OTHER
- Packages
		- [react-native-config](https://www.npmjs.com/package/react-native-config)
		- [plugin-transform-inline-environment-variable](https://stackoverflow.com/a/37823398) 
- `env.js` file that is not in source control
- remote configuration where you hit an API endpoint or flag that passes back the keys/urls