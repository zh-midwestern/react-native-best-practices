# Continuous Integration

## Bare Minimum
- **Automated Testing**: Implement automated testing for your app, covering unit tests, integration tests, and UI tests. Ensure that these tests are regularly run in the CI pipeline to detect and address issues early in the development process.
- **Version Control Integration**: Integrate your CI system with a version control system like Git. Automate the process of triggering CI builds and deployments upon code commits or pull requests, ensuring that code changes are continuously tested and integrated.
- **Artifact Generation**: Set up CI to generate build artifacts, such as binary files or installable packages, for various platforms (iOS and Android). These artifacts should be available for deployment to test and production environments, enabling automated delivery and release processes.

## Best Practices 
- **Automated Testing**: Implement a comprehensive suite of automated tests, including unit tests, integration tests, and UI tests. Run these tests as part of your CI pipeline to identify and address issues early in the development process.
- **Version Control Integration**: Use a version control system like Git and integrate it with your CI/CD pipeline. Ensure that code commits, pull requests, and branches trigger automated builds, tests, and deployments.
- **Parallel Testing**: Distribute test execution across multiple devices and simulators/emulators to reduce testing time. Utilize tools like Appium, Detox, or React Native Testing Library for efficient parallel testing.
- **Consistency Across Platforms**: Ensure that your CI/CD setup supports both iOS and Android platforms, allowing for consistent testing, building, and deployment across both major mobile platforms.
- **Separate Staging Environment**: Create a staging environment that mirrors the production environment as closely as possible. Test your app in this environment to identify issues that might not surface in development or testing.
- **Code Linting and Static Analysis**: Integrate code linting and static analysis tools into your CI pipeline to enforce code quality and catch potential issues related to coding standards and best practices.
- **Pull Request Reviews**: Require code reviews for all changes, especially those involving CI/CD configuration. This helps ensure that the CI/CD process itself is robust and follows best practices.
- **Artifact Versioning**: Implement versioning for your app's build artifacts, making it easy to track and deploy specific versions of your app when necessary.
- **Containerization**: Use containerization technologies like Docker to create reproducible build and test environments, ensuring consistency in different stages of the CI pipeline.
- **Performance Monitoring**: Integrate performance monitoring tools into your CI/CD process to identify performance regressions and address them proactively.
- **Environment Variables Management**: Safely manage environment variables and secrets used in your CI/CD pipeline, ensuring sensitive information is securely handled.
- **Pipeline Customization**: Customize your CI/CD pipeline to suit your project's specific requirements, incorporating the necessary steps for testing, building, and deployment.
- **Documentation**: Maintain clear and up-to-date documentation for your CI/CD pipeline setup, making it easy for team members to understand and contribute to the process.

## Tools
- **Jenkins**: Jenkins is an open-source automation server that can be used to set up custom CI/CD pipelines for React Native projects. It offers great flexibility and can be tailored to the specific needs of your project. While it's powerful, it may require more configuration and maintenance compared to cloud-based solutions.
- **Travis CI**: Travis CI is a cloud-based CI/CD service that integrates with GitHub repositories. It's easy to set up and configure, making it a good choice for small to medium-sized React Native applications. It provides a straightforward way to automate your build and test workflows.
- **CircleCI**: CircleCI is another cloud-based CI/CD platform that integrates seamlessly with version control systems. It's known for its performance and scalability. CircleCI offers a free tier for open-source projects and small teams, making it a suitable choice for an average React Native app.
- **GitHub Actions**: If your React Native project is hosted on GitHub, GitHub Actions is a built-in CI/CD solution that allows you to define and automate your CI workflows directly in your GitHub repository. It's a convenient choice if you want to keep everything within the GitHub ecosystem. 

	*For an average React Native application, GitHub Actions is recommended due to its ease of integration with GitHub repositories and the convenience of defining CI/CD workflows within the same platform. It's user-friendly and provides ample capabilities for setting up automated build and testing processes.*

