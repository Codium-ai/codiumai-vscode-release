<div align="center">
<div align="center">

# CodiumAI - Meaningful tests for busy devs

</div>

[![Discord](https://badgen.net/badge/icon/discord?icon=discord&label&color=purple)](https://discord.gg/kG35uSHDBc)

---

**CodiumAI** analyzes your code and generates meaningful tests to catch bugs before you ship. With CodiumAI, you can easily and quickly create comprehensive test suites that help you ensure the reliability and correctness of your software. Supports Python, Javascript and Typescript.

---

</div>

![How it works](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/v04-qa9.gif)

_Beta Version - Supported in VSCode version 1.70.0 and above_

## Features

#### 🤖 Generates unit tests suite automatically

#### 🔬 Analyzes your code

#### 💡 Suggests code modifications to improve the performance and correctness of your code

#### 💫 Finds potential bugs in your code and suggests ways to fix them

#### 🚀 Helps you improve code quality

By creating comprehensive test suites, our tool helps you catch and fix bugs early, and ensures that your code is reliable and maintainable.

---

## Supported languages

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/supported.png)

---

## How to use CodiumAI?

> #### TL;DR:

> - Click on the `Generate Tests` button above a function/class/method name
> - Use CodiumAI side panel to generate tests for a function/class/method
> - Use CodiumAI's keybinding shortcut - mac: `cmd+ctrl+c` | linux: `alt+shift+c` | windows: `ctrl+win+z`
> - Select code -> right click -> Choose "CodiumAI - Generate Tests"
> - Or just use the command palette and select "CodiumAI - Generate Tests"

#### Generate tests

Generate tests for a function or a class, using the `Test this class/function/method` button above a function/class/method name:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/GenerateTests.png)

Generate tests for code snippet, by selecting the code you want to test, right-click on it and choose `CodiumAI - Generate Tests` option:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/GenerateTestsForSnippet.png)

##### Watch tutorial -> https://youtu.be/BxFuKFX_KSA

#### Review the results

CodiumAI tab will present the test results - review the test names, objectives, types, and the test code:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ReviewResults.png)

#### Quick Actions - Generate tests for behavior

Quickly generate tests from behaviors using Quick Actions - Click on the CodiumAI panel on the left, choose the behavior you want to generate tests for, 
and get the generated test inside your editor.

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/QuickActions-Tests.png)

#### Explore behavior coverage

CodiumAI generates a behavior list of your code and marks each behavior as covered or not covered based on the generated test.
The coverage percentages are calculated by the number of covered behaviors.
You can refresh the coverage when you modify your test suite (add, remove, or modify tests):

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/BehaviorCoverage.png)

#### Add test for uncovered behavior

For behaviors that are not covered by tests, you can click on the "Generate test" button next to it, and CodiumAI will generate a test
for this behavior.

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/AddTestForBehavior.png)

#### Add more behaviors

Missing a behavior? Simply add new behaviors and generate tests for them:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/AddBehavior.png)

##### Watch tutorial -> https://youtu.be/xHwIvCjvQDI 

#### Modify tests

Want to modify a single test code? Simply type the change you want inside the `Suggest changes..` field, and TestGPT will modify the code based on your request:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/SuggestChanges.png)

Want to modify the objective of a single test? Edit the name or the objective of a single test, and click regenerate:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ModifyObjective.png)

You can also just click the `Regenerate` button, without changing the test description, and get an alternative code for this test:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/RegenerateSingleTest.png)

You can manually edit the test within the panel:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ManualEditTest.png)

Want more tests? Click on `Give me more tests` at the bottom of the test suite:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/RequestMoreTests.png)

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

Improve and personalize your test suite by giving general instructions, example of tests and select your preferred testing framework in the `Configuration` section:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/AddTestExample.png)
![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ChangeGeneralConfiguration.png)
![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ModifyFramework.png)

#### Save your test suite

When you're happy with your generated test suite, you can click on `Copy tests` and copy the test suite code, or simply click on `Open as a file` and we will create a test file for you:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/OpenCopy.png)

#### Code analysis

Read your code analysis written by our TestGPT model, you can use it for documentation and to make sure your code is doing what it should. Click on the `Code Analysis` tab and find out:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/CodeAnalysis.png)

#### Code suggestions

Our TestGPT model can find some insights about your code and suggests some modifications that you can apply to your code (to improve performance, correctness, and more). Click on the `Code Suggestions` tab and find out:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/CodeSuggestions.png)

Choose the suggestion you want to apply, and merge them to your code:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/MergeSuggestions.png)

#### Quick Actions - Code Suggestions

Quickly get code suggestions from your code using Quick Actions - Click on the CodiumAI panel on the left, click on the "Get code suggestions for this class" option,
and get suggestions from your editor as comments

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/QuickActions-CodeSuggestions.png)

##### Watch tutorial -> https://youtu.be/yK713au2MJk

### Report a bug

Had a bug with CodiumAI? Report us via email (support@codium.ai), [Discord](https://discord.gg/kG35uSHDBc) or open a [GitHub issue](https://github.com/Codium-ai/codiumai-vscode-release/issues), and provide us with your request ID. You can copy it from the CodiumAI panel:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/SendRequstID.png)

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
