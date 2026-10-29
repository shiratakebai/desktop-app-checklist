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
- **Generation controls specific to LLM front ends** (regenerating automatically when a result is unsatisfactory, continuing automatically by length, the pacing of character-by-character display): limited to LLM front ends; no counterpart was found in other kinds of desktop applications. The general parts are covered by TASK-05 Retry and idempotency and TASK-10 Viewport behavior for streaming output.

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
- **VS Code, JetBrains IDEs**: unfocused editor groups and terminals are dimmed or get a different background, so the user can tell which pane will receive typed input without trying a keystroke. See A11Y-02 Visible focus, logical order, focus return.
- **Feishu**: when a shortcut conflicts with an embedded app or website, the user chooses whether the embedded content, Feishu, or both in turn respond; shortcuts that cannot be changed say so on their detail page. See INPUT-04 Customizable shortcuts.
- **Clibor, Hidemaru, Quicker**: Clibor's clipboard monitor can delay storing an entry and ignore updates repeated within a short time, so the "retrieving data" placeholder is not recorded; Hidemaru can switch its monitoring method when another clipboard tool conflicts; Quicker's FAQ lists the clipboard-monitoring programs that cause lag. See INPUT-10 Clipboard formats and lifetime.
- **Figma, Feishu, Telegram Desktop**: recently closed tabs or windows reopen from the tab menu or with Ctrl + Shift + T, and repeated presses restore them in closing order. See INPUT-14 Undo over confirmation and FILE-02 Recent files.
- **VS Code, Firefox**: tabs can wrap onto several rows, pinned tabs can sit on their own row, and whether a new tab opens next to the current one or at the end is a setting. See WINDOW-06 Workspace and view context restoration.
- **mpv, IrfanView**: whether the window resizes and moves with the next object of a different size is the user's choice; IrfanView can keep the pointer over the Next/Previous toolbar buttons. See WINDOW-01 Position and size restoration.
- **Raycast, Alfred**: the input source switches to a chosen one when the launcher appears and switches back when it closes. See WINDOW-10 Quick summon and focus return.
- **ShareX, Snipaste**: pinned images can be closed all at once or by group, new pins default to a corner, edge, or the center, and click-through can be toggled and released for all pins at once. See WINDOW-09 Always on top.
- **Obsidian, Hidemaru**: the open files, panels, and layout can be saved as a named workspace and loaded in one step. See APPEARANCE-05 Adjustable, resettable panels.
- **VS Code, Notepad++, JetBrains IDEs**: with the menu bar hidden, VS Code and Notepad++ show it temporarily on Alt or F10 on Windows and Linux; JetBrains IDEs can tuck the main menu under a hamburger button. See APPEARANCE-05 Adjustable, resettable panels.
- **Telegram Desktop, Discord, Alfred**: a theme can be previewed before it is applied; Telegram Desktop reverts to the previous theme when the user does not confirm within a countdown. See APPEARANCE-06 Safe custom colors.
- **Alfred, Everything, Listary, Snipaste**: each troubleshooting page explains why settings fail to persist: Alfred lists permission problems and Dropbox conflict files; Everything requires enabling "Store settings and data in %APPDATA%"; Listary offers a "Safe Exit" from the tray to force a save; Snipaste explains that the configuration reverts to defaults when config.ini in the program directory cannot be written. See SETTINGS-04 Reliable persistence, tolerant of manual edits.
- **mpv, Sakura Editor, Hidemaru**: a separate group of settings applies automatically by extension, protocol, or file type. See SETTINGS-05 Clear scope.
- **Telegram Desktop, Zoom, SillyTavern, Blender**: the download location, connecting to a Zoom Room, tag handling on import, and the treatment of unsaved images on save are each offered as a setting with "ask every time", "always", and "never". See SETTINGS-07 Reset by category.
- **Typora**: the file list sorts in natural order, comparing numbers in names by value. See LOCALE-05 Multilingual text handling.
- **Hidemaru**: autosave runs immediately when the user switches windows. See DATA-02 Autosave and crash recovery.
- **Blender, Krita, Affinity Photo**: the number of undo steps or the undo memory limit is a setting; Blender states that disabling global undo also disables Adjust Last Operation. See DATA-04 Undo and redo targets.
- **Obsidian, VS Code**: history snapshots show their differences from the current version, and old content can be copied out without restoring the whole file. See DATA-05 Version history and backup.
- **Blender, Krita, LibreOffice**: a replace-save keeps the previous version as a backup file (`.blend1`, `~`, `.BAK`); Krita can place it in the same directory, the user directory, or the temporary directory and warns that the last one gets emptied; LibreOffice falls back to its backup directory when the same directory is not writable; Blender states that autosave files in the temporary directory may disappear after a reboot or a disk cleanup. See DATA-05 Version history and backup.
- **JetBrains IDEs, VS Code**: when file watching exceeds the system limit, the application says so and falls back to scanning directories; directories that need no watching can be excluded. See DATA-07 External changes and conflicts.
- **Obsidian, Typora**: Obsidian gives each device a user-editable name that identifies it in the sync log and in conflicted-copy file names; Typora's license page lists activated devices and can deactivate one remotely. See DATA-07 External changes and conflicts and LICENSE-04 Changing or losing devices.
- **Firefox, Audacity**: Firefox can keep files opened only for viewing in a temporary directory instead of the downloads folder; Audacity shows the free space when a temporary directory is chosen, rejects FAT volumes, and advises against network drives and USB sticks. See DATA-09 Transparent, movable data location.
- **Firefox**: after a crash, the Restore Session page lists the previous windows and tabs with checkboxes for which to restore; a repeated crash offers starting a new session. See DATA-14 Unfinished work is discoverable after leaving.
- **Audacity, Blender, LibreOffice, Notepad++, IrfanView**: open, save, import, and export, or fonts, textures, and render output, each remember their own directory or take a fixed one, and an empty setting falls back to the last location; Notepad++ can follow the current document and does not update the last directory when a dialog is cancelled; IrfanView's slideshow and batch dialogs can open in the last-used or the current folder; Blender uses the system temporary directory when its own does not exist. See FILE-01 Platform file dialogs and persistent access.
- **Typora, Notepad++**: frequently used folders can be pinned in the recent list so they are not evicted, and clearing the list asks whether to clear pinned items too; files on an intermittently reachable network drive can be kept in the recent list without a check at launch. See FILE-02 Recent files.
- **Listary, Everything**: a third-party file manager and its arguments can be set for opening the containing folder; Listary's FAQ explains that "Application not found" comes from another file manager taking over the folder association. See FILE-06 Reveal in system.
- **JetBrains IDEs**: closing a tool window with a running process offers to terminate the process, disconnect, or ask each time. See TASK-06 Entry point for background tasks.
- **Krita**: the FAQ explains how to correct the offset caused by a monitor or tablet connected after system startup. See TASK-09 Sleep, wake, network, and device changes.
- **Obsidian, Zotero**: the sync log can be filtered for conflicts and lists skipped files with the reason; Zotero shows the status and a report ID on the sync error icon. See NETWORK-04 Visible sync queue.
- **Telegram Desktop**: when the built-in transport fails to connect, the message says it keeps retrying in the background and offers opening the page in a browser instead. See NETWORK-02 Timeouts and reconnection.
- **Telegram Desktop, WeCom, Discord, Steam**: Telegram Desktop and Discord set automatic downloads separately by content type, source, and size limit, with an exception list; WeCom never downloads confidential files automatically; Steam restricts automatic updates to a time window and has a per-game setting for downloading other updates while playing. See NETWORK-06 Data usage control.
- **Slack, Telegram Desktop**: the notification settings can send a sample notification; Telegram Desktop explains when launch at startup has been disabled in Windows Settings and offers to open them. See SYSTEM-03 System notifications and attention.
- **Zoom, Feishu**: each shortcut in the list has its own checkbox for working globally. See SYSTEM-04 Global shortcuts.
- **CLaunch, Alfred, Snipaste, PowerToys**: CLaunch warns, before the tray icon is hidden with every feature disabled, that it can no longer be shown, and running the program again forces it to appear; Alfred's and Snipaste's documentation explain how to open preferences after the menu bar or tray icon is hidden; the PowerToys Keyboard Manager FAQ explains how to stop a wrong remapping quickly and warns about orphaned keys. See SYSTEM-11 Alternatives when system features are unavailable.
- **OBS Studio, Audacity**: the application lists the screen recording, camera, microphone, and accessibility permissions it needs with their purposes in one place, and gives the authorization steps for each platform. See PRIVACY-02 Handling revoked permissions.
- **Ditto, Alfred, Clibor**: Ditto honors the Windows clipboard exclusion formats, keeps marked content out of its history, and can exclude clips by regular expression and process name; Alfred's clipboard history is off by default and ignores Keychain Access, 1Password, and similar applications by default; Clibor can stop monitoring at startup, delete the history on exit, and encrypt stored data. See PRIVACY-10 When and why the clipboard is read.
- **Telegram Desktop, Syncthing**: Telegram Desktop's app lock can be unlocked with Windows Hello or the system password after the passcode has been entered once, and it explains that a passcode prevents launching minimized; Syncthing's FAQ gives the way to reset a forgotten GUI password. See PRIVACY-13 Scope of app lock protection.
- **VS Code, Notepad++**: opening Find seeds the query with the selected text, selections above a length threshold are not seeded, and a large selection turns on "find in selection" automatically. See FIND-04 Repeated searches and FIND-01 Visible scope and exclusions.
- **Bandizip, 7-Zip**: files extracted from an archive carrying an origin mark carry the same mark. See TRUST-06 Handing over origin marks on downloaded content.
- **Thunderbird, foobar2000**: Thunderbird can warn before an update that will disable add-ons; foobar2000's FAQ lists each error message shown when a component is refused and what to do about it. See EXTEND-03 Controlled updates.
- **VS Code, JetBrains IDEs**: when launched from an icon, the application reads the login shell's environment to find the tools available in a terminal, and reports the reason when the read times out or fails. See COMPONENT-01 Coexistence with system copies.
- **Slack**: settings deployed by an organization are either defaults, which users can still change, or enforced values, which are locked. See MANAGED-03 Visible policy control.
- **Zoom**: system notifications are silenced while the desktop is shared, and whether the application's own toolbars and meeting notifications appear in the shared picture is a choice. See MEDIA-05 Confirming the screen capture scope.
- **Zoom**: audio and video stop automatically when the computer locks or the screen saver starts during a meeting. See MEDIA-04 Actual capture state and stop control.
- **IntelliJ IDEA**: with a language pack enabled, settings search and Find Action match both the localized names and the original English names. See LOCALE-05 Multilingual text handling and SETTINGS-02 Searchable settings.
- **VS Code**: in a non-English UI the command palette shows each command's English name on a second line; every setting has a Copy Setting ID action; the title bar has persistent toggles for the primary side bar, panel, and secondary side bar. See LOCALE-05 Multilingual text handling, SETTINGS-02 Searchable settings, and APPEARANCE-05 Adjustable, resettable panels.
- **GNOME Settings**: the Japanese translation keeps the English search keywords for each panel and adds kanji, kana, and romaji readings. See LOCALE-05 Multilingual text handling.
- **Firefox**: the settings search finds content in subdialogs behind buttons and shows the matching keyword next to the button. See SETTINGS-02 Searchable settings.
- **GIMP**: action search lists unavailable actions after the available ones, with the reason they are unavailable; size fields accept arithmetic with units. See INPUT-05 Command palette and INPUT-18 Input constraints and inline correction.
- **Blender**: translation of interface labels, tooltips, and the default names of new data can be turned on separately; tooltips can show the Python identifier. See LOCALE-01 UI language and SETTINGS-02 Searchable settings.
- **LibreOffice Calc**: English function names can be used instead of localized ones, which switches formula input, display, and the function wizard together. See LOCALE-01 UI language.

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
