# YHacks 2026 Codex Skills

Two skills for the YHacks workshop. Use Codex Setup to get your tools ready, then use Task Breakdown to turn an idea into a plan you can build and test.

## Install the skills

1. On this repository’s GitHub page, choose **Code → Download ZIP** and extract the ZIP.
2. Open your home folder. On Windows, enter `%USERPROFILE%` in File Explorer’s address bar. On macOS, choose **Go → Home** in Finder. Create an `.agents` folder if needed, then create a `skills` folder inside it. On macOS, press **Command + Shift + .** to show hidden folders.
3. Copy the entire `codex-setup` and `task-breakdown` folders from the extracted ZIP into `.agents/skills`. Keep `agents/openai.yaml` inside the `task-breakdown` folder.
4. Open a Codex chat in the ChatGPT desktop app and check for both skills in **Skills** in the sidebar. If either is missing, check that the files are in the locations shown below and restart the app.

```text
~/.agents/skills/
├── codex-setup/
│   └── SKILL.md
└── task-breakdown/
    ├── SKILL.md
    └── agents/
        └── openai.yaml
```

`~` means your home folder. [Official Codex skill installation guide](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)

## Use [Codex Setup](codex-setup/SKILL.md)

Use this skill for first-time setup or to pick up where you left off. Start a Codex chat and send the prompt below. The skill helps you check your desktop setup, connect GitHub, and verify the workshop tools one step at a time.

```text
$codex-setup Help me get ready for the YHacks workshop. I’m signed in to Codex and haven’t connected GitHub yet.
```

Change the second sentence to describe what you’ve already done or where you got stuck.

## Use [Task Breakdown](task-breakdown/SKILL.md)

Describe who your app helps and what the smallest useful version should do. Use the skill to get a short list of tasks with one way to check each task.

```text
$task-breakdown I want to build a study timer for students. It should let them enter a task, choose a duration, and start or reset the timer.
```

Pick one task from the breakdown and ask Codex to turn it into a copyable prompt. To review an implementation plan before Codex edits files, enter `/plan` and give Codex that prompt.
