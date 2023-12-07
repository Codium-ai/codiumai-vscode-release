<div align="center">

# CodiumAI - Meaningful tests for busy devs  
[![Twitter URL](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://twitter.com/CodiumAI)    [![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/kG35uSHDBc)    [![Twitter URL](https://img.shields.io/badge/TikTok-000000?style=for-the-badge&logo=tiktok&logoColor=white)](https://www.tiktok.com/@codiumai)
---

**CodiumAI** analyzes your code and generates meaningful tests to catch bugs before you ship. With CodiumAI, you can easily and quickly create comprehensive test suites that help you ensure the reliability and correctness of your software. It supports all languages!

---

</div>

<!-- Table of Contents -->
## Table of Contents
1. [SUPPORTS ALL PROGRAMMING LANGUAGES](#supports-all-programming-languages)
2. [Explore our new CodiumAI Chat](#explore-our-new-codiumai-chat)
3. [🌟 NEW! Explore two of our upcoming Teams plan features, available for a limited time!](#-new-explore-two-of-our-upcoming-teams-plan-features-available-for-a-limited-time)
   - [Prepare for Pull Request using our new CodiumAI Chat!](#prepare-for-pull-request-using-our-new-codiumai-chat)
   - [Extend your current test suites](#extend-your-current-test-suites)
4. [Features](#features)
   - [🤖 Generate unit tests suite automatically](#-generate-unit-tests-suite-automatically)
   - [🔬 Analyze your code](#-analyze-your-code)
   - [💡 Suggest code modifications to improve the performance and correctness of your code](#-suggest-code-modifications-to-improve-the-performance-and-correctness-of-your-code)
   - [💫 Find potential bugs in your code and suggest ways to fix them](#-find-potential-bugs-in-your-code-and-suggest-ways-to-fix-them)
   - [📄 Add docstring automatically and enhance your code](#-add-docstring-automatically-and-enhance-your-code)
   - [🚀 Help you improve code quality](#-help-you-improve-code-quality)
5. [How to use CodiumAI?](#how-to-use-codiumai)
   - [TL;DR:](#tldr)
   - [Generate tests](#generate-tests)
   - [Review the results](#review-the-results)
   - [Explore behavior coverage](#explore-behavior-coverage)
      - [Add tests for uncovered behavior](#add-tests-for-uncovered-behavior)
      - [Add more behaviors](#add-more-behaviors)
   - [Modify tests](#modify-tests)
   - [Run your tests and find possible bugs in your code](#run-your-tests-and-find-possible-bugs-in-your-code)
   - [Change test suite configurations](#change-test-suite-configurations)
   - [Save your test suite](#save-your-test-suite)
   - [CodiumAI Chat - NEW!](#codiumai-chat---new)
      - [Explain your code](#explain-your-code)
      - [Enhance your code](#enhance-your-code)
      - [Generate Docstring](#generate-docstring)
      - [Get improvement suggestions](#get-improvement-suggestions)
   - [Report a bug](#report-a-bug)
6. [How to uninstall](#how-to-uninstall)
7. [Links](#links)
8. [Terms of use](#terms-of-use)


## **SUPPORTS ALL PROGRAMMING LANGUAGES**

### Generate tests using CodiumAI:

![How it works](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/Tests-Gif.gif)

### You can also trigger CodiumAI by right-clicking and choosing CodiumAI:

![How it works](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/all-lang-vscode-gif.gif)

_Beta Version - Supported in VSCode version 1.70.0 and above_

---

## Explore our new [CodiumAI Chat](https://github.com/Codium-ai/codiumai-vscode-release#codiumai-chat---new)! 

## 🌟 NEW! Explore two of our upcoming [Teams plan](https://www.codium.ai/pricing/) features, available for a limited time!

### Prepare for Pull Request using our new CodiumAI Chat!
Easily get PR descriptions, automated reviews for your PR, automatic commit messages, and branch-diff improvement suggestions before opening your pull request.
Try out our new chat feature today! See how it works:

![PrePR](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/prepr.gif)


### Extend your current test suites 
Already have a test suite? Let CodiumAI help you with adding missing tests to it! Currently supporting Python, JS and TS.
See how it works:

![Extend Test Suite](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/extend-test-suite.gif)

---

## Features

#### 🤖 Generate unit tests suite automatically

#### 🔬 Analyze your code

#### 💡 Suggest code modifications to improve the performance and correctness of your code

#### 💫 Find potential bugs in your code and suggest ways to fix them

#### 📄 Add docstring automatically and enhance your code

#### 🚀 Help you improve code quality

By creating comprehensive test suites, our tool helps you catch and fix bugs early and ensures that your code is reliable and maintainable.

---

## How to use CodiumAI?

#### TL;DR:

- Click on the `CodiumAI` button above a function/class/method name
- Use CodiumAI chat to get code explanation, enhance your code, add docstring and get improvement suggestions to your code.
- Use CodiumAI's keybinding shortcut - mac: `cmd+ctrl+c` | Linux: `alt+shift+c` | windows: `ctrl+win+z`
- Right-click on your code -> Choose `CodiumAI - ` and choose the desired command
- Or just use the command palette and select `CodiumAI - Generate Tests`

---


### Generate tests

Generate tests for a function, a class, or a method using the `Test this class/function/method` button above a function/class/method name:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/GenerateTests.png)

Generate tests for code snippets by selecting the code you want to test, right-clicking on it, choosing the `CodiumAI - ` and selecting the desired command:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/GenerateTestsForSnippet.png)

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/all-languages-vscode.gif)

##### Watch tutorial -> https://youtu.be/BxFuKFX_KSA

#### Review the results

CodiumAI tab will present the test results - review the test names, objectives, types, and the test code:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ReviewResults.png)

### Explore behavior coverage

CodiumAI generates a behavior list of your code and marks each behavior as covered or not covered based on the generated test.
The number of covered behaviors calculates the coverage percentages.
You can refresh the coverage when you modify your test suite (add, remove, or modify tests):

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/BehaviorCoverage.png)

For each behavior, explore its sub-behaviors for more test variations:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/SubBehaviors.png)

#### Add tests for uncovered behavior

For behaviors that are not covered by tests, you can click on the `Generate test` button next to it, and CodiumAI will generate a test
for this behavior.

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/AddTestForBehavior.png)

#### Add more behaviors

Missing a behavior? Simply add new behaviors and generate tests for them:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/AddBehavior.png)

##### Watch tutorial -> https://youtu.be/xHwIvCjvQDI

#### Modify tests

Want to modify a single test code? Simply type the change you want inside the `Suggest changes..` field, and TestGPT will modify the code based on your request:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/SuggestChanges.png)

You can also click the `Regenerate` button and get an alternative code for this test:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/RegenerateSingleTest.png)

You can manually edit the test within the panel:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ManualEditTest.png)

Want more tests? Click on `Give me more tests` at the bottom of the test suite:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/RequestMoreTests.png)

You can focus on code changes from your uncommitted changes, read the code explanation of your changes and generate tests for them:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/CodeChanges.png)

Want to remove a test from your test suite? Click on the `delete` button on each test:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/DeleteSingleTest.png)

#### Run your tests and find possible bugs in your code

You can run the generated tests directly from the CodiumAI panel. Simply click `Run All Tests` button to run all the test, or `Run` button on each single test:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/RunYourTests.png)

The test failed? See the log by clicking the `failed` button, and easily fix the test by clickeing `Fix Test` button:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/FixTest.png)

When TestGPT identifies possible bug in your code, it alerts you and gives you relevant information on the bug and possible fix, click on `Possible Code Bug` to see the data:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/PossibleCodeBug.png)

Click `Fix Code` to get a possible fix to your bug:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/FixCode.png)

After analyzing, click `Review Fix` button to see the code diff:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ReviewFix.png)

Review the suggested fix, and if you approve it, click `Apply to my Code` button merge it to your code:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ApplyFix.png)

##### Watch tutorial -> https://youtu.be/l_ITy2_KDZ0

#### Change test suite configurations

Improve and personalize your test suite by giving general instructions, providing examples of tests and selecting your preferred testing framework in the `Configuration` section:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/AddTestExample.png)
![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ChangeGeneralConfiguration.png)
![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ModifyFramework.png)

#### Save your test suite

When you're happy with your generated test suite, you can click on `Copy tests` and copy the test suite code, or click on `Open as a file` and we will create a test file for you:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/OpenCopy.png)

### CodiumAI Chat - NEW!

Use our chat commands to improve your code! See how it works:

![How it works](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/chat-gif.gif)

#### Explain your code

Get a detailed code explanation on every component or code snippet you want, using CodiumAI chat command /explain:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/explain.png)

#### Enhance your code

Choose the component you want to enhance, or select the relevant lines, and choose /enhance command in our CodiumAI chat. You can add additional instructions as a free text.

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/enhance.png)

#### Generate Docstring

Choose the component you want to add docstring to, or select the relevant lines, and choose /docstring command in our CodiumAI chat. You can add additional instructions as a free text.

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/docstring.png)

#### Get improvement suggestions

Get suggestions to improve your code correctness and robustness, by choosing /improve command in CodiumAI chat. You can add additional instructions as a free text.

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/improve.png)




### Report a bug

Had a bug with CodiumAI? Report us via email (support@codium.ai), [Discord](https://discord.gg/kG35uSHDBc) or open a [GitHub issue](https://github.com/Codium-ai/codiumai-vscode-release/issues), and provide us with your request ID. You can copy it from the CodiumAI panel:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/SendRequstID.png)


---

> Tip 1: If you can't see the `Generate Tests` button you might have to set `"editor.codeLens": true,` in your VSCode configuration file.
> <br>

> Tip 2: You can show and hide CodiumAI panel in the extension settings or from the command palette.
> <br>

---

## How to uninstall

1. Select "CodiumAI" button in the bottom status bar.
2. Hover over the authentication notification, select the settings icon and "Manage Extension" option from the dropdown.
3. CodiumAI Extension will open in a new tab. Select Uninstall and Reload VSCode.

## Links

[![Join our Discord community](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/Joincommunity.png)](https://discord.gg/kG35uSHDBc)

- Discord community: https://discord.gg/kG35uSHDBc
- CodiumAI site: https://codium.ai
- Blog: https://www.codium.ai/blog/
- Troubleshooting: https://www.codium.ai/blog/technical-faq-and-troubleshooting/
- Support: support@codium.ai

## Terms of use

- Terms of use: https://www.codium.ai/terms
- Privacy policy: https://www.codium.ai/privacy-policy
- Please notice - similar to other popular generative-AI tools (such as copilot), we also transmit code snippets to our servers.
