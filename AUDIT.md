# Audit Guide for AI Coding Agents

English | [简体中文](zh-CN/AUDIT.md)

This guide is for an AI coding agent asked to audit a desktop application against [checklist.md](checklist.md). The goal is a report that lets the user decide what to improve. Read checklist.md before starting. The user's instructions take precedence over this guide.

## Done

The audit is done when every applicable checklist item within the scope agreed at checkpoint 1 (quick or full) has one of the statuses below with evidence, and the user has the report in the structure given under "Report" below.

| Status | Meaning |
| --- | --- |
| Implemented | The code or a run shows the expected behavior |
| Partial | Part of the expected behavior is present; the report says what is missing |
| Missing | Searched for and not present |
| Not verified | The code cannot settle it, for example runtime or platform behavior; the report gives a way to verify it: a [scenarios.md](scenarios.md) scenario, or, where none fits, minimal verification steps written by the agent |
| Not applicable | Does not apply to this product; the report gives the reason |

## Constraints

- **No changes to the project until the user chooses what to address.** The user needs the full picture before deciding, and edits made during the audit mix findings with fixes.
- **Every status cites evidence**: a file and line, a configuration value, a build or packaging setting, or a test result. Readers can then check any finding themselves. When no evidence can be found either way, the status is Not verified, not Missing. Each piece of evidence states its type: static inspection (code and configuration) or runtime verification (behavior observed in a run). Under the checklist's rules for checking items off, only runtime-verified items can be marked `[x]`.
- **Use the user's language** for questions and the report.
- **Name items by ID and title together**, for example "INSTALL-07 Update authenticity", never by the bare ID. The user does not have the checklist open; the ID is a key for the agent, and the title is the name the user understands. In conversation, add one clause saying what the item is about.

## Two checkpoints with the user

These are the only points where the work waits for the user.

**1. Before auditing, confirm the scope.** Determine from the codebase the stack, target platforms, distribution methods, product type, feature tags, and which conditional domains apply (see [README.md](README.md#product-types) and the domain headings in checklist.md). Present this briefly and ask only what the code cannot answer. Usually that is which platforms the product commits to rather than merely builds for, whether CJK input or right-to-left scripts matter, which similar products users mainly migrate from or use alongside, and whether the user wants a quick audit (all Baseline items, plus the QoL items the agent judges most valuable for this product type) or a full one. Scope decides which items apply, so wait for the answers. Parenthetical notes in an item for platforms the product does not commit to do not count toward that item's status.

**2. Before changing anything, let the user choose.** After the report, ask which items to address. Unless the user prefers otherwise, suggest this order: Baseline items that can lose data (for example, the DATA domain; SETTINGS-04 Reliable persistence, tolerant of manual edits; FILE-05 Network drives, removable media, and cloud placeholders), then Baseline items that make the application unusable in a committed environment, then the remaining Baseline items, then QoL items by value relative to effort. Lost user data cannot be restored by a later fix, which is why it comes first. Address one item or a small related group at a time, say how each change can be verified, and update its status in the report.

## Questions by user moment

After the domain-by-domain review, the agent asks itself one question for each of the ten moments below: what happens in the product when the user is at this moment, and which checklist item covers it. The agent answers these from the code and from runs; they are not questions for the user, who is asked only the scope questions at checkpoint 1. Record anything without an answer under "Possible unknown needs" in the report. Read domain by domain, one need can be split across several items that each look covered; asking by moment finds the gaps between items.

| Moment | Question |
| --- | --- |
| First use | On first launch, with no data yet, can the user understand the application and finish a first task? |
| Interruption | When an operation is interrupted halfway, what happens to the work in progress? |
| Leaving | After the user switches to another task, closes the window, or leaves the computer, how do they learn where unfinished work remains? What information does content handed to other programs or people carry? |
| Returning | On coming back, can the user continue from the previous state? |
| Mistake | After a wrong deletion, overwrite, or click, can the user recover? |
| Environment change | After a change of display, scaling, device, network, or storage location, does everything still work? |
| System failure | What state remains after a crash, a lost connection, a full disk, or a shutdown? |
| Repetitive work | Does the user repeat the same operation many times? |
| After an update | After an upgrade, are settings, data, and familiar actions still there? |
| Migrating in / running alongside | When the user comes from a similar product or uses both, is each setting, data type, and behavior they rely on there matched here, substituted, or deliberately left out? Answer against the settings pages of the products identified at checkpoint 1; when none was identified, record this under possible unknown needs. |

The top of [scenarios.md](scenarios.md) groups scenarios by the same moments, which helps in choosing scenarios for verification.

## Report

Lead with the summary. Use this structure so reports are comparable across projects and re-audits:

```markdown
# Checklist audit: <project name>

## Scope
- Stack, platforms, type and tags, skipped domains (with reason), depth
- Items left out of the audit and how many (in a quick audit, the QoL items not selected)
- Checklist version used (release tag or commit hash), so a re-audit knows what changed

## Summary
- Baseline: N implemented, N partial, N missing, N not verified, N not applicable
- QoL: N implemented, N partial, N missing, N not verified, N not applicable

## Baseline items missing or partial
| Item (ID and title) | Finding | Evidence | Suggested change | Effort |
| --- | --- | --- | --- | --- |

## Top five QoL improvements
| Item (ID and title) | Finding | Evidence | Suggested change | Effort |
| --- | --- | --- | --- | --- |

## Possible unknown needs
| Moment | Finding | Evidence | Suggestion |
| --- | --- | --- | --- |

## Not verified
| Item (ID and title) | Reason | Scenario (number and title) or verification steps |
| --- | --- | --- |

## Not applicable
| Item or domain (ID and title) | Reason |
| --- | --- |

## Appendix: results by item
| Item (ID and title) | Status | Evidence | Evidence type |
| --- | --- | --- | --- |
```

Effort is small (under an hour), medium (within a day), or large (more than a day). The appendix lists every item in scope, and the sections above draw from it; "Top five QoL improvements" only suggests an order of work, and the status of the remaining QoL items is in the appendix. Present the report in the conversation and offer to save it in the project.

## Notes

- Appendix A of checklist.md lists implementation pitfalls by stack. Check the ones for the detected stack.
- The user usually cannot see tool output. In a long audit, give a one-line progress note every few domains.
- For a re-audit, start from the previous report: re-check its partial, missing, and not verified items; items affected by code changes since then; items added or changed in the checklist since the version used last time; and items brought in by scope changes (new platforms, distribution methods, or applicable domains).