## OTHER
- **[Expo App Services](https://expo.dev/eas)**: A set of services and tools provided by Expo, a popular platform for developing React Native applications. EAS streamlines and enhances the development and deployment process of React Native projects built with Expo.
	- [p] Super easy to host and deploy apps, expecially if they're build with Expo
	- [p] Developers provide an option to host the [Expo Build process on your server](https://docs.expo.dev/build-reference/local-builds/), but consequently, it is suited for companies where the project’s code has to be kept private
	- [p] Handles the stressful stuff for you, like signing certificates and keystore files, which saves a lot of engineering time and effort
	- [p] Provides extensive documentation in case you need help
	- [p] Supports both Expo and React Native apps
	- [c] The free tier is limited if builds are frequent
	- [c] During peak hours, you might have to wait a bit for your builds to complete on the free tier, which might be a problem if you’re on a tight deadline
	- [c] As of writing this article, running [E2E tests](https://docs.expo.dev/build-reference/e2e-tests/) is in an early state, though support continues to develop

<br>

 - **[Microsoft App Center](https://appcenter.ms/sign-in?original_url=%2Fapps)**: A CI/CD platform dedicated to app development. Unlike Expo Application Services, it supports both React Native and other cross-platform technologies like Unity and Xamarin.
	 - [p] The free tier is generous. In many cases, it is enough for personal and small-scale projects, but the service also provides a 30-day free trial for their paid tier
	 - [p] Provides clear and exhaustive documentation
	 - [p] Supports end-to-end tests
	 - [p] Widely used in enterprise environments, so extensive support is available from the community
	 - [c] No option to run builds on local infrastructure. As discussed before, this might be a problem in situations where source code privacy is important
	 - [c] Paid option may be too expensive for small startups
	 - [c] E2E tests are locked behind a paywall
	 - [c] As of writing this article, [Microsoft doesn’t support Expo apps](https://github.com/microsoft/appcenter/issues/189)
	 
<br> 

- **[GitHub Actions](https://github.com/features/actions)**: A prominent option among numerous open-source programmers. One reason for its popularity is that this tool integrates with GitHub, so developers can use it to automate their workflows directly from their GitHub repository.
	- [p] The service allows for more control, which means that you can add tests and even change your build agent
	- [p] Its free tier is more than enough for personal projects. Moreover, GitHub even issues [Pro accounts for students](https://education.github.com/pack), which allows them to upgrade to a paid option for free
	- [p] Other than building apps, GitHub Actions can also run [automated code quality checks](https://github.com/marketplace/actions/sonarqube-scan). This is suitable in situations where you want to detect code smells and bugs in your project before deployment
	- [p] The [self-hosted runners feature](https://docs.github.com/en/actions/hosting-your-own-runners/managing-self-hosted-runners/about-self-hosted-runners) allows companies to host their version of Actions on local infrastructure. As discussed before, this is great for private code repositories
	- [p] The free tier allows for [end-to-end tests](https://remarkablemark.org/blog/2023/02/18/how-to-run-react-native-detox-tests-on-github-actions/)
	- [c] The process of building a CI/CD pipeline is too involved. In some cases, it might be too complex for beginners who are looking to deploy their app
	- [c] GitHub Actions does not have dedicated documentation for React Native apps. Because of this, you might have to rely on the community for help

<br>

- **[CodeMagic](https://codemagic.io/start/)**: CI/CD pipeline specifically geared towards mobile app development frameworks, including [Flutter](https://blog.logrocket.com/tag/flutter), Cordova, Ionic, and others
	- [p] Their servers use Apple’s M-series machines, which leads to [rapid build times](https://www.jeffgeerling.com/blog/2021/apple-m1-compiles-linux-30-faster-my-intel-i9)
	- [p] CodeMagic uses a pay-as-you-go model, which means that you only pay for the resources you use. In some cases, this might be a cheaper option as compared to other services in this list
	- [p] Amazing documentation with step-by-step guides
	- [p] Supports [end-to-end tests](https://docs.codemagic.io/yaml-testing/testing/) on the free tier
	- [c] Does not have a self-hosted option, which can be a problem for privacy-sensitive code

<br>

- **Bitrise**: supports [add-ons](https://devcenter.bitrise.io/en/references/bitrise-add-ons.html) to help in development with, for example, [debug reports](https://devcenter.bitrise.io/en/testing/test-reports.html) or [release management](https://devcenter.bitrise.io/en/release-management.html)
	- [p] Rapid build times: Just like CodeMagic, this also supports Apple’s M series machines to compile and build code
	- [p] Pay-as-you-go model: The biggest upside to this service is that you can save money by only paying for the resources you use
	- [p] Supports [end-to-end tests](https://devcenter.bitrise.io/en/testing.html) on the free tier
	- [c] Does not provide a self-hosted option

<br>

- **Jenkins**: Targeted towards enterprises and large businesses. This is because the software is completely self-hosted. This is great for situations where the project’s source code has to be kept private.
	- [p] Completely self-hosted, allows companies to avoid spending money on expensive tiers and instead use local hardware.
	- [c] Maintaining and making sure your Jenkins host remains secure might be a hassle for some teams


## SOURCES
[Best CI/CD tools for React Native](https://blog.logrocket.com/best-ci-cd-tools-react-native/)

