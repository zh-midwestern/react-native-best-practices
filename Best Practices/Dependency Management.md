# DEPENDENCY MANAGMENT

## Bare Minimum
- **Package Manager**: Use a package manager, such as npm (Node Package Manager) or Yarn, to install, update, and manage external dependencies efficiently. It should be configured to fetch and install packages from a central repository.
- **Version Control**: Include a `package.json` file in your version control system to track and share the list of dependencies used in your project. This ensures consistency among team members and across different development environments.
- **Dependency Locking**: Implement dependency locking mechanisms, such as a `yarn.lock` or `package-lock.json` file, to freeze dependency versions and prevent unexpected changes when new versions are released. This helps maintain stability and predictability in your project.

## Best Practices
- **Use a Package Manager**: Utilize a package manager like npm (Node Package Manager) or Yarn to handle dependencies. These tools simplify the installation, updating, and removal of packages and ensure consistency across different development environments.
- **Dependency Versioning**: Specify exact versions or version ranges for your dependencies in the `package.json` file. This helps prevent unexpected breaking changes when new versions are released.
- **Lock Files**: Generate and maintain lock files, such as `package-lock.json` for npm or `yarn.lock` for Yarn. Lock files record the specific versions of packages used in your project, ensuring that every team member uses the same versions.
- **Regular Updates**: Periodically update your project's dependencies to benefit from bug fixes, new features, and security patches. However, be cautious when updating, as it may introduce breaking changes; thoroughly test your application after updates.
- **Peer Dependencies**: Specify peer dependencies in your package.json to indicate which versions of other packages your project is compatible with. This helps maintain compatibility with the broader ecosystem.
- **Security Scanning**: Use security scanning tools like npm audit or Yarn audit to identify and address known security vulnerabilities in your project's dependencies.
- **Linter Configuration**: Integrate dependency management into your linting and code analysis process to ensure that you adhere to best practices and detect issues with dependency usage.
- **Document Dependencies**: Maintain clear and up-to-date documentation about the purpose and usage of each dependency in your project. This aids in onboarding new team members and troubleshooting issues.
- **Prune Unused Dependencies**: Regularly remove unused or redundant dependencies from your project to keep your codebase clean and minimize the size of your application.
- **Test Library Updates**: Create automated tests for your application and dependencies to ensure that updates do not introduce regressions or conflicts. Test critical functionality after each update.
- **Automate Dependency Checks**: Implement automated dependency checks in your Continuous Integration (CI) pipeline to verify that all dependencies are up to date and free from vulnerabilities.

## Tools
- **npm (Node Package Manager)**: npm is the default package manager for Node.js and JavaScript. It's widely used in the React Native ecosystem for managing dependencies. It works well for most React Native projects, offering a vast repository of packages and straightforward integration.
- **Yarn**: Yarn is an alternative package manager that aims to be faster and more reliable than npm. It provides features like caching, workspaces, and deterministic installs. Yarn is a solid choice for larger React Native projects or teams that prefer its features and performance improvements.
- **pnpm**: pnpm is another package manager that prioritizes speed and storage efficiency. It uses a shared store for dependencies, reducing duplication. It's suitable for projects concerned with disk space and seeking fast, consistent installations. 

	*For an average React Native application, npm is recommended due to its familiarity and widespread adoption. It's a dependable choice that provides access to a vast ecosystem of packages.*

### Other
- **[npm (Node Package Manager)](https://www.npmjs.com/package/npm)**: A package manager for the JavaScript programming language. It is the default package manager for the JavaScript runtime environment Node.js. It consists of a command-line client, also called npm, and an online database of public and paid-for private packages called the npm registry.
- **[Yarn](https://yarnpkg.com/)**: It stands for *Yet Another Resource Negotiator* and it is a package manager just like npm. It was developed by Facebook and is now open-source. The intention behind developing yarn(at that time) was to fix performance and security concerns with npm.
- **Differences**:
		- tasks are executed per package and sequentially with npm while yarn executes these tasks in parallel, increasing persormance
		- both offer caching mechanisms, however Yarn seems to do it a bit better by implementing a [zero-install paradigm](https://master--yarn2.netlify.app/features/zero-installs).
