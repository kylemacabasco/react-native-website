---
title: How to Contribute Code
---

Thank you for your interest in contributing to React Native! From commenting on and triaging issues, to reviewing and sending PRs, [all contributions are welcome](/contributing/overview). In this document, we'll cover the steps to contributing code to React Native.

## Prerequisites

:::info
Please refer to the [Environment Setup](/docs/environment-setup) guide to setup required tools and the development environment based on the platform us use and platform which you want to develop for.
:::

## For First Time Contributors 

Hello first contributors! Thanks for your interest in contributing to React Native! In this document, we'll cover the very first step on how to get your first ever issue assigned to you! We know that looking at the repository is very overwhelming, so we would like to make this a seamless experience for users. 

First, we have a list of [`good first issues`](https://github.com/facebook/react-native/labels/good%20first%20issue) that include bugs with relatively limited scope. Please look through to see which issue stands out to you. 

After you click on an issue that you are interested in, check to see if anyone else is already assigned to this issue. An example of this would be this [`issue that has 65 different task`](https://github.com/facebook/react-native/issues/34872) that includes a brief description of what needs to be done and how to test the code correctly. As you get to see the many different task that are open, you finally get the courage to get assigned to one of the tasks. 

In order to get assigned to this issue as a collaborator, you would need to write a message (scroll to the bottom of the page) saying that you would like to help or work on a particular task that you picked, just like this [`example`](https://github.com/facebook/react-native/issues/34872#issuecomment-1268417038). After that, the user that open that issue will assign you as a contributor to that issue.  However, if you like to help out another contributor with their issue, you just have to ask if they are willing to collaborate. Please do not be nervous to ask other users if you would like to help since this is what we are all here for! 

Then you would follow the following steps stated on [`Contributing Overview`](/contributing/overview), which is summarized as follows:

1. Fork the React Native repository and create your branch from `main`.
2. Make the desired changes to React Native sources. Use the `packages/rn-tester` app to test them out.
3. If you've added code that should be tested, add tests.
4. If you've changed APIs, update the documentation, which lives in [separate repo](https://github.com/facebook/react-native-website/).
5. Ensure the test suite passes, either locally or on CI once you opened a pull request.
6. Make sure your code lints (for example via `yarn lint --fix`).
7. Push the changes to your fork.
8. Create a pull request to the React Native repository.
9. Review and address comments on your pull request.
10. A bot may comment with suggestions. Generally we ask you to resolve these first before a maintainer will review your code.
11. If changes are requested and addressed, please [request review](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review) to notify reviewers to take another look.
12. If you haven't already, please complete the [Contributor License Agreement](/contributing/contribution-license-agreement) ("CLA"). **[Complete your CLA here.](https://code.facebook.com/cla)**

Please see below for more detailed workflow that is necessary to do these steps correctly. 

## Development Workflow

After cloning React Native, open the directory and run `yarn` to install its dependencies.

Now you are set up to run several commands:

- `yarn start` starts the Metro packager server.
- `yarn lint` checks the code style.
- `yarn format` automatically formats your code.
- `yarn test` runs the Jest-based JavaScript test suite.
  - `yarn test --watch` runs an interactive JavaScript test watcher.
  - `yarn test <pattern>` runs JavaScript tests with matching filenames.
- `yarn flow` runs the [Flow](https://flowtype.org/) typechecks.
  - `yarn flow-check-android` does a full Flow check over `*.android.js` files.
  - `yarn flow-check-ios` does a full Flow check over `*.ios.js` files.
- `yarn test-typescript` runs the [TypeScript](https://www.typescriptlang.org/) typechecks.
- `yarn test-ios` runs the iOS test suite (macOS required).

## Testing your Changes

Tests help us prevent regressions from being introduced to the codebase. We recommend running `yarn test` or the platform-specific scripts above to make sure you don't introduce any regressions as you work on your change.

The GitHub repository is [continuously tested](/contributing/how-to-run-and-write-tests#continuous-testing) using CircleCI, the results of which are available through the Checks functionality on [commits](https://github.com/facebook/react-native/commits/main) and pull requests.

You can learn more about running and writing tests on the [How to Run and Write Tests](/contributing/how-to-run-and-write-tests) page.

## Coding Style

We use Prettier to format our JavaScript code. This saves you time and energy as you can let Prettier fix up any formatting issues automatically through its editor integrations, or by manually running `yarn run prettier`. We also use a linter to catch styling issues that may exist in your code. You can check the status of your code styling by running `yarn run lint`.

However, there are still some styles that the linter cannot pick up, notably in Java or Objective-C code.

### Objective-C

- Space after `@property` declarations
- Brackets on _every_ `if`, on the _same_ line
- `- method`, `@interface`, and `@implementation` brackets on the following line
- _Try_ to keep it around 80 characters line length (sometimes it's not possible...)
- `*` operator goes with the variable name (e.g. `NSObject *variableName;`)

### Java

- If a method call spans multiple lines closing bracket is on the same line as the last argument.
- If a method header doesn't fit on one line each argument goes on a separate line.
- 100 character line length

## Sending a Pull Request

Code-level contributions to React Native generally come in the form of [a pull request](https://help.github.com/en/articles/about-pull-requests). The process of proposing a change to React Native can be summarized as follows:

1. Fork the React Native repository and create your branch from `main`.
2. If you've added code that should be tested, add tests.
3. If you've changed APIs, update the documentation.
4. Ensure the test suite passes, either locally or on CI once you opened a pull request.
5. Make sure your code lints (for example via `yarn lint --fix`).
6. Push the changes to your fork.
7. Create a pull request to the React Native repository.
8. Review and address comments on your pull request.
9. A bot may comment with suggestions. Generally we ask you to resolve these first before a maintainer will review your code.
10. If you haven't already, submit the [Contributor License Agreement ("CLA")](#contributor-license-agreement).

If all goes well, your pull request will be merged. If it is not merged, maintainers will do their best to explain their reasoning.

If this is your first time sending a pull request, we have created a [step-by-step guide to help you get started](contributing/how-to-open-a-pull-request). For more detailed information on how pull requests are handled, see the [Managing Pull Requests page](Managing-Pull-Requests).

### Contributor License Agreement

In order to accept your pull request, we need you to submit a [Contributor License Agreement (CLA)](/contributing/contribution-license-agreement). You only need to do this once to work on any of Meta's open source projects. It only takes a minute, so you can do it while you wait for your dependencies to install.

## License

By contributing to React Native, you agree that your contributions will be licensed under the [LICENSE](https://github.com/facebook/react-native/blob/main/LICENSE) file in the root directory of the React Native repository.
