Okay, here's the `CONTRIBUTING.md` (Contributor Guide) for your project, written in English. This file is essential for any open-source project on GitHub, as it provides the necessary guidelines for others to collaborate effectively.

It focuses on a clear workflow, best practices, and how to maintain project consistency.

-----

# Saika Suite Contributor Guide

Thank you for your interest in contributing to Saika Suite\! Your support is fundamental to making this project a powerful and accessible tool for the Cuban community and beyond.

This guide will help you understand how you can contribute, what we expect from your contributions, and how to maintain the quality and consistency of the codebase.

## 1\. Code of Conduct

Before you begin, please review our [Code of Conduct](https://www.google.com/search?q=CODE_OF_CONDUCT.md). We are committed to fostering an open and welcoming environment. As contributors, we pledge to make participation in our project and our community a harassment-free experience for everyone, regardless of age, body size, visible or invisible disability, ethnicity, sex characteristics, gender identity and expression, level of experience, education, socio-economic status, nationality, personal appearance, race, religion, or sexual identity and orientation.

## 2\. How to Contribute?

There are many ways to contribute to Saika Suite, not just by writing code:

  * **Report Bugs**: If you find an error, please report it. A good bug description is invaluable.
  * **Suggest Features**: Share your ideas for new functionalities or improvements.
  * **Improve Documentation**: Clear and accurate documentation is vital. Help us improve it.
  * **Write Code**: Implement new features, fix bugs, or improve existing code.
  * **Translate**: Help translate the application and documentation into other languages.
  * **Testing**: Help test new features or verify bug reports.
  * **Feedback**: Use the application and give us your opinion. Your experience is important\!

## 3\. Where to Start?

  * **Open Issues**: Check the [Issues](https://www.google.com/search?q=https://github.com/SaikaNET-Studio/saika-suite/issues) section on GitHub. Look for labels like `good first issue`, `bug`, `enhancement`, or `help wanted`.
  * **Discussions**: Join discussions in the repository or on SaikaNET Studio's communication channels (if any).

## 4\. Reporting Bugs

If you find a bug:

1.  **Search first:** Before creating a new issue, search to see if a similar report already exists.
2.  **Use the template:** Open a new issue and select the `bug_report.md` template.
3.  **Describe the problem:**
      * **Steps to reproduce:** Explain how to replicate the bug, step by step.
      * **Expected vs. observed behavior:** Describe what you expected to happen and what actually occurred.
      * **Saika Suite version and your operating system:** Indicate which software version you are using and on which operating system (Windows, Android, Linux).
      * **Screenshots or videos:** If possible, attach images or videos that illustrate the problem.
      * **For offline errors:** If the error occurs offline, use the `feedback_offline.md` template to describe the conditions.

## 5\. Suggesting Features

If you have an idea for a new feature:

1.  **Search first:** Make sure the feature hasn't been suggested already.
2.  **Use the template:** Open a new issue and select the `feature_request.md` template.
3.  **Describe the feature:** Clearly explain the idea, why you think it's useful, and how it would benefit users.

## 6\. Code Contributions

To submit code changes, follow these steps:

1.  **Fork the Repository:** Create your own copy (fork) of the Saika Suite repository on GitHub.
2.  **Clone Your Fork:**
    ```bash
    git clone https://github.com/YOUR_USERNAME/saika-suite.git
    cd saika-suite
    ```
3.  **Create a Branch:** Create a new branch for your changes. Use a descriptive name (e.g., `feature/new-function-x` or `bugfix/fix-error-y`).
    ```bash
    git checkout -b feature/your-feature-name
    ```
4.  **Set Up Your Development Environment:** Ensure you have Python 3.x and all dependencies installed. Refer to the `README.md` for more details.
    ```bash
    pip install -r requirements.txt
    # Optional, if applying changes to specific platforms:
    # pip install -r requirements_android.txt
    # pip install -r requirements_linux.txt
    ```
5.  **Make Your Changes:** Implement your improvements or corrections. Follow existing coding conventions in the project.
      * **Modularity:** Keep the code well-modularized, following the structure defined in `src/`.
      * **Comments:** Comment your code when necessary to explain complex logic.
      * **Tests:** If you add new features, consider writing unit tests for them in the `tests/unit/` directory.
6.  **Commit Your Changes:** Make clear and atomic commits. Each commit should represent a logical change.
    ```bash
    git add .
    git commit -m "feat: Add new function X for SaikaPlay module"
    # or
    git commit -m "fix: Fix download error in SaikaGrab on resume"
    ```
7.  **Push Your Branch:**
    ```bash
    git push origin feature/your-feature-name
    ```
8.  **Create a Pull Request (PR):**
      * Go to your forked repository on GitHub, and you will see an option to create a Pull Request from your branch to the `main` branch of the original Saika Suite repository.
      * **PR Title:** Should be clear and concise, summarizing the change.
      * **PR Description:** Explain the changes made in detail, why they are necessary, and if it resolves any existing issues (link the issue using `#` followed by the number, e.g., `#123`).
      * **Screenshots/Videos:** If the changes are visual, include demonstrations.

### Code Guidelines

  * **PEP 8:** We strive to follow [PEP 8](https://peps.python.org/pep-0008/) coding style guidelines.
  * **Variable and Function Names:** Use descriptive, `snake_case` names.
  * **Separation of Concerns:** Each module and function should have a clear, single responsibility.
  * **Internationalization (i18n):** If your change involves user-visible text, ensure it is "i18n-ready" (ready for translation), using the mechanisms we define for this in `src/core/utilities/i18n.py`.

## 7\. Pull Request Review Process

Once you submit your Pull Request:

  * The SaikaNET Studio team will review it.
  * We may request changes, improvements, or clarifications.
  * Be patient and responsive to feedback; review is a collaborative process to improve the software.
  * Once approved, your changes will be merged into the `main` branch.

## 8\. License

By contributing to Saika Suite, you agree that your contributions will be licensed under the same conditions as the main project. Please review our [LICENSE](https://www.google.com/search?q=LICENSE) file for more details.

We look forward to your contributions and thank you for your support in building an even better Saika Suite\!

-----
