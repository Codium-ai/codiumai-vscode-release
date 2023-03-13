# CodiumAI - Meaningful tests for busy devs

---

> CodiumAI analyzes your code and generates meaningful tests to catch bugs before you ship. With CodiumAI, you can easily and quickly create comprehensive test suites that help you ensure the reliability and correctness of your software. Supports Python, Javascript and Typescript.
---

![How it works](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/v042-qa-3Full.gif)

_Alpha Version 0.5.0 - Supported in VSCode version 1.70.0 and above_

## Features

#### 🤖 Generates unit tests automatically

Simply press the "generate tests" button above your class or function, and CodiumAI will generate a set of suggested tests for different use cases.

#### ✨ Works seamlessly with VSCode

The generated test wuite will be displayed in a new panel in your VSCode IDE, along with your code analysis, so you can easily review and edit them as needed.

#### 🚀 Helps you improve code quality

By creating comprehensive test suites, our tool helps you catch and fix bugs early, and ensures that your code is reliable and maintainable.

---

## Installing

![Install](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/Step1.png)
<br>

![Successful installation](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/Step2.png)
<br>

![Github Login page step one](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/Step3.png)
<br>

![Github Login page step two](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/Step4.png)

<br>

## Getting started

![Review the results](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/Step5.png)
<br>

![Modify test style](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/Step6.png)
<br>

![Modify test cases](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/Step7.png)
<br>

![Regenerate tests](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/Step8.png)
<br>

![Accept and enjoy](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/Step9.png)

<br>

1. After installation, you should receive a notification on the bottom of the VSCode editor. Click "Sign in" button in the notification popup to activate CodiumAI with your GitHub or Google account. If you can't see the notification on the bottom right of the editor window, click the button labeled CodiumAI in the bottom status bar.

2. You will be redirected to the GitHub or Google login page.

3. Once you confirm the activation you should be redirected back to the editor. Status notification should show your GitHub or Google username when the activation was successful.

4. Open existing Python, JS or TS file or write a new class/function and press the "Generate Tests" on top of the class/function.

5. Another option, select a Python, JS or TS file, and click on CodiumAI button on the left bar. Select a class or a function that you want to generate tests for.

6. A new panel will open in your VSCode IDE with the generated tests, along with the test suite, a configuration panel, excluded tests and your code analysis.

7. Options for configurations:
   - Add general instructions - choose or add style for your test suite.
   - Add examples of data inputs to enhance and accurate your generated tests.
   - Add example of tests to accurate yout tests suite style to match your style.
   - Add your own test to start the test suite from.
   - Choose auto mock on / off - to automatically generate mocks for your tests.
   - Choose number of tests to generate.

8. On `Settings` button, change the tests framework to match your framework preferences.

9. Click `Re-generate` button to regenerate the test suite based on your configuration and settings.

10. Modify the test cases list to fully control generated tests. Remove the cases you don't need, or add them back from `Excluded Tests` tab.

11. On each test case, you can click `Copy test` to copy the test code, or `Exclude test` to remove the test from the test suite.

12. On the bottom of the test suite you can click `Copy tests` to copy the entire test suite, or `Save to file` to save the entire test suite to your project. 

> Tip 1: If you can't see the `Generate Tests` button you might have to set `"editor.codeLens": true,` in your VSCode configuration file.
> <br>

> Tip 2: You can show and hide CodiumAI panel in the extension settings or from the command palette.
> <br>

<br>
## How to uninstall

1. Select "CodiumAI" button in the bottom status bar.
2. Hover over the authentication notification, select the settings icon and "Manage Extension" option from the dropdown.
3. CodiumAI Extension will open in a new tab. Select Uninstall and Reload VSCode.

## Links

[![Join our Discord community](https://raw.githubusercontent.com/Codium-ai/codiumai-vscode-release/main/media/docs/Joincommunity.png)](https://discord.gg/SgSxuQ65GF)

- Discord community: https://discord.gg/SgSxuQ65GF
- CodiumAI site: https://codium.ai
- Blog: https://www.codium.ai/blog
- Support: support@codium.ai

## Terms of use

- Terms of use: https://www.codium.ai/terms-of-use
- Privacy policy: https://www.codium.ai/platform-privacy-policy
- Please notice - similar to other popular generative-AI tools (such as copilot), we also transmit code snippets to our servers.
