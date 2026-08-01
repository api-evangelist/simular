---
generated: '2026-07-21'
method: searched
source: https://docs.simular.ai/simulang/simulang-claude-code
name: Simulang for Claude Code
description: >-
  Provider-published Claude Code skill for natural-language desktop automation
  on macOS. Invoked with /simulang; Claude looks up the installed simulang-js
  API, writes a TypeScript script, and runs it with the Simulang CLI.
api: cli/simular-cli.yml
operations:
  - simulang run
  - simulang init-claude
tools:
  - "@simular-ai/simulang"
  - "@simular-ai/simulang-js"
---

# Simulang for Claude Code

> This is a verbatim capture of Simular's published Claude Code skill setup
> (https://docs.simular.ai/simulang/simulang-claude-code). Simular ships the
> skill itself via `simulang init-claude`; this file is the API Evangelist
> catalog record of that provider-published agent skill.

Simulang is a **Claude Code skill** for **desktop automation** on macOS. You
describe the task in natural language (open apps, click controls, type text,
scroll, capture screenshots, inspect the accessibility tree); Claude looks up
the installed `simulang-js` API, writes a TypeScript script, and runs it with
the Simulang CLI.

## Setup

1. Install the Simulang CLI globally:
   ```bash
   npm install -g @simular-ai/simulang
   ```
2. Install the Claude Code skill:
   ```bash
   simulang init-claude
   ```
3. (Optional) Enable the log viewer for visual debugging:
   ```bash
   npm install @simular-ai/simulang-log-viewer
   ```

## Usage

Invoke the skill with `/simulang` followed by what you want to do. Claude then:

1. Looks up the `simulang-js` API docs for the installed version.
2. Writes a TypeScript script.
3. Runs it with `simulang run`.
4. Shows you screenshots or results.

Example prompts:

- `/simulang open safari and go to github.com`
- `/simulang take a screenshot of the current screen`
- `/simulang find all buttons on the screen using accessibility tree`
- `/simulang click on the submit button`
- `/simulang type "hello world" and press enter`

## Requirements

- Node.js >= 22.18
- macOS: grant Accessibility and Screen Recording permissions when prompted
- Optional grounding-model element finding via `OPENROUTER_API_KEY`
