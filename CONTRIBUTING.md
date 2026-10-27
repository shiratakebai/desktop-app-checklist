# Contributing

English | [简体中文](zh-CN/CONTRIBUTING.md)

## Inclusion criteria

A new item must meet all four:

1. **Observable by users.** It describes what users get, not framework configuration keys.
2. **Common across products.** Many kinds of products encounter it; needs specific to one product are not included.
3. **Easy to overlook.** The checklist exists to remind.
4. **Backed by a source.** Name at least one existing product that does it, or a real failure, complaint, or incident caused by its absence. The source goes in the pull request description, not in the checklist text; sources published by platform vendors, standards bodies, government agencies, or software companies are also added to [references.md](references.md).

Material that meets the first three criteria but lacks a source, or applies only to a narrow kind of product, can go in [side-notes.md](side-notes.md) instead.

Before proposing a new item, check whether one more sentence in an existing item would cover it. Most "what happens on failure" and "what is preserved after recovery" points belong in an existing item rather than a new one.

## Item format

```
- [ ] **ID Title** `tag` · Baseline or QoL — Expected behavior. Requirements for failure paths or handoffs.\
  Common failure: One typical defect.
```

- **ID**: Numbered sequentially within the domain. Numbers of deleted items are not reused. English and Chinese versions share the same IDs. The ID is a stable key, not a name: inside checklist.md a cross-reference may use the bare ID, because the reader is in the document and can search for it; everywhere else that a reader may see without the checklist open (scenarios, README, AUDIT.md, audit reports) the ID is followed by the item title.
- **Tags**: Only seven: `data` `text` `background` `on-demand` `network` `multi-window` `distribution` (in the Chinese version: `数据` `文本` `后台` `浮窗` `联网` `多窗` `分发`). No tag means the item applies to nearly all desktop applications.
- **Domain applicability**: TRUST, EXTEND, AUTOMATE, LICENSE, MANAGED, FAIR, FIND, COMPONENT, MEDIA, and TRANSFER are relevant only to some products. Their applicability is stated under the domain heading instead of through additional tags.
- **Baseline / QoL**: For scanning only; does not indicate priority. Baseline means its absence breaks features, loses data, or makes the application unusable in some environments. QoL means it improves efficiency and comfort.
- **Common failure**: Optional. Describes one concrete, reproducible defect.
- **Line break**: The trailing `\` on the expected behavior line renders "Common failure" on its own line.

## Writing guidelines

### Register

- Use declarative sentences that describe the expected state, such as "A failed write leaves the original file intact." Checking an item means the statement holds for the product.
- Do not address the reader as "you". Avoid colloquialisms, metaphors, exclamations, and rhetorical questions.
- Do not split content that fits in one paragraph into a series of one-sentence paragraphs, and do not add recaps, definitions, or summaries the content does not need.
- Use standard platform and industry terminology, and use the same term for the same concept throughout.

### No defensive writing

Defensive writing is qualification, clarification, or disclaimer added to fend off objections without changing what the reader does. The test: if the sentence were removed, would the reader act on the checklist any differently? If not, remove it. This kind of writing is especially common in AI-generated text; when revising items with AI, framing the task as "write" or "edit for style" produces less of it than framing it as "review".

Common forms and how to fix them:

- **Weakened expected behavior**, such as "may", "in some cases", or "depends on the situation": state it definitely. When the behavior genuinely varies by product, state what decides it.
- **Negative limits and contrasts**, such as "does not mean", "does not guarantee", or "rather than": state what happens or what the correct approach is. Keep "X is not Y" only when the misconception is common and leads directly to defects, followed by the reason, as in "Sync is not backup: incorrect content is synced to every device just the same."
- **Announcements, self-corrections, and disclaimers**, such as "the following covers only", "strictly speaking", or "for reference only": remove them and write the content directly.

The scope statement (not a compliance standard, no certification) appears once, at the top of the document. Items do not cite external sources; sources are listed in [references.md](references.md).

### Content

- **Broad scope, precise claims.** The bar for inclusion is low; the bar for wording is high. "Offer a portable mode" is acceptable; "every application must store data in its program directory" is not. Numbers are examples, not standards.
- **Outcome first, implementation second.** Item text describes behavior users can observe. Specific APIs, parameters, and platform implementations go into Appendix A, indexed by item ID.
- **Cover the normal path and the failure path together.** If there is saving, cover save failure; if there is sync, cover conflicts; if there is a hotkey, cover registration failure.
- **Prioritize handoffs.** Handoffs between windows, between memory and files, between this machine and others, and between old and new versions are where problems occur most.
- **Note platform differences in parentheses** within the item rather than splitting it.
- **No process machinery.** Do not add state models, acceptance criteria, scoring, or schemas. To support verification, add a walkthrough scenario to scenarios.md.

## Scenario format

Each scenario contains steps, checkpoints, and related items written as ID and title. The guidelines at the top of scenarios.md require disposable samples for scenarios that kill processes, disconnect storage, overwrite, migrate, or uninstall, so individual scenarios do not repeat it. Scenarios do not need to cover every combination of platform, device, and input method.

## Keeping AUDIT.md in sync

AUDIT.md refers to domain and item IDs, conditional domains, and the Baseline/QoL distinction defined in checklist.md. When any of these change, update AUDIT.md in the same pull request.

## Maintaining both languages

The English version in the repository root is primary; the Chinese version is in `zh-CN/`. Update both languages when changing an item. If only one language can be done, say so in the pull request and a maintainer will complete the other.

## Licensing

Contributions are licensed under [CC BY 4.0](LICENSE), the same as the rest of this repository. Submitting a pull request means agreeing to this.
