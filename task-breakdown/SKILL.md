---
name: task-breakdown
description: Help a beginner turn a coding idea or task into a manageable breakdown, adjust its detail, and prepare a prompt for one selected task. Use when the user asks how to break down, scope, or organize coding work; ordinary implementation requests do not need a separate planning exercise.
---

# Task Breakdown

Help the learner choose useful units of work. Match their goal, current progress, and requested level of detail. Explain unfamiliar terms briefly in plain language.

## Choose an appropriate breakdown

- Use the conversation and supplied project context before asking questions. If a missing decision would materially change the tasks, ask a small number of focused questions. Otherwise state the assumption briefly and offer a provisional breakdown. Do not turn a rough idea into an extended interview.
- For an oversized idea, identify the smallest useful version with the user. Keep optional future features separate. Do not silently replace their idea or select a complex technology stack.
- Choose feature-based tasks, project stages, or a combination according to what makes the work understandable. Briefly explain the choice when it helps; do not force multiple alternatives.
- For a small new prototype, roughly three to five main tasks is a useful starting point, not a quota. Add one level of sub-tasks only where it clarifies the work. A small change can remain a single task. Do not invent setup, deployment, or other stages for work that does not need them.

## Stop at useful tasks

A leaf task is small enough when it has a coherent outcome, enough context for one focused agent request, and an observable success check. Note dependencies in ordinary language when they affect the order.

Split further only when a task hides distinct outcomes, unresolved decisions, or work too large to review meaningfully. Keep tightly related behavior together when splitting it would produce artificial handoffs. A task may change several files. Avoid individual variables, functions, clicks, or terminal commands unless the learner requests that level of explanation.

Include a short check with each leaf task. Checks belong with the behavior being built; a separate final integration check is useful only when it adds coverage. Do not manufacture a testing phase for every tiny edit or promise that a proposed check has been run.

## Present and adapt

- Assume the learner has little technical background. Keep the first response short and easy to scan: at most one brief goal sentence, the task breakdown, and one short adjustment line. Prefer short bullets or a shallow tree over explanatory paragraphs. Add a question or assumption only when it affects the breakdown; omit generic introductions and repeated requirements.
- Use a compact list, or a shallow text tree when hierarchy is helpful or requested. For a tree, use the project as the root. Use short task labels and one brief “Done when” check per leaf. Keep essential constraints and checks even when shortening the answer; do not split tasks merely to make each line shorter.
- Use familiar words. Explain a necessary technical term in a short phrase where it appears, rather than adding a glossary. Offer further explanation when asked instead of teaching every related concept upfront.
- Explain the grouping in one short line only when it helps the learner make a decision. Offer one relevant adjustment, such as “Ask me to simplify this or expand one task.” Keep longer explanations for follow-up questions.
- Follow explicit choices about grouping, depth, count, and completed work. Expand only the requested branch and retain earlier choices within the current project unless the learner changes them. If a requested structure creates an important omission, flag it briefly while preserving their structure.
- Do not generate a prompt for every task automatically. If asked for the next prompt, use the selected task, or the first unfinished prerequisite when none is selected. Provide one copyable prompt with **Context**, **Task**, **Constraints**, and **Check**. Preserve the agreed scope and exclude adjacent features when necessary to prevent scope creep. Include only context the next agent actually needs.

## Relationship to execution and /plan

This skill guides task breakdown; it does not enable Plan mode. When useful, explain that `/plan` lets Codex investigate and propose an approach before editing. Do not claim that mentioning this skill toggles the app's mode or that plain chat is Plan mode.

Respond in chat. Do not create plan files, change code, run tests, install tools, or deploy as part of a breakdown request. Once the user asks to implement, hand off the selected task to the normal coding workflow without adding a new planning or approval ritual. If Plan mode is active, respect its actual restrictions and explain the transition needed for implementation.
