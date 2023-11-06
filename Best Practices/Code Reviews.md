# CODE REVIEW

## Bare Minimum
- **Clear Review Guidelines**: Establish clear and documented code review guidelines that define expectations for the review process. Guidelines should cover coding standards, best practices, and the review workflow to provide a consistent framework for reviewers and developers.
- **Regular and Timely Reviews**: Ensure that code reviews are conducted regularly and in a timely manner. Delays can disrupt the development process and hinder collaboration. Encourage team members to prioritize reviews and provide constructive feedback promptly.
- **Constructive Feedback Culture**: Foster a culture of constructive feedback and open communication. Encourage reviewers to provide specific feedback and suggestions for improvement rather than focusing solely on identifying issues. Promote a positive and collaborative atmosphere during reviews.

## Best Practices
- **Set Clear Review Objectives**: Clearly define the goals and objectives of each code review. This helps reviewers focus on specific aspects, such as code quality, functionality, or security, and provides context for the review process.
- **Automated Code Analysis**: Integrate code analysis tools (e.g., ESLint) into your development process to catch common issues automatically. These tools can identify issues before they reach the code review stage, saving time and reducing the likelihood of errors.
- **Small, Digestible Changes**: Encourage developers to submit smaller, well-contained code changes that are easier to review. This practice simplifies the review process and allows for a more focused examination of each component.
- **Coding Standards and Guidelines**: Define and adhere to coding standards and guidelines specific to your project. This includes consistent code formatting, naming conventions, and best practices. Use linters and formatters (e.g., ESLint and Prettier) to enforce these standards.
- **Code Ownership and Author Feedback**: Assign code ownership to team members, allowing specific individuals to review code related to their areas of expertise. Encourage authors to respond to feedback and participate in discussions during the review process.
- **Use a Code Review Checklist**: Develop a code review checklist that includes items to evaluate in every review, such as code quality, functionality, documentation, and adherence to best practices.
- **Peer Reviews**: Promote peer reviews where team members with different perspectives and expertise review each other's code. This diversity of viewpoints can uncover issues and improve the overall quality of the code.
- **Automated Testing**: Ensure that code changes include relevant unit tests or integration tests. Automate testing processes as part of your CI/CD pipeline to verify that code modifications do not introduce regressions.
- **Continuous Integration (CI)**: Integrate code reviews with your CI system to automatically trigger checks and tests upon code submission. This ensures that code changes meet quality and stability standards.
- **Documentation**: Document code review discussions, decisions, and any additional context that arises during the review process. This information can serve as a valuable resource for team members in the future.
- **Consistent Feedback Format**: Encourage reviewers to provide feedback in a consistent and structured format. This makes it easier for developers to understand and address feedback.
- **Respectful and Constructive Feedback**: Promote a culture of respect and constructive criticism during code reviews. Focus on improving code quality rather than criticizing the author. Encourage reviewers to offer suggestions and solutions along with issue identification.
- **Regular Review Meetings**: Consider holding regular code review meetings or sessions to discuss complex or critical code changes. These meetings can facilitate in-depth discussions and knowledge sharing.

## Tools
- **GitHub Pull Requests**: If your React Native project is hosted on GitHub, using its built-in pull request (PR) feature is a convenient choice. It allows for code review, discussions, and integrations with CI/CD tools. GitHub Actions can be used for automated testing.
- **GitLab Merge Requests**: For projects hosted on GitLab, Merge Requests (MRs) offer similar functionality to GitHub pull requests. They enable code review, collaboration, and integration with GitLab CI/CD pipelines.
- **Bitbucket Pull Requests**: Bitbucket provides pull request functionality for code reviews, along with features like inline commenting and integration with Bitbucket Pipelines for CI/CD.
- **Review Board**: Review Board is a code review tool that can be self-hosted or used as a hosted service. It supports reviewing changes in various version control systems, including Git.
- **Phabricator**: Phabricator is an open-source code review and collaboration platform. It offers features for code review, task management, and more. You can self-host Phabricator or use a hosted version provided by Phacility.
- **CodeStream**: CodeStream is an extension for popular code editors like VS Code, enabling in-line discussions and code reviews. It integrates with various version control platforms and can be suitable for smaller teams.
- **Crucible**: Crucible by Atlassian is a code review tool that works well with Jira and other Atlassian products. It provides a platform for reviewing code and documenting feedback. 


## Other
- Commits
		- [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/)
		- [descriptive messages](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/)
- [Pull Request Best Practices ](https://rewind.com/blog/best-practices-for-reviewing-pull-requests-in-github/)