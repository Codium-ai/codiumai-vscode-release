# CodiumAI - Meaningful tests for busy devs

---
> CodiumAI analyzes your code and generates meaningful tests to catch bugs before you ship. With CodiumAI, you can easily and quickly create comprehensive test suites that help you ensure the reliability and correctness of your software. Supports Python, Javascript and Typescript.
---

![How it works](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/v04-qa9.gif)

_Beta Version - Supported in VSCode version 1.70.0 and above_

## Features

#### 🤖 Generates unit tests suite automatically

#### 🔬 Analyzes your code

#### 💡 Suggests code mofications to improve the performance and correctness of your code

#### 🚀 Helps you improve code quality

By creating comprehensive test suites, our tool helps you catch and fix bugs early, and ensures that your code is reliable and maintainable.

---

## Supported languages

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/supported.png)

---

## How to use CodiumAI?

#### Generate tests 
Generate tests for a function or a class, using the `Generate tests` button above a function/class name, or using CodiumAI panel and choose the desired function/class:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/GenerateTests.png)

#### Review the results
CodiumAI tab will present the test results - review the test names, objectives, types, and the test code:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ReviewResults.png)

#### Modify tests
Want to modify a single test code? Simply type the change you want inside the `Suggest changes..` field, and TestGPT will modify the code based on your request:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/SuggestChanges.png)

Want to modify the objective of a single test? Edit the name or the objective of a single test, and click regenerate:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/ModifyObjective.png)

You can also just click the `Regenerate` button, without changing the test description, and get an alternative code for this test:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/RegenerteSingleTest.png)

Want more tests? Click on `Give me more tests` at the bottom of the test suite:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/RequestMoreTests.png)

Want to remove a test from your test suite? Click on the `delete` button on each test:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/media/docs/DeleteSingleTest.png)

#### Change test suite configurations
Improve and personalize your test suite by giving general instructions, examples of input and tests and select your preferred testing framework in the `Configuration` section:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/media/docs/AddTEstExample.png)
![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/media/docs/AddInputData.png)
![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/media/docs/ChangeGeneralConfiguration.png)
![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/media/docs/ModifyFramework.png)

#### Add your own test
Want to add a custom test that was not automatically generated? Click on `New custom test` button and write the test name and objective, and TestGPT model will generate the test code for you, based on your preferences:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/media/docs/AddCustomTest.png)

#### Code analysis
Read your code analysis written by our TestGPT model, you can use it for documentation and to make sure your code is doing what it should. Click on the `Code Analysis` tab and find out:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/media/docs/CodeAnalysis.png)

#### Code suggestions
Our TestGPT model can find some insights about your code and suggests some modifications that you can apply to your code (to improve performance, correctness, and more). Click on the `Code Suggestions` tab and find out:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/media/docs/CodeSuggestions.png)

#### Save your test suite
When you're happy with your generated test suite, you can click on `Copy tests` and copy the test suite code, or simply click on `Open as a file` and we will create a test file for you:

![](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/media/docs/OpenCopy.png)


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
- Support: support@codium.ai

## Terms of use

- Terms of use: https://www.codium.ai/terms
- Privacy policy: https://www.codium.ai/privacy-policy
- Please notice - similar to other popular generative-AI tools (such as copilot), we also transmit code snippets to our servers.
