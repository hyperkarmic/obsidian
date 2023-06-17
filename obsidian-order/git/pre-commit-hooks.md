# What are pre-commit hooks?

Pre-commit hooks are scripts that run before code is committed to a repository. They can be written in any language and can be used to automate linting, formatting, testing, and security scanning. You can configure pre-commit hooks to run automatically when You run the `git commit` command.

The primary purpose of pre-commit hooks is to catch issues early in the development process. By running automated tests before committing code, You can catch issues before they become problems. This can help prevent bugs and security vulnerabilities from making their way into production.

# Why use pre-commit hooks?

Pre-commit hooks provide several benefits to You and Your project team:

1.  Catch errors early: Pre-commit hooks catch errors before they are committed to the repository. This helps prevent errors from being propagated throughout the codebase and causing problems later on.
2.  Enforce coding standards: Pre-commit hooks can enforce coding standards and style guidelines, ensuring that all code in the repository is consistent and easy to read.
3.  Ensure code quality: Pre-commit hooks can run tests, lint code, and perform other checks to ensure that code meets quality standards.
4.  Improve security: Pre-commit hooks can scan code for security vulnerabilities, ensuring that sensitive information is protected and that the codebase is secure.

# How to set up pre-commit hooks?

You can set up pre-commit hooks by following these simple steps:

1.  Install a pre-commit hook manager: There are several pre-commit hook managers available, such as [pre-commit](https://pre-commit.com/) and [husky](https://github.com/typicode/husky). These tools make it easy to manage and configure pre-commit hooks. (You can install pre-commit using [asdf-vm](https://asdf-vm.com/). Check out my [Medium story on the WSL](https://medium.com/towardsdev/my-wsl-setup-as-a-cloud-dev-getting-the-best-of-both-worlds-a0b3a74c14ad), where I also talked about asdf-vm.)
2.  Create a pre-commit hook script: Create a script that performs the actions You want to run before committing code. You can use most programming languages like Python or JavaScript for this.
3.  Configure the pre-commit hook manager: Configure the pre-commit hook manager to run Your pre-commit hook script before committing code. If You use pre-commit you only have to add one yaml file for this.
***
![[pre-commit-hook.jpg]]
#pre-commit-hooks
