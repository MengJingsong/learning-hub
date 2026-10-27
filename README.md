# Learning Hub

Personal learning repository: `MengJingsong/learning-hub`.

This repository brings together English study, computer-science knowledge, and interview preparation. Each category has its own instructions and learning state.

## Start here

Read [router.md](router.md) to choose a category, then load only its relevant instructions. Copy [project-instructions.md](project-instructions.md) into ChatGPT Project Instructions to use the shared entry point.

| Category | Scope | Instructions |
|---|---|---|
| [english](english/README.md) | English vocabulary, expression, listening, speaking, reading, and writing | [English router](english/instructions/router.md) |
| [CS](CS/README.md) | Computer-science foundations, research, and engineering concepts | [CS router](CS/instructions/router.md) |
| [interview](interview/README.md) | Coding, system design, technical questions, and behavioral interview practice | [Interview router](interview/instructions/router.md) |

## Structure

```text
README.md
router.md
project-instructions.md
english/
  README.md
  study-materials/
  instructions/
  english-study/
    README.md
    project-instructions.md
    inbox.md
    mastery.md
    session-log.md
CS/
  README.md
  instructions/
    router.md
    learning.md
  study-materials/README.md
  mastery.md
  session-log.md
interview/
  README.md
  instructions/
    router.md
    preparation.md
  study-materials/README.md
  mastery.md
  session-log.md
```

## Routing examples

- `英语模式` or `english` selects English; existing commands such as `查词模式` and `听力模式` remain available.
- `CS模式` or `计算机模式` selects computer-science learning.
- `面试模式` or `interview` selects interview preparation.
- `默认模式` clears the active category and mode and resumes intent routing.
- Explicit task requests take precedence for that request. Categories and modes persist only within the current conversation.

Technical English belongs in English when the learning objective is language. Concepts and principles belong in CS. Timed answers, mock interviews, and job-oriented practice belong in interview. Link shared knowledge instead of duplicating it.

## Learning records

The existing English corpus, inbox, mastery scores, and session history are preserved under `english/`. CS and interview begin with empty learning records; no knowledge or mastery is assumed.

## Repository migration

The repository is `MengJingsong/learning-hub` (formerly `MengJingsong/English`). Existing repository content was moved beneath `english/`; internal paths now include that prefix. The repository URL is https://github.com/MengJingsong/learning-hub.

For a local clone, update its remote:

```sh
git remote set-url origin https://github.com/MengJingsong/learning-hub.git
```

Saved ChatGPT Project settings are external to this repository. Replace their previous English-only instructions with the root `project-instructions.md`.
