# Modern Desktop App Capability & QoL Checklist

English | [简体中文](zh-CN/README.md)

This checklist describes capabilities and quality-of-life behaviors that desktop GUI applications typically need beyond their core features. It is intended for review during design, implementation, and release.

It applies to desktop GUI applications on Windows, macOS, and Linux and is independent of any technology stack. It is not a compliance standard and does not provide scoring or certification.

## Why this checklist

A growing share of desktop software is now built largely through AI coding agents, a practice often called vibe coding. With an agent, many quality-of-life behaviors that once took significant effort, such as restoring scroll position, handling IME composition, saving atomically, or returning focus after a dialog closes, cost little to implement once someone asks for them. The hard part is no longer writing the code but knowing that the behavior should exist.

Agents do not reliably fill that gap on their own. Many of these behaviors are rarely described explicitly; they appear in bug reports, in footnotes of platform documentation, or in the habits of experienced developers. Nothing guarantees that the training data of future models will cover them.

This checklist collects these behaviors in one place, as a reference that can be handed to an agent or used by a reviewer.

Platform guidelines and design systems answer how to implement a known requirement correctly. This checklist answers which requirements are easy to miss. The two complement each other.

## Files

| File | Contents |
| --- | --- |
| [checklist.md](checklist.md) | The main checklist: 26 domains, 220 items. Each item describes expected behavior; some include a typical defect |
| [AUDIT.md](AUDIT.md) | Guided audit procedure for AI coding agents |
| [scenarios.md](scenarios.md) | 42 combined scenarios for verification in a real environment |
| [references.md](references.md) | Sources behind the items, organized by domain |
| [side-notes.md](side-notes.md) | Related topics outside the checklist's scope, product examples, and similar checklists |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Inclusion criteria and writing guidelines |

## Overview: 12 checks

The following 12 checks summarize the main checklist; each corresponds to one or two domains. Check only the scenarios the product commits to supporting.

- [ ] **Display and layout**: Primary content and actions remain usable after changes to system scale, text size, theme, half-screen snapping, or multiple displays.
- [ ] **Input and interaction**: Keyboard, focus, IME, mouse, touchpad, and common editing behaviors follow platform conventions.
- [ ] **Assistive technology**: Control semantics, key states, and complex content are exposed to assistive technologies, and core tasks can be completed.
- [ ] **Context restoration**: After going back, switching tabs, restarting, or summoning, the user returns to a reasonable place in their work.
- [ ] **Visible state**: Save, connection, task, permission, and error states match reality; items needing attention can be found.
- [ ] **Recovery from mistakes**: Reversible actions can be undone, destructive actions are protected, and the scope of each action is clear.
- [ ] **Data protection under failure**: Save failures, crashes, external changes, and sync conflicts never silently destroy the user's valid content.
- [ ] **Data portability**: Users can find, export, or migrate their data and know which parts are omitted or lossy.
- [ ] **Working with other software**: Copy and paste, drag in and out, external open, reveal in system, sharing, and printing are supported as needed.
- [ ] **Settings and permissions**: Settings and permissions can be discovered, adjusted, reset, and re-granted; failures and degraded states produce feedback.
- [ ] **Long-running use**: The application does not steal focus, interrupt repeatedly, or waste energy; long tasks and offline states behave completely.
- [ ] **Install, update, troubleshoot, and uninstall**: Distribution channels, data compatibility, self-recovery, and exiting background activity are all addressed.

## Product types

A product can belong to more than one type. The table indicates which tags and scenarios to review first.

| Type | Examples | Tags to review first | Scenarios to review first |
| --- | --- | --- | --- |
| **Workbench** | Editors, IDEs, note-taking apps, design tools | `data` `text` `multi-window` | S01, S04, S06, S07, S13, S21, S24, S26, S37, S39, S41, S42 |
| **On-demand utility** | Launchers, screenshot tools, dictionaries, clipboard managers | `on-demand` `background` | S09, S11, S19, S20, S25, S31, S33 |
| **Viewer and batch tool** | Image viewers, media players, converters, download managers | Mostly untagged items; `network` as needed, plus the COMPONENT, MEDIA, and TRANSFER domains | S02, S10, S12, S21, S22, S30, S32, S34 |

Tags:

| Tag | Does the product… |
| --- | --- |
| `data` | hold data that users create or organize |
| `text` | let users read or edit text, code, or logs for long periods |
| `background` | keep running after its windows are closed |
| `on-demand` | stay hidden until summoned by a hotkey and dismissed after use |
| `network` | depend on network services or accounts |
| `multi-window` | support multiple windows, tabs, or documents |
| `distribution` | behave differently depending on how it is distributed |

Untagged items apply to nearly all desktop applications.

## How to use

### With an AI coding agent (recommended)

The checklist is designed primarily for projects developed with AI coding agents. In the project to be audited, give the agent this instruction:

> Clone tag v1.0 of https://github.com/shiratakebai/modern-app-capability-checklist into a temporary directory outside this project, then follow its AUDIT.md to audit this project.

<!-- When releasing a new version, update the tag here. -->

[AUDIT.md](AUDIT.md) defines the outcome and leaves the method to the agent. The agent pauses at two points: before auditing, to confirm the scope it inferred from the codebase; and after the report, so the user can choose which items to address. The report has a fixed structure, and every finding cites evidence. The agent does not modify the project before the user has chosen. The instruction pins a release tag so that the audit guide stays at a reviewed version; newer releases are listed on the repository's Releases page. If the agent cannot access the network, download this repository manually and give the agent the local path to AUDIT.md.

### In manual review

1. **Architecture**: Review the Baseline items in WINDOW, DATA, SETTINGS, NETWORK, and INSTALL. The window model, atomic writes, configuration directories, and offline boundaries are the most expensive to change later.
2. **Refinement**: Based on the product type, select the items that shape everyday use, Baseline or QoL, and review them together, for example IME, clipboard, startup flashing, scroll position restoration, and focus behavior.
3. **Before release**: Run three to five scenarios on real devices and record which were tested and which were not.
4. **In the project**: Copy the checklist into the project repository, delete items that do not apply with a reason, and work through the rest.

## Out of scope

- Web and mobile applications.
- Schemas, state models, scoring, and formats for acceptance evidence.
- Complete compatibility tables for each framework.
- Conformance mappings to WCAG or platform HIGs.
- Global priorities. Each product sets its own.

## Translations

The English version in the repository root is the primary version. A Simplified Chinese translation is in [zh-CN/](zh-CN/README.md).

## License

Copyright © 2026 shiratakebai. Licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE).
