---
name: codex-setup
description: Guide beginners through ChatGPT desktop, Codex, GitHub, MCP connections, and workshop skills for local development. Use for first-time setup and for checking or resuming a setup step.
---

# Codex Setup

Guide the learner one step at a time in short bullets. Give the next action, its link if needed, and one thing to check. Use evidence from the chat to skip completed steps. If the check fails, troubleshoot that step before moving on. Carry a short status summary into a new chat if the setup requires one.

Setup works in a chat without a project, including a temporary workspace. Never create a project or project folder during setup, and never ask the learner to create, select, or open one as a prerequisite. The learner chooses their project separately when they are ready to build.

## 1. Identify web or desktop

If the surface is unclear, ask whether the learner is using ChatGPT in a browser or the installed ChatGPT desktop app. An in-app browser tab is not evidence that the conversation is a web chat.

- **Web:** If the learner's OS is known from their message or trusted information about their own device, give the matching installer. For Mac, use [ChatGPT for Mac](https://chatgpt.com/download/). For Windows, use [Download the ChatGPT Windows installer](https://get.microsoft.com/installer/download/9PLM9XGG6VKS?cid=website_cta_psi). If the OS is unknown, offer both links and let the learner choose. The OS reported by a cloud or remote workspace identifies that workspace, so use the student's own device information to select an installer. After installation, have them sign in with the same account and switch to Codex. Give them a short resume message with their completed steps. [Desktop setup guide](https://learn.chatgpt.com/docs/app#get-started-with-the-desktop-app)
- **Desktop:** Confirm they have signed in and selected Codex. If both are already confirmed, continue directly to the first unfinished account or plugin step in the current chat.

## 2. Set up GitHub

Guide GitHub account creation and email verification using [GitHub account setup](https://docs.github.com/en/get-started/onboarding/getting-started-with-your-github-account). For student account questions, use the [ChatGPT terms](https://openai.com/policies/row-terms-of-use/#registration-and-access) and [GitHub account terms](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service#b-account-terms). Students handle sign-in and service permissions in the app or browser.

Open the [GitHub plugin page](https://chatgpt.com/plugins/github) and select **Install plugin**. Connect the standard GitHub app for a github.com account when prompted. Enable access to the student's repository when there is one. [Plugin installation](https://learn.chatgpt.com/docs/plugins#install-and-use-a-plugin)

- **GitHub check:** Select `@GitHub` and ask it to read the README from a repository the student names. Report whether an actual tool call succeeded. If they have no repository yet, mark the account connection as reported and leave repository access pending.

## 3. Check the current chat and any separately added MCP

- **Install or connect prompt inside a chat:** If Codex shows **Continue** after setup, resume there and retry the read-only check. [Same-chat connection flow](https://learn.chatgpt.com/docs/app/commands#start-a-chat-with-a-plugin)
- **Installed through the plugin directory:** Start a new Codex chat as documented. Carry forward completed checks and retry the first pending one. Plugin selection with `@` confirms availability in the composer. A successful read confirms access. [Plugin installation](https://learn.chatgpt.com/docs/plugins#install-and-use-a-plugin)
- **Separate MCP server provided for the workshop:** In desktop Codex, open **Settings → MCP servers → Add server**, enter the instructor's server details, save, and choose **Restart**. Authenticate when prompted. Use `/mcp` to see the server, then try a read-only tool in the current chat. If the tool is still missing after restart, try a new Codex chat. For OpenAI Docs MCP, use **Streamable HTTP**, name `openaiDeveloperDocs`, and URL `https://developers.openai.com/mcp`. Verify it by fetching an official page about Plan mode through the server. [Desktop MCP setup](https://learn.chatgpt.com/docs/extend/mcp#configure-in-the-chatgpt-desktop-app) · [OpenAI Docs MCP](https://learn.chatgpt.com/learn/docs-mcp)

When the learner cannot run a check here, give them the exact prompt to run and ask for the result or error. Distinguish a reported install, a visible tool, and a verified tool call. For a failed check, confirm the account, project or team access, and plugin availability in that chat. Use only read-only checks during onboarding.

## 4. Add and check the workshop skills

- **OpenAI Docs:** Check the Skills list for `openai-docs`. If missing, use `$skill-installer openai-docs`. Check that Codex can select it and cite an official answer about `/plan`.
- **Task Breakdown ZIP:** If the instructor has not shared the ZIP yet, mark it pending and continue any other checks. When the student has it, guide them to extract the whole `task-breakdown` folder into `.agents/skills` under their home folder, which is the personal skills location. Explain that a leading dot may hide `.agents` in their file browser. Check for `~/.agents/skills/task-breakdown/SKILL.md` and confirm that Codex can select `$task-breakdown`. If the skill is missing, verify the path and restart Codex if needed. [Personal skill location](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)

## 5. Verify the planning skill

In the current Codex chat, have the student enter `/plan`, select `task-breakdown`, and ask it to divide their own idea into a few tasks with one check each. If they have not chosen an idea, they can try a one-page website for a school club as a practice example. Confirm that the skill was selected and the result is a short breakdown with checks. The student can review the breakdown and ask for a first-task prompt in chat. Actual implementation happens later when they choose to start their project. [Codex prompting guide](https://learn.chatgpt.com/docs/prompting#prompting-codex)

Finish with a short list of verified steps and any pending checks, such as a missing workshop ZIP. Use the same list as a resume message when switching chats.
