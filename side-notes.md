# Side Notes

English | [简体中文](zh-CN/side-notes.md)

This file collects material related to [checklist.md](checklist.md) that is not part of the checklist itself: related topics outside the checklist's scope, product examples of checklist items, and similar checklists. The sources behind the items are listed in [references.md](references.md). This file is not part of an audit, and [AUDIT.md](AUDIT.md) does not ask agents to check it item by item.

## Related topics outside the scope

The following topics relate to the checklist but are not items. Each entry gives the reason.

- **Platform visual specifications** (spacing, corner radius, color, icon size): these concern implementing known requirements correctly, and the checklist does not map conformance to platform HIGs.
- **Windows access key assignment, macOS Services menus and floating panels, GNOME gesture reservations**: platform conventions to implement according to the respective guidelines. Custom-drawn interfaces often lack access keys; see INPUT-03 Discoverable shortcuts.
- **In-app clipboard history**: the evidence comes mainly from code and text editors, and it has to be designed together with the clipboard protection in PRIVACY-07 Displaying and copying sensitive content.
- **Viewing a list and details side by side**: a layout decision for each product to make according to its tasks.
- **Holding a modifier to switch tools temporarily**: limited to canvas, drawing, and design products.
- **Routing notifications to the device in use**: limited to instant messaging products.
- **Marking participants from outside the organization**: limited to collaboration and communication products.
- **Showing the remaining time for expiring downloads**: so far seen only in chat products.
- **Accuracy of store listings and app descriptions**: part of running a distribution channel.
- **Regional restrictions and age ratings**: legal and operational matters.
- **Switching audio and subtitle tracks in media players**: a feature of specific products.
- **Design process self-review lists** (such as Tencent CDC's interaction self-check list): these check whether the design process is complete, not what the product can do.

## Product examples

The following product behaviors correspond to checklist items and can help explain an item to a team.

- **Slack**: the "Drafts & sent" view in the sidebar lists drafts, scheduled messages, and sent messages in one place. See DATA-14 Unfinished work is discoverable after leaving and TASK-06 Entry point for background tasks.
- **Telegram Desktop**: drafts appear in the chat list and sync across devices. See DATA-14 Unfinished work is discoverable after leaving.
- **WeChat, QQ**: unsent text shows as "[Draft]" in the conversation list, and a recalled message can be edited and sent again. See DATA-14 Unfinished work is discoverable after leaving and TASK-03 Stop waiting, cancel the task, or revert the result.
- **Telegram Desktop**: messages are marked as read only in the active window, never while the session is locked. See SYSTEM-14 Accurate unread and pending state.
- **Sublime Text**: new, unmodified files show no unsaved marker; old undo history is not restored after the file changed on disk; recovered unsaved files keep their encoding. See DATA-01 Visible save state, WINDOW-06 Workspace and view context restoration, and DATA-02 Autosave and crash recovery.
- **VS Code**: a single click opens a preview tab that becomes permanent after editing or a double-click; after a redesign, a layout density setting was added and an option to return to the classic interface was kept for a transition period. See INPUT-17 Separating browsing from activation, APPEARANCE-04 Layout density, and HELP-08 What's new after an update.
- **VS Code**: when an unfocused window needs the user's confirmation, a badge appears on the Dock icon and disappears when the window gains focus. See TASK-06 Entry point for background tasks.
- **GitHub Copilot app**: reading position is anchored to content identity during reflow, so opening the file tree sidebar does not move the file being read. See DISPLAY-08 No flashing, no jumping, stable targets.
- **1Password**: secondary windows open on the active display, and quitting with an update pending no longer restarts the app. See WINDOW-12 Placement and stacking of owned windows and INSTALL-03 Update preferences.
- **Telegram Desktop**: Ctrl+Shift+number shortcuts were removed by default after conflicting with input methods, and taskbar window previews are hidden while locked. See INPUT-04 Customizable shortcuts and PRIVACY-13 Scope of app lock protection.
- **Obsidian**: after a bookmark is deleted with the keyboard, focus moves to the next item; Esc in the quick switcher restores the previous selection; the file explorer can reveal the active file. See A11Y-02 Visible focus, logical order, focus return; INPUT-17 Separating browsing from activation; and FIND-02 Recognizable matches, navigable results.
- **Obsidian, Sakura Editor, Feishu**: bookmarks, line bookmarks, and message markers. See FIND-05 Personal markers for later.
- **Typora**: moving an image within the app updates the references in the Markdown file. See DATA-11 Relocating external resources.
- **New Outlook**: Undo Send delays delivery by up to 30 seconds. See INPUT-14 Undo over confirmation.
- **Figma**: when selected objects have different property values, the panel shows a mixed value. See INPUT-11 Multi-selection and batch actions.

## Similar checklists

The following checklists overlap in part with this one and can supplement it for a particular platform or area. Among the public Chinese, English, Japanese, and Korean sources reviewed, none was found that covers cross-platform desktop capabilities, data and task handoffs, and less visible QoL behaviors together.

| Checklist | Scope | Difference from this checklist |
| --- | --- | --- |
| [Microsoft UX checklist for desktop applications](https://learn.microsoft.com/en-us/windows/win32/uxguide/top-violations) | Windows desktop UI | Focused on controls and platform consistency; no data protection, recovery, IME, installation, or privacy |
| [Google Adaptive app quality · Desktop](https://developer.android.com/docs/quality-guidelines/adaptive-app-quality/experiences/desktop) | Android apps on desktop | Tiered, numbered, with test methods; about 30 items, Android only |
| [HarmonyOS app UX standards](https://developer.huawei.com/consumer/cn/doc/doccenter-ux-design/ux-guidelines-overview-0000001760867048) (Chinese) | General, large-screen, and PC HarmonyOS apps | Detailed on keyboard, mouse, and windows; little on data and lifecycle |
| [Digital Agency UI checklist](https://www.digital.go.jp/resources/standard_guidelines) (Japanese) | Government websites and services | Concrete input and form behavior; no desktop windows, tray, installation, or file handoff |
| [KRDS](https://www.krds.go.kr/html/site/outline/outline_04.html) (Korean) | Korean digital government services | Graded as required, recommended, and excellent; government services |
| [Vercel web-interface-guidelines](https://github.com/vercel-labs/web-interface-guidelines) | Web interface QoL | Ships an agent instruction file and is close in form to this checklist; web only |
| [Front-End-Checklist](https://github.com/thedaviddias/Front-End-Checklist) | Web front-end release checks | Ships an MCP server; web only |
| [mac-arsed-mac-app](https://github.com/bartreardon/skills/blob/main/mac-arsed-mac-app/SKILL.md) | macOS native conventions | A skill file for AI agents with about 30 points; macOS only |
| [SmartHR UI design usability checklist](https://smarthr.design/products/usability/usability-checklist/) (Japanese) | SaaS web design review | 22 checks mapped to JIS X 25010 |
| [checklist.design](https://www.checklist.design/) | Pages, components, and flows | Answers "what should this page have"; no desktop category |
| [Alipay experience design review list](https://developer.aliyun.com/article/82295) (Chinese) | Mobile products | Organized by situational factors and error branches; community repost |
