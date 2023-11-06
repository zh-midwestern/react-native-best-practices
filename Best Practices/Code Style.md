# CODE STYLE

## Bare Minimum
- **Coding Guidelines**: Establish and document clear coding guidelines that define how code should be formatted and structured. Include rules for naming conventions, indentation, and code organization.
- **Linter Configuration**: Implement a linter, such as ESLint, with a defined set of rules that enforce the coding guidelines. Use a tool like Prettier in conjunction with ESLint to automatically format the code to adhere to the guidelines.
- **Enforce Code Reviews**: Incorporate code reviews as an essential part of your development process. Ensure that team members review and provide feedback on code changes to maintain code style consistency.

## Best Practices
- **Consistent Formatting**: Adopt a consistent code formatting style using tools like Prettier to automatically format code. Ensure uniform use of indentation, spacing, and line breaks.
- **Naming Conventions**: Define clear naming conventions for variables, functions, classes, and components. Follow established conventions, such as camelCase for variables and PascalCase for component names.
- **File Structure**: Organize project files and directories logically. Maintain a consistent file structure, separating components, screens, and utility functions, to enhance code organization.
- **Comments and Documentation**: Include clear and concise comments in the code to explain complex logic, functions, and components. Additionally, generate documentation for your code to facilitate understanding and maintenance.
- **Consistent Imports**: Enforce consistent import statements by specifying the order of imports, separating third-party and custom modules, and avoiding unused imports.
- **Descriptive Component Names**: Choose descriptive names for React Native components to make their purpose clear. Use meaningful names that reflect the component's functionality.
- **Redux Code Style**: If using Redux for state management, follow consistent patterns for actions, reducers, and selectors. Maintain a predictable state structure and action naming.
- **Error Handling**: Implement consistent error handling practices, such as using try-catch blocks for handling exceptions and providing meaningful error messages.
- **Testing**: Follow consistent practices for writing test cases, including structuring test files, using test suites, and providing descriptive test names. Ensure that test code aligns with coding guidelines.
- **Linting Rules**: Set up a linting tool like ESLint with a configuration that enforces code style rules. Customize the rules to match your project's coding guidelines.
- **Version Control Integration**: Include code style configurations in version control and ensure that all team members adhere to the same code style rules. Use tools like pre-commit hooks to enforce code style before committing changes.
- **Continuous Integration**: Integrate code style checks into your Continuous Integration (CI) pipeline to ensure that code adheres to coding guidelines with every code change.

## Tools
- **ESLint**: ESLint is a popular JavaScript linter that allows you to define and enforce coding rules and standards. It can be configured for React Native development, and you can choose from various ESLint configurations tailored to your needs.
- **Prettier**: Prettier is a code formatter that automatically enforces a consistent code style by reformatting your code. It works well in conjunction with ESLint to ensure consistent code formatting.
- **Airbnb's ESLint Config**: The Airbnb ESLint config provides a widely adopted set of coding guidelines for JavaScript and React. It includes rules for React Native development and is a solid choice for maintaining code consistency.
- **StandardJS**: StandardJS is an opinionated code style and linting tool that enforces a strict set of rules for code formatting. While it's quite rigid, it can be a good choice for those who prefer minimal configuration. 

	*For an average React Native application, I recommend using ESLint in combination with Prettier. This combination allows you to enforce coding guidelines while also automatically formatting your code to adhere to those guidelines. Additionally, consider using a popular ESLint configuration like Airbnb's to benefit from well-established standards.*

## NAMING CONVENTION
### File Naming Conventions:
1. **Components**:
	- Use PascalCase (also known as UpperCamelCase) for component file names. For example, `MyComponent.js` or `CustomButton.js`.
1. **Screens**:
    - Similarly, use PascalCase for screen file names. For example, `HomeScreen.js` or `ProfileScreen.js`.
3. **Helpers/Utilities**:
    - Use camelCase for utility files, like `apiUtils.js` or `dateHelpers.js`.
4. **Stylesheets**:
    - When creating stylesheets for components or screens, use the same name as the corresponding component or screen but in kebab-case. For example, if you have a component named `MyComponent`, the stylesheet should be named `my-component-styles.js`.
5. **Configuration/Constants**:
    - Use camelCase for configuration or constant files. For example, `appConfig.js` or `apiConstants.js`.
6. **Tests**:
    - For test files, use the same name as the file being tested and append `.test.js` or `.spec.js`. For example, if you're testing `MyComponent.js`, the test file can be named `MyComponent.test.js`.

### Variable Naming Conventions:
1. **Camel Case**:
    - Use camelCase for variable names. For example, `myVariable` or `userDetails`.
2. **Constants**:
    - Use uppercase with underscores to denote constants. For example, `API_KEY` or `MAX_COUNT`.
3. **Function Names**:
    - Use descriptive and clear function names in camelCase. For example, `getUserData` or `calculateTotalPrice`.
4. **Boolean Variables**:
    - Prefix boolean variable names with "is," "has," or "should" to make their intent clear. For example, `isLoading`, `hasError`, or `shouldShowModal`.
5. **Props**:
    - When using props in your components, follow the same camelCase convention as regular variables. For example, `userName` or `isVisible`.
6. **State Variables**:
    - When using state in your components, prefix state variable names with "state." For example, `stateCount` or `stateData`.
7. **Event Handlers**:
    - For event handlers, use camelCase and prefix with "on." For example, `onPressButton` or `onChangeText`.
8. **Arguments and Parameters**:
    - Use camelCase for function arguments and parameters. For example, `function calculateTotalPrice(orderAmount)`.