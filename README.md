# qodo Gen

### Code, test and review with confidence

[qodo Gen](https://www.qodo.ai/products/ide-plugin/) is your AI-powered coding assistant and mentor. qodo Gen helps you understand your code, test it and review it with your team.

**[Sign in to start using qodo Gen.](https://app.qodo.ai/signin)**

**Supports all programming languages!**

## [![GitHub](https://img.shields.io/badge/github-000000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Codium-ai) [![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/kG35uSHDBc) [![X URL](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://twitter.com/QodoAI)

---

## Table of Contents

1. [What can qodo Gen do?](#What-can-qodo-Gen-do?)
2. [Using qodo Gen Shortcuts](#Using-qodo-Gen-Shortcuts)
3. [qodo Gen Chat](#qodo-Gen-Chat)
4. [Code Completion](#Code-Completion)
5. [Tests Generation](#Tests-Generation)
6. [Learn More](#Learn-More)
7. [Support and Community](#Support-and-Community)
8. [Data Sharing](#Data-Sharing)

---

## What can qodo Gen do?

qodo Gen uses advanced AI models to deeply understand your code structure, logic, and context to help you write better code.

With qodo Gen, you can:

- Understand your code better.
- Improve code quality.
- Uncover potential bugs.
- Ease your PR process.
- Generate tests and Docstrings.

And much more.

Start using qodo Gen by clicking the qodo Gen logo in your Extensions bar.

![qodo Gen Demo](https://www.qodo.ai/images/qodo-gen-gifs/Demo.gif)

---

### Using qodo Gen Shortcuts

Use qodo Gen's keybinding shortcuts:

- Linux: `alt+shift+c`
- Mac: `cmd+ctrl+c`
- Windows: `ctrl+win+z`

---

---

## qodo Gen Chat

qodo Gen Chat offers real-time coding assistance within your development environment. Use qodo Gen Chat for:

- **Improving your code:**  
   From making it more secure to beautifying and cleaning it.

- **Understanding your code better:**  
  Simplify onboarding for new or junior developers by providing in-depth insights into your codebase.

- **Asking free-style questions about your code:**  
  Get instant answers to any code-related question using AI-powered free-form queries.

- **Generating docstrings:**  
  Improve code maintainability by generating docstrings.

- **Generating unit tests and test suits:**  
  Secure and eliminate bugs in your code by adding extensive testing.

---

### Focus

**Focus** is the part of your code that your conversation in qodo Gen Chat centers around.  
It could be an entire file or just a few lines of code.

![Choosing Focus](https://www.qodo.ai/images/qodo-gen-gifs/ChoosingFocus.gif)

#### Guidelines on choosing Focus

Select the focus that best fits your current coding task or question. Consider the scope of your query and what it relates to.

#### Choose the best Context

To get the best, most relevant results to your Chat query, make sure to choose the most relevant Context. **This will help qodo Gen Chat's AI models tailor the best response for you.**  
Learn more about Context in this document and in our [documentation portal](https://qodo-gen-docs.qodo.ai/chat/add-context/).

#### Switch Focus as needed

You can switch the focus at any time based on the evolving needs of your development work. qodo Gen seamlessly adapts to the selected focus and updates the context it's using.

#### Focus types

To choose Focus, click `Add focus` on the bottom left, or type `@` in the chatbox.  
You can then select one of two Focus types:

1. [**Current File**](https://qodo-gen-docs.qodo.ai/chat/focus/#selecting-a-focus:~:text=%C2%B6-,Current%20File,-:%20Focuses%20on%20the): Focuses on the current file you're working on.

   When choosing Current File Focus, you have to choose a **Secondary Focus** option. The Secondary Focus refines the context for qodo Gen Chat's responses.

   There are two options for Secondary Focus:

   - **Selected Lines:** Manually select lines in your code to set as the focus for your request.

     ![Selected Lines Focus](https://www.qodo.ai/images/qodo-gen-gifs/SelectedLinesFocus.gif)

   - **Component:** Select specific code components from the bottom right part of the chatbox. The components consist of functions, methods and classes automatically detected from the current file.

2. [**Git Diff**](https://qodo-gen-docs.qodo.ai/chat/focus/git-diff/): Include Git changes across your entire project, enabling you to manage and review code changes effectively.

   To choose Git Diff click on `@` and select `Git Diff`.  
   You can then choose to focus on either `Local Changes`, `Staged Changes` or `Committed Changes`.

   Git-Diff supports commands for managing commits, documentation, code quality, and more.

---

### Context

Think of Context like the brain of qodo Gen Chat. The Context is what qodo Gen's AI models know about your code and what they use to give the best, most accurate response.

**Adding more context will give more accurate and relevant responses**, so choosing context is an important part of using qodo Gen Chat to your advantage.

#### Adding Context

There are multiple ways to add Context to qodo Gen Chat:

1. **Code Snippet:** Select a few lines of code from your project to add as context.

   **Usage:** Select a code snippet, right-click and choose `Add to qodo Gen as context`.

   ![Snippet As Context](https://www.qodo.ai/images/qodo-gen-gifs/SnippetAsContext.gif)

   **Shortcuts:**

   - **VSCode:**

     - Mac: `Cmd+Shift+E`
     - Windows: `Ctrl+Shift+E`

   - **JetBrains:**
     - Mac: `Cmd+Option+Comma`
     - Windows: `Ctrl+Alt+Comma`

2. **Files:** Select any file from your project to add as context.

   **Usage:** Click on `@` or type `@` in the chatbox, and select `Add a file or a folder`.  
   Alternatively, right-click any file from your project and choose `Add to qodo Gen as context`.

3. **Folder:** Select any folder from your project to add as context.

   **Usage:** Click on `@` or type `@` in the chatbox, and select `Add a file or a folder`.  
   Alternatively, right-click any folder from your project and choose `Add to qodo Gen as context`.

4. **Entire Project:** Select your entire project to add as context.

   **Usage:** Click on `@` or type `@` in the chatbox, and select `Add a file or a folder`. Under the searchbar, choose `Full project`.

5. **Image:** Select any image to add as context.  
   For example, add an image of a required design and qodo Gen Chat will help you create it.

   **Usage:** Click on `@` or type `@` in the chatbox, and select `Upload an image`.

   [Learn more about adding images to the chat.](https://qodo-gen-docs.qodo.ai/chat/images)

---

### Commands

Commands are what qodo Gen Chat is all about. Call a command to unlock all of qodo Gen Chat's capabilities.

**To call commands either:**

- **Type them directly** in the chatbox with a leading slash `/`.
- **Manually select lines from your code**, right-click and choose `qodo Gen`, then pick a command from the list.

###

![Calling Commands](https://www.qodo.ai/images/qodo-gen-gifs/Commands.gif)

#### Commands List

- **`/ask`**: Ask any free-text question about your code.

- **`/explain`**: Understand how the selected code works.

- **`/improve`**: Get suggestions to improve your code.

- **`/enhance`**: Beautify and clean your code.

- **`/docstring`**: Automatically generate docstrings.

- **`/find-on-github`**: Find relevant open-source code on GitHub.

- **`/quick-test`**: Automatically generate unit tests.

- **`/test-suite`**: Get step-by-step examples to create a test suite.

[Find out more about qodo Gen Chat Commands on our documentation portal.](https://qodo-gen-docs.qodo.ai/chat/commands/)

---

### Continue Chat

After receiving your response, click `Continue this chat` to keep the conversation going. Your current chat will be used as context for the rest of the conversation.

---

### Learn More

You can find out more about qodo Gen Chat in our [documentation portal](https://qodo-gen-docs.qodo.ai/chat).

---

---

## Code Completion

qodo Gen Code Completion is a powerful tool designed to accelerate your coding process, reducing the need for repetitive tasks such as copying and pasting code snippets from the internet.  
By enabling Code Completion, qodo Gen learns from your codebase and provides real-time suggestions that seamlessly integrate with your writing flow.

![Code Completion](https://www.qodo.ai/images/qodo-gen-gifs/CodeCompletion.gif)

---

### Use Code Completion

Code Completion is a Pro feature, exclusively available for Teams and Enterprise users. [Visit Qodo's website to learn more.](https://www.qodo.ai/glossary/ai-code-completion/)

As you type, qodo Gen analyzes your code in real-time to grasp your intention. It then presents code completions in a grayed-out format directly in your editor. These suggestions aim to complete your current line of code or offer snippets that fit the context of your work. To accept a suggestion, simply press the Tab key, and the completion will be inserted into your code.

---

### Customization

Configure qodo Gen Extension settings to customize Code Completion to suit your specific coding style and needs.

Provide general instructions to guide qodo Gen in generating code completions. This customization ensures that the suggestions are not only accurate but also align with your preferences and project requirements.

[Learn how to configure your Code Completion settings.](https://qodo-gen-docs.qodo.ai/installation/extension-settings/)

---

### Learn More

You can find out more about Code Completion in our [documentation portal](https://qodo-gen-docs.qodo.ai/code-completion).

---

---

## Tests Generation

qodo Gen leverages advanced AI technology to generate comprehensive tests for **any programming language**.

Test generation boosts productivity, enhances code quality and simplifies the development process, helping you deliver reliable, high-performance software with ease.

![TestGeneration](https://www.qodo.ai/images/qodo-gen-gifs/TestGeneration.gif)

---

### Using Test Generation

- **For a function, class or method:** Click the `Test this function` button above the function declaration.
- **For code snippets:** Select the code you want to test. Right-click on your selection and choose `qodo Gen`. From the dropdown menu choose `Generate Tests`.

The qodo Gen Testing tab will open.

---

### Test Suite

#### Improve Tests

The more context, the better the tests generated by qodo Gen.
<br>Provide test examples to qodo Gen in the test box and improve your generated tests.

#### Explore Behavior Coverage

The Behaviors Coverage section categorizes function behaviors into three main types, each representing a different aspect of how your code operates:

- **Happy Path:** The ideal and expected use cases of your code, where everything operates as intended without any errors or exceptions.
- **Edge Case:** The boundaries of your code's logic, handling unusual or extreme inputs or scenarios that might not be immediately obvious.
- **Other:** Less common use cases not fitting into the first two categories.

Click on `Generate test` next to any behavior to generate a test for a specific behavior type.

#### Tests

In this section you can find tests generated by qodo Gen and run them.  
Alternatively, you can `Run and auto-fix`: if a test fails, qodo Gen will attempt to fix it automatically and re-run it.

---

### Context

qodo Gen uses your codebase as **Context** to generate the most relevant tests. You can manage this Context in the `Context` tab.

---

### Configuration

You can improve and personalize your test suite in the `Configuration` section.

- **Provide test examples and improve your generated tests:** The more context, the better the outcome. qodo Gen uses examples to improve tests generation.
- **General instructions:** Customize your test generation by choosing your preferred testing framework, number of tests required and giving hints.
- **Configuration file management:** Ensure consistency across your project or team and save settings to a TOML file. [Learn more about the configuration file.](https://qodo-gen-docs.qodo.ai/tests/configuration/#saving-configuration-to-a-file)

---

### Learn More

Find out more about test generation in our [documentation portal](https://qodo-gen-docs.qodo.ai/tests).

---

---

## Uninstall qodo Gen

1. Click on the Qodo button in the bottom status bar.
2. Hover over the authentication notification, select the settings icon and choose the `Manage Extension` option.
3. qodo Gen Extension will open in a new tab. Select Uninstall and reload VSCode.

## Learn More

Find out more about qodo Gen and other Qodo products in our [documentation portal](https://qodo-gen-docs.qodo.ai).

## Support and Community

**Need help?** Visit our [FAQ and troubleshooting guide](https://www.qodo.ai/blog/technical-faq-and-troubleshooting/).

**[Join our Discord community!](https://discord.gg/kG35uSHDBc)**

## Data Sharing

Similar to other popular generative-AI tools, we transmit code snippets to our servers. You can learn more in our [terms of use](https://www.qodo.ai/terms) and [privacy policy](https://www.qodo.ai/privacy-policy).

You can opt out of sharing data with Qodo.
<br>Go to the extension's settings and check the box `Opt out of sharing my data with Qodo`.
