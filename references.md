# References

English | [简体中文](zh-CN/references.md)

This file lists the sources behind the items in [checklist.md](checklist.md), checked in October 2026. Sources are mainly documents published by platform vendors, standards bodies, government agencies, and software companies; where a normative source already covers a fact, community discussions and individual reports are not listed. The checklist text itself does not cite sources. This file is organized by domain, and each entry states the behavior it supports.

## General principles and standards

- [Nielsen Norman Group · 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/): review angles such as visibility of status, user control and recovery, and recognition over recall.
- [W3C · WCAG 2.2](https://www.w3.org/TR/WCAG22/), [WCAG2ICT](https://www.w3.org/TR/wcag2ict/): accessibility requirements and their interpretation for non-web software.
- [ISO 9241-110:2020](https://www.iso.org/standard/75258.html): interaction principles for human-system dialogue.
- [Google · Site Reliability Engineering · Reliable Product Launches at Scale](https://sre.google/sre-book/reliable-product-launches/): controlling the growth of a launch checklist by backing new questions with real incidents. The "Backed by a source" criterion in CONTRIBUTING.md is based on this.
- [AWS Builders' Library · Making retries safe with idempotent APIs](https://aws.amazon.com/builders-library/making-retries-safe-with-idempotent-APIs/): retries of operations with side effects do not produce duplicate results.

## Platform guidelines and quality checklists

- [Microsoft · UX checklist for desktop applications](https://learn.microsoft.com/en-us/windows/win32/uxguide/top-violations) and [Windows User Experience Interaction Guidelines](https://learn.microsoft.com/en-us/windows/win32/uxguide/): item-by-item review of Windows desktop UI, covering windows, dialogs, controls, keyboard, errors, and help. Written for Windows 7 and not updated since.
- [Microsoft · Windows app design](https://learn.microsoft.com/en-us/windows/apps/design/), [Windows app development best practices](https://learn.microsoft.com/en-us/windows/apps/get-started/best-practices): current Windows app design and development practices.
- [Microsoft · Certification requirements for Windows desktop apps](https://learn.microsoft.com/en-us/previous-versions/windows/win32/win_cert/certification-requirements-for-windows-desktop-apps): archived desktop certification requirements, including rollback of failed installations, multiple users, and saving before shutdown.
- [Apple · Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/): macOS conventions for windows, the menu bar, undo, drag and drop, file management, and notifications.
- [GNOME · Human Interface Guidelines](https://developer.gnome.org/hig/), [Integrating with GNOME](https://developer.gnome.org/documentation/guidelines/maintainer/integrating.html): GNOME interaction conventions and desktop integration checks.
- [KDE · Human Interface Guidelines](https://develop.kde.org/hig/): [Simple by default](https://develop.kde.org/hig/simple_by_default/), [Powerful when needed](https://develop.kde.org/hig/powerful_when_needed/), [Communicating status changes](https://develop.kde.org/hig/status_changes/).
- [Google · Adaptive app quality · Desktop](https://developer.android.com/docs/quality-guidelines/adaptive-app-quality/experiences/desktop): tiered quality requirements for Android apps on desktop, with test IDs.
- [Huawei · HarmonyOS app UX standards](https://developer.huawei.com/consumer/cn/doc/doccenter-ux-design/ux-guidelines-overview-0000001760867048) (Chinese): experience standards for general, large-screen, and PC HarmonyOS apps, with test methods and pass criteria.
- [Digital Agency of Japan · UI checklist](https://www.digital.go.jp/resources/standard_guidelines) (Japanese): concrete checks for input, errors, recognition, and explanatory text.
- [Korea · KRDS digital government design system](https://www.krds.go.kr/html/site/outline/outline_04.html) (Korean): service patterns graded as required, recommended, and excellent.

## DISPLAY · Display and layout

- [Microsoft · High DPI Desktop Application Development on Windows](https://learn.microsoft.com/en-us/windows/win32/hidpi/high-dpi-desktop-application-development-on-windows): system scaling, mixed DPI, and DPI changes from remote desktop sessions.
- [Microsoft · Support snap layouts for desktop apps](https://learn.microsoft.com/en-us/windows/apps/desktop/modernize/ui/apply-snap-layout-menu): how custom title bars and minimum window sizes affect snap layouts.
- [Microsoft · Win32 UX Guide · Layout](https://learn.microsoft.com/en-us/windows/win32/uxguide/vis-layout): larger windows show more content, and body text has a maximum width.
- [GNOME HIG · Adaptive Design](https://developer.gnome.org/hig/guidelines/adaptive.html): layout adaptation to window size.
- [Microsoft · Win32 UX Guide · Tooltips and Infotips](https://learn.microsoft.com/en-us/windows/win32/uxguide/ctrl-tooltips-and-infotips): truncated names can be viewed in full.
- [GitHub · Rendering huge pull requests in the GitHub Copilot app](https://github.blog/engineering/user-experience/rendering-huge-pull-requests-in-the-github-copilot-app/): anchoring the reading position to content when heights change.
- [Krita · Color Management Settings](https://docs.krita.org/en/reference_manual/preferences/color_management_settings.html): separating canvas color space, display configuration, and HDR output.
- [Typora · Zoom](https://support.typora.io/Zoom/), [Slack · Adjust your zoom level in Slack](https://slack.com/help/articles/236067467-Adjust-your-zoom-level-in-Slack): interface zoom set within the application, with a hint panel showing the current factor and a reset.

## TYPO · Fonts and text

- [Apple HIG · Typography](https://developer.apple.com/design/human-interface-guidelines/typography): system fonts, dynamic type sizes, and legibility.
- [Notepad++ · Preferences](https://npp-user-manual.org/docs/preferences/): showing whitespace, line endings, and control characters on demand; the first line as the name of an untitled tab; locking the tab bar and disabling drag of selected text.
- [VS Code · User and workspace settings](https://code.visualstudio.com/docs/configure/settings): `editor.renderWhitespace`; the `@modified` filter and per-setting reset; confirmation before closing only when triggered from the keyboard; session restore can be turned off; untitled editors labeled by content.

## A11Y · Accessibility

- [W3C · ARIA Authoring Practices Guide · Patterns](https://www.w3.org/WAI/ARIA/apg/patterns/), [Developing a Keyboard Interface](https://www.w3.org/WAI/ARIA/apg/practices/keyboard-interface/): keyboard models for composite controls, single Tab stops, and the distinction between focus and selection.
- [W3C · Understanding Label in Name](https://www.w3.org/WAI/WCAG22/Understanding/label-in-name.html): accessible names match the visible text.
- [W3C · WCAG 2.2 · Three Flashes or Below Threshold](https://www.w3.org/TR/WCAG22/#three-flashes-or-below-threshold), [Understanding Pause, Stop, Hide](https://w3c.github.io/wcag/understanding/pause-stop-hide.html): control of flashing and continuous motion.
- [Apple HIG · Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility), [GNOME HIG · Accessibility](https://developer.gnome.org/hig/guidelines/accessibility.html): platform accessibility requirements.
- [Microsoft · Win32 UX Guide · Keyboard](https://learn.microsoft.com/en-us/windows/win32/uxguide/inter-keyboard): Tab order and initial focus.
- [Microsoft · Accessibility Insights for Windows](https://accessibilityinsights.io/docs/windows/overview/): a tool for checking UI Automation semantics and Tab stops.
- [Game Accessibility Guidelines](https://gameaccessibilityguidelines.com/full-list/), [Microsoft · Xbox Accessibility Guidelines](https://learn.microsoft.com/en-us/gaming/accessibility/guidelines): input alternatives, remembered settings, and motion control that carry over to ordinary applications.
- [W3C · Understanding Content on Hover or Focus](https://www.w3.org/WAI/WCAG22/Understanding/content-on-hover-or-focus.html), [Understanding Pointer Cancellation](https://www.w3.org/WAI/WCAG22/Understanding/pointer-cancellation.html): dismissing hover content without moving the pointer; activating on release and canceling by moving off the target.
- [Microsoft · Keyboard shortcuts in Windows](https://support.microsoft.com/en-us/windows/keyboard-shortcuts-in-windows-dcc61a57-8ff0-cffe-9796-cb9706c75eec), [VS Code · Accessibility](https://code.visualstudio.com/docs/configure/accessibility/accessibility): F6 cycles through the regions of a window.
- [Microsoft · Create accessible PDFs](https://support.microsoft.com/en-us/accessibility/office-accessibility/create-accessible-pdfs), [LibreOffice · PDF/UA export](https://help.libreoffice.org/latest/en-US/text/shared/01/ref_pdf_export_universal_accessibility.html): exported documents keep tags, reading order, language, and alternative text.

## INPUT · Keyboard, mouse, IME, and clipboard

- [W3C · UI Events](https://www.w3.org/TR/uievents/): key events during composition and `isComposing`.
- [VS Code · Keyboard layouts in keybindings](https://code.visualstudio.com/docs/configure/keybindings#keyboard-layouts): displaying shortcuts for the current keyboard layout.
- [Apple HIG · Keyboards](https://developer.apple.com/design/human-interface-guidelines/keyboards), [The menu bar](https://developer.apple.com/design/human-interface-guidelines/the-menu-bar): standard macOS shortcuts and a complete menu bar.
- [W3C APG · Dialog (Modal)](https://www.w3.org/WAI/ARIA/apg/patterns/dialog-modal/), [Combobox](https://www.w3.org/WAI/ARIA/apg/patterns/combobox/): closing order of nested overlays and Enter in suggestion lists.
- [KDE · KActionCollection](https://api.kde.org/kactioncollection.html): central management of actions, default shortcuts, and configurability.
- [Microsoft · Shell Clipboard Formats](https://learn.microsoft.com/en-us/windows/win32/shell/clipboard), [Clipboard Formats](https://learn.microsoft.com/en-us/windows/win32/dataxchg/clipboard-formats), [Clipboard Operations](https://learn.microsoft.com/en-us/windows/win32/dataxchg/clipboard-operations): multi-format clipboard data, virtual files, and delayed rendering.
- [Apple · Supporting Drag and Drop Through File Promises](https://developer.apple.com/documentation/appkit/supporting-drag-and-drop-through-file-promises): dragging content whose local file does not exist yet.
- [Apple HIG · Drag and drop](https://developer.apple.com/design/human-interface-guidelines/drag-and-drop): move and copy rules, scrolling during a drag, selection after a drop, and confirmation before drops that cannot be undone.
- [Microsoft · Win32 UX Guide · Mouse and Pointers](https://learn.microsoft.com/en-us/windows/win32/uxguide/inter-mouse): Esc cancels a drag, and clicks take effect on release.
- [PatternFly · Bulk selection](https://www.patternfly.org/patterns/bulk-selection/), [eBay Playbook · Selection](https://playbook.ebay.com/design-system/patterns/selection), [Adobe · React Aria · Selection](https://react-aria.adobe.com/selection): counts, scope, and clearing for selections across pages.
- [W3C APG · Checkbox](https://www.w3.org/WAI/ARIA/apg/patterns/checkbox/): representing a mixed state.
- [Microsoft · PowerToys PowerRename](https://learn.microsoft.com/en-us/windows/powertoys/powerrename), [VS Code · Basic Editing](https://code.visualstudio.com/docs/editing/codebasics): previewing old and new values before batch renames and replacements.
- [VS Code · User interface](https://code.visualstudio.com/docs/editing/getting-started/userinterface): preview tabs and permanent tabs.
- [Krita · Tablet Settings](https://docs.krita.org/en/reference_manual/preferences/tablet_settings.html): distinguishing pressure input from mouse events.
- [GNOME HIG · Text fields](https://developer.gnome.org/hig/patterns/controls/text-fields.html), [KDE HIG · Getting input](https://develop.kde.org/hig/getting_input/), [Apple HIG · Entering data](https://developer.apple.com/design/human-interface-guidelines/entering-data): input constraints, inline correction, and direct entry of precise values.
- [W3C · Understanding Accessible Authentication (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/accessible-authentication-minimum.html): authentication accepts pasting and password managers.
- [GNOME · Evolution spell checking](https://teams.pages.gitlab.gnome.org/Websites/help.gnome.org/evolution/mail-composer-spellcheck.html): choosing dictionaries by language.
- [Slack · Set your Enter key preference](https://slack.com/help/articles/115005523006-Set-your-Enter-key-preference), [Manage your keyboard layout](https://slack.com/help/articles/115005429666-Manage-your-keyboard-layout), [Feishu · Desktop keyboard shortcuts](https://www.feishu.cn/hc/zh-CN/articles/894529368028) (Chinese): a setting for whether Enter sends or starts a new line, excluded from "reset all shortcuts"; a manual layout choice appears only when detection fails.
- [Blender · Keymap preferences](https://docs.blender.org/manual/en/latest/editors/preferences/keymap.html), [Input preferences](https://docs.blender.org/manual/en/latest/editors/preferences/input.html): keymap presets matching other products and export of only the differences; emulated numpad and three-button mouse; switching the tablet API between Windows Ink and WinTab.
- [Krita · General Settings](https://docs.krita.org/en/reference_manual/preferences/general_settings.html): choosing which clipboard representation to paste, with "ask each time" and a network-dependent option; font DPI conversion for files from older versions.
- [JetBrains · Appearance](https://www.jetbrains.com/help/idea/settings-appearance.html): drag and drop only while Alt is held, to avoid moving files, tabs, and panels by accident.
- [LibreOffice · Security Options and Warnings](https://help.libreoffice.org/latest/en-US/text/shared/optionen/securityoptionsdialog.html): Ctrl-click required to follow hyperlinks.
- [Microsoft · Text Services Framework](https://learn.microsoft.com/en-us/windows/win32/tsf/what-is-text-services-framework), [Apple · Writing Tools](https://developer.apple.com/documentation/appkit/writing-tools): speech, handwriting, and system writing tools reach text areas through the platform text interfaces; custom text views need to adopt them.
- [Windows Terminal · Interaction](https://learn.microsoft.com/en-us/windows/terminal/customize-settings/interaction), [iTerm2 · Menu Items](https://iterm2.com/documentation-menu-items.html): warnings before pasting multiple lines or text ending in a line break.
- [Blender · Fields](https://docs.blender.org/manual/en/latest/interface/controls/buttons/fields.html): mathematical expressions and units in number fields.
- [Microsoft Teams · Check your spelling in multiple languages](https://support.microsoft.com/en-us/teams/chat/check-your-spelling-in-multiple-languages-in-microsoft-teams), [LibreOffice · Selecting the Document Language](https://help.libreoffice.org/latest/en-US/text/shared/guide/language_select.html): proofing languages set independently of the UI language, down to a paragraph or selection.

## WINDOW · Windows

- [Qt · QWindow](https://doc.qt.io/qt-6/qwindow.html): platforms such as Wayland do not let applications set window positions.
- [Apple · applicationShouldTerminateAfterLastWindowClosed](https://developer.apple.com/documentation/appkit/nsapplicationdelegate/applicationshouldterminateafterlastwindowclosed(_:)): whether to quit after the last window closes.
- [Microsoft · Win32 UX Guide · Window Management](https://learn.microsoft.com/en-us/windows/win32/uxguide/win-window-mgt), [GNOME HIG · Windows](https://developer.gnome.org/hig/patterns/containers/windows.html), [Apple HIG · Modality](https://developer.apple.com/design/human-interface-guidelines/modality): main and owned windows, and document-level modality.
- [Microsoft · Kernel object namespaces](https://learn.microsoft.com/en-us/windows/win32/termserv/kernel-object-namespaces), [Apple · LSMultipleInstancesProhibited](https://developer.apple.com/documentation/bundleresources/information-property-list/lsmultipleinstancesprohibited): the scope of single-instance checks across user sessions.
- [Microsoft · Navigation history and backwards navigation](https://learn.microsoft.com/en-us/windows/uwp/layout/navigation-history-and-backwards-navigation), [JetBrains · Recent files and locations](https://www.jetbrains.com/help/idea/recent-files-and-changes.html): Back and Forward along the visited path.
- [Sublime Text · Changelog](https://www.sublimetext.com/download): external open requests run after loading finishes; old undo history is not restored after the file changed on disk; recovered unsaved files keep their encoding.
- [mpv · Manual · --drag-and-drop](https://mpv.io/manual/stable/#options-drag-and-drop), [--focus-on](https://mpv.io/manual/stable/#options-focus-on): whether an externally opened file replaces or is appended to the playlist, and whether the window takes focus.
- [Raycast · Settings](https://manual.raycast.com/settings), [Alfred · Appearance](https://www.alfredapp.com/help/appearance/), [Alfred · Snippets troubleshooting](https://www.alfredapp.com/help/troubleshooting/snippets/): which display the launcher appears on and whether it moves to the active Space; returning to the root search after a delay; a non-activating panel by default; reporting a Secure Input lock and slowing down key events for targets that drop pasted text.
- [JetBrains · System settings](https://www.jetbrains.com/help/idea/system-settings.html), [Telegram Desktop · Settings strings](https://translations.telegram.org/en/tdesktop/settings/): confirmation before exiting; "Hold to Quit" and a warning before quitting with the shortcut; "Send with Enter" versus "Send with Ctrl+Enter".
- [Audacity · The Audacity IPC server failed to initialize](https://support.audacityteam.org/au3/troubleshooting/error-codes/error-the-audacity-ipc-server-failed-to-initialize), [Jan · Troubleshooting](https://docs.jan.ai/desktop/troubleshooting): a visible error when the single-instance channel or the local service port cannot be set up, including a stale process from the previous run.

## APPEARANCE · Appearance

- [W3C APG · Window Splitter](https://www.w3.org/WAI/ARIA/apg/patterns/windowsplitter/): keyboard control of splitters and restoring position after collapsing.
- [Microsoft · Win32 UX Guide · List Views](https://learn.microsoft.com/en-us/windows/win32/uxguide/ctrl-list-views), [Semi Design · Table](https://semi.design/design/zh-CN/show/table) (Chinese): choosing columns, resizing columns, and fixed headers and columns.
- [VS Code · Modernizing the VS Code UI](https://code.visualstudio.com/blogs/2026/10/15/modern-ui): a layout density setting added after a redesign, with the classic interface kept for a transition period.
- [Apple HIG · Split views](https://developer.apple.com/design/human-interface-guidelines/split-views), [Sidebars](https://developer.apple.com/design/human-interface-guidelines/sidebars), [WinUI · NavigationView](https://learn.microsoft.com/en-us/windows/apps/design/controls/navigationview), [Microsoft · Show or hide the ribbon](https://support.microsoft.com/en-us/office/show-or-hide-the-ribbon-in-office-d946b26e-0c8c-402d-a0f7-c6efa296b527): several visible ways to reveal hidden panes, a pane toggle button, and a way back to a hidden ribbon.
- [Microsoft · Acrylic material](https://learn.microsoft.com/en-us/windows/apps/design/style/acrylic), [AppKit · accessibilityDisplayShouldReduceTransparency](https://developer.apple.com/documentation/appkit/nsworkspace/accessibilitydisplayshouldreducetransparency): solid backgrounds when the user turns off transparency.

## SETTINGS · Settings

- [Qt · QSettings](https://doc.qt.io/qt-6/qsettings.html), [QStandardPaths](https://doc.qt.io/qt-6/qstandardpaths.html): native storage locations for configuration.
- [VS Code · Settings Sync](https://code.visualstudio.com/docs/configure/settings-sync), [Profiles](https://code.visualstudio.com/docs/configure/profiles): machine-specific settings are not overwritten by sync, and shortcuts sync per platform.
- [GNOME HIG · Switches](https://developer.gnome.org/hig/patterns/controls/switches.html): switches show whether a feature has actually taken effect.
- [Microsoft · Win32 UX Guide · Confirmations](https://learn.microsoft.com/en-us/windows/win32/uxguide/mess-confirm): where "Don't show again" belongs, and not asking to save changes the user did not make.
- [Everything · Options](https://www.voidtools.com/support/everything/options/): showing only modified settings and resetting one value; a per-computer, per-user database name for portable use; search and run history kept, cleared, or expired separately from being disabled; programs launched while running as administrator also run elevated.
- [mpv · Manual · --reset-on-next-file](https://mpv.io/manual/stable/#options-reset-on-next-file), [Hidemaru · Settings by file type](https://help.maruo.co.jp/hidemaru/html/280_Support.html) (Japanese): adjustments made during playback carry over to the next file or are reset per option; a separate group of settings per file type.
- [Blender · Defaults](https://docs.blender.org/manual/en/latest/getting_started/configuration/defaults.html), [Inkscape · FAQ](https://inkscape.org/learn/faq/): importing preferences and extensions from the previous version; user-added extensions, palettes, and templates live in the user directory and survive upgrades; a DPI change on opening old files offers conversion choices.
- [LibreOffice · Load/Save General options](https://help.libreoffice.org/latest/en-US/text/shared/optionen/01010200.html): printer settings and the view position stored in a document are not applied by default when another user opens it.
- [LM Studio · User or Developer](https://lmstudio.ai/docs/app/user-interface/modes), [Zoom · Changing settings in the Zoom Workplace desktop and mobile app](https://support.zoom.com/hc/en/article?id=zm_kb&sysparm_article=KB0060612): a User mode that shows only the chat interface and a Developer mode with full access; rarely used options grouped under "Advanced" on each settings page.
- [VS Code · Settings](https://code.visualstudio.com/docs/configure/settings): search filters, advanced settings in search results, and copying a setting's ID.
- [Microsoft · Launch the Windows Settings app](https://learn.microsoft.com/en-us/windows/apps/develop/launch/launch-settings-app): `ms-settings:` links open a specific system settings page.

## LOCALE · Language and region

- [Microsoft · Handling a new era in the Japanese calendar in .NET](https://devblogs.microsoft.com/dotnet/handling-a-new-era-in-the-japanese-calendar-in-net/): handling a change of Japanese era.
- [IANA · Time Zone Database](https://www.iana.org/time-zones): time zone rules change several times a year as governments revise them; applications follow the system's data or update their bundled copy.
- [Unicode · UAX #15 Normalization Forms](https://www.unicode.org/reports/tr15/), [Syncthing · autoNormalize](https://docs.syncthing.net/advanced/folder-autonormalize.html): canonically equivalent sequences, and file names that differ in normalization across systems.
- [Microsoft · StrCmpLogicalW](https://learn.microsoft.com/en-us/windows/win32/api/shlwapi/nf-shlwapi-strcmplogicalw), [Apple · localizedStandardCompare:](https://developer.apple.com/documentation/foundation/nsstring/localizedstandardcompare(_:)): sorting that treats digits as numbers, consistent with the file manager.
- [JetBrains · Search Everywhere](https://www.jetbrains.com/help/idea/searching-everywhere.html), [VS Code 1.86 release notes](https://code.visualstudio.com/updates/v1_86): finding actions and settings in a localized UI, and showing original English names next to translations.

## DATA · Data protection, saving, and recovery

- [Microsoft · ReplaceFileW](https://learn.microsoft.com/en-us/windows/win32/api/winbase/nf-winbase-replacefilew), [MoveFileExW](https://learn.microsoft.com/en-us/windows/win32/api/winbase/nf-winbase-movefileexw): keeping attributes and access control when replacing a file, and writing through the cache.
- [SQLite · Atomic Commit](https://sqlite.org/atomiccommit.html), [Online Backup API](https://www.sqlite.org/backup.html), [Write-Ahead Logging](https://www.sqlite.org/wal.html): atomic commits, consistent backups of a running database, and the WAL file as part of database state.
- [Apple HIG · File management](https://developer.apple.com/design/human-interface-guidelines/file-management): autosave, browsing versions, and the unsaved-changes indicator.
- [Apple HIG · Undo and redo](https://developer.apple.com/design/human-interface-guidelines/undo-and-redo): naming the action in undo items and making the result visible.
- [Syncthing · Understanding Synchronization](https://docs.syncthing.net/users/syncing.html): file watchers miss events and need periodic scans; case conflicts.
- [Obsidian · Back up your files](https://obsidian.md/help/backup), [Troubleshoot Obsidian Sync](https://obsidian.md/help/sync/troubleshoot): sync is not backup; conflict handling by file type.
- [GIMP · Export File](https://docs.gimp.org/3.0/en/gimp-export-dialog.html), [LibreOffice Calc · Importing and Exporting CSV](https://help.libreoffice.org/latest/en-US/text/scalc/guide/csv_formula.html), [1Password · Export your data](https://support.1password.com/export/): full projects versus exchange formats, and stating the scope of an export.
- [Zotero · Data directory in cloud storage](https://www.zotero.org/support/kb/data_directory_in_cloud_storage_folder): risk of database corruption in synced folders.
- [Zotero · Why can't Zotero find a linked file?](https://www.zotero.org/support/kb/missing_linked_file), [Typora · Images](https://support.typora.io/Images/): relinking external resources and updating references when moving resources in the app.
- [Slack · Send and read messages](https://slack.com/help/articles/201457107-Send-and-read-messages), [Telegram · Drafts](https://telegram.org/blog/drafts): a central place for drafts and scheduled messages, and draft markers in the chat list.
- [Zotero · General preferences](https://www.zotero.org/support/preferences/general), [Joplin · Attachments](https://joplinapp.org/help/apps/attachments/): choosing whether imported tags are attached; attachments no longer referenced by any note are removed after the note history retention period.
- [JetBrains · Invalidate caches](https://www.jetbrains.com/help/idea/invalidate-caches.html), [Thunderbird · Rebuilding the Global Database](https://support.mozilla.org/en-US/kb/rebuilding-global-database): rebuilding derived indexes from the interface without touching source data.
- [Bandizip · Preventing data loss with safe backups](https://cn.bandisoft.com/bandizip/help/backup/) (Chinese): testing the archive before the source files are deleted.
- [CLaunch · Other options](https://pyonky.github.io/CLaunch-Help/ja/optOther.htm) (Japanese): a single-user mode for carrying a portable copy on a USB stick, and registering items with relative paths.
- [Microsoft · Save a copy before editing](https://support.microsoft.com/en-us/office/collab-files/save-a-copy-before-editing-to-prevent-changing-the-original-file): switching to a copy before editing when AutoSave writes to the original.
- [Microsoft · Data import and analysis options in Excel](https://support.microsoft.com/en-us/excel/data-import-and-analysis-options-in-excel), [LibreOffice · Text Import](https://help.libreoffice.org/latest/en-US/text/shared/00/00000208.html): controlling type conversion on import, including leading zeros, long numbers, dates, and the interpreting locale.

## FILE · Files and resources

- [Apple · Accessing files from the macOS App Sandbox](https://developer.apple.com/documentation/security/accessing-files-from-the-macos-app-sandbox): persistent access and security-scoped bookmarks in the sandbox.
- [Microsoft · Build a Cloud Sync Engine that Supports Placeholder Files](https://learn.microsoft.com/en-us/windows/win32/cfapi/build-a-cloud-file-sync-engine): online-only placeholder files.
- [KDE HIG · Simple by default](https://develop.kde.org/hig/simple_by_default/): files opened without the Open dialog also enter recent files; irreversible deletion is postponed while an undo prompt is shown.
- [OBS · Standard Recording Output Guide](https://obsproject.com/kb/standard-recording-output-guide): a file name template for recordings with variables for source and time.
- [Syncthing · FAQ](https://docs.syncthing.net/users/faq.html), [Joplin · FAQ](https://joplinapp.org/help/faq/): a missing folder marker stops syncing instead of propagating deletions; notes lost after the WebDAV URL was changed to an empty target.
- [JetBrains · Read-only files](https://www.jetbrains.com/help/idea/read-only-files.html): read-only state shown in the status bar with the reasons it cannot be cleared.
- [mpv · Manual · --autocreate-playlist](https://mpv.io/manual/stable/#options-autocreate-playlist), [IrfanView · Browsing properties](https://www.irfanview.net/help/guida/hlp_propertiesx_others_1.htm): browsing neighboring files in the same directory, filtering by type, what happens at the end of the folder, and jumping to the next file after a deletion.

## TASK · Tasks, responsiveness, and resources

- [Microsoft · Win32 UX Guide · Progress Bars](https://learn.microsoft.com/en-us/windows/win32/uxguide/progress-bars), [GNOME HIG · Progress bars](https://developer.gnome.org/hig/patterns/feedback/progress-bars.html): overall progress, remaining time, and Cancel versus Stop.
- [JetBrains · Experimental zero-latency typing](https://blog.jetbrains.com/idea/2015/08/experimental-zero-latency-typing-in-intellij-idea-15-eap/): latency from input to display.
- [Microsoft Edge · Performance features](https://support.microsoft.com/en-us/edge/learn-about-performance-features-in-microsoft-edge): exceptions to background throttling for playback and capture.
- [OBS · Hybrid MP4 / MOV](https://obsproject.com/kb/hybrid-mp4): what main content and metadata survive an interrupted recording.
- [VS Code · Release notes 1.102](https://code.visualstudio.com/updates/v1_102): a Dock badge when an unfocused window needs confirmation.
- [Obsidian · Settings](https://obsidian.md/help/settings), [Help and support](https://obsidian.md/help/resources): a notice when startup takes longer than expected, a startup time breakdown that can be copied, and rebuilding the vault cache from settings.
- [qBittorrent · Explanation of Options](https://github.com/qbittorrent/qBittorrent/wiki/Explanation-of-Options-in-qBittorrent): resume data saved at a set interval; running an external program on completion; bringing the add dialog to the front; preventing sleep while torrents are active; a network interface and IP binding for all connections.
- [OBS · GPU Selection Guide](https://obsproject.com/kb/gpu-selection-guide), [Blender · System preferences](https://docs.blender.org/manual/en/latest/editors/preferences/system.html): which GPU the application uses on multi-GPU machines; an "Allow Online Access" switch; registering and unregistering file associations.
- [Affinity Photo 2 · Preferences](https://affinity.help/photo2/English.lproj/pages/Workspace/preferences.html): a RAM usage limit and a disk usage warning; tablet input method; preferring metafile over raster when pasting; renderer choice; resetting the font cache.

## NETWORK · Network, offline, and sync

- [RFC 8252 · OAuth 2.0 for Native Apps](https://www.rfc-editor.org/rfc/rfc8252.html): signing in through the system browser and returning to the app.
- [Electron · Security](https://www.electronjs.org/docs/latest/tutorial/security): secure transport and certificate validation.
- [Apple · App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/): guideline 2.5.5 requires apps to work on IPv6-only networks.
- [JetBrains · HTTP Proxy](https://www.jetbrains.com/help/idea/settings-http-proxy.html): testing the connection through the proxy, exceptions, and which connections the proxy settings affect.
- [OBS · Stream Connection Troubleshooting](https://obsproject.com/kb/stream-connection-troubleshooting), [Syncthing · Configuration](https://docs.syncthing.net/users/config.html): binding to a network interface and IP family.

## SYSTEM · System integration

- [XDG Desktop Portal](https://flatpak.github.io/xdg-desktop-portal/docs/): [Background](https://flatpak.github.io/xdg-desktop-portal/docs/doc-org.freedesktop.portal.Background.html) and [Global Shortcuts](https://flatpak.github.io/xdg-desktop-portal/docs/doc-org.freedesktop.portal.GlobalShortcuts.html), launch at login and global shortcuts in a sandbox.
- [Microsoft · Win32 UX Guide · Notifications](https://learn.microsoft.com/en-us/windows/win32/uxguide/mess-notif), [GNOME HIG · Notifications](https://developer.gnome.org/hig/patterns/feedback/notifications.html): withdrawing notifications, foreground behavior, and how often to raise them again.
- [Slack · Troubleshoot Slack notifications](https://slack.com/help/articles/360001559367-Troubleshoot-Slack-notifications): badges remaining on conversations already read.
- [Microsoft · WM_QUERYENDSESSION](https://learn.microsoft.com/en-us/windows/win32/shutdown/wm-queryendsession), [ShutdownBlockReasonCreate](https://learn.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-shutdownblockreasoncreate), [RegisterApplicationRestart](https://learn.microsoft.com/en-us/windows/win32/api/winbase/nf-winbase-registerapplicationrestart): saving before shutdown, stating why shutdown is blocked, and restarting after a system update.
- [Raycast · Games](https://manual.raycast.com/games), [Troubleshooting](https://manual.raycast.com/troubleshooting): hotkeys paused while a game is in the foreground; shortcuts that stop firing after a system update, AltGr conflicts on non-US layouts, and snippets that do not expand in some applications.
- [PowerToys · PowerToys Run](https://learn.microsoft.com/en-us/windows/powertoys/run), [Keyboard Manager](https://learn.microsoft.com/en-us/windows/powertoys/keyboard-manager), [Awake](https://learn.microsoft.com/en-us/windows/powertoys/awake), [mpv · Manual · --stop-screensaver](https://mpv.io/manual/stable/#options-stop-screensaver): ignoring shortcuts in full-screen mode and choosing the monitor; re-enabling after another hook interferes; keeping the system awake with a separate switch for the screen; the screensaver re-enabled when playback is not active.
- [Listary · Hotkey](https://help.listary.com/options-hotkey), [Integration](https://help.listary.com/options-integration): disabling the hotkey in full-screen games and in listed applications; what pressing the hotkey again does.
- [Clibor · Settings](https://chigusa-web.com/clibor/howto/settings/), [CLaunch · Disabling](https://pyonky.github.io/CLaunch-Help/ja/optDisable.htm), [Temporarily disabling CLaunch](https://pyonky.github.io/CLaunch-Help/ja/extSuspend.htm) (Japanese): disabling hotkeys while a remote desktop client is in use; per-application and full-screen disabling; a suspend mode shown on the tray icon; the double-tap interval; paste key and wait before pasting; deleting history on exit.

## INSTALL · Installation, updates, and uninstallation

- [Homebrew · Cask Cookbook](https://docs.brew.sh/Cask-Cookbook): the `auto_updates` declaration and the scope of `zap`.
- [VS Code · Portable mode](https://code.visualstudio.com/docs/setup/portable): portable distribution and automatic updates.
- [Mozilla · Install an older version of Firefox](https://support.mozilla.org/en-US/kb/install-older-version-firefox): downgrade protection and profile data.
- [Microsoft · SmartScreen reputation and code signing](https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/smartscreen-reputation): a newly signed version can still trigger warnings until it builds reputation.
- [Microsoft · WebView2 distribution](https://learn.microsoft.com/microsoft-edge/webview2/concepts/distribution): distributing a runtime dependency.
- [Tauri · Updater](https://v2.tauri.app/plugin/updater/), [Sparkle · Documentation](https://sparkle-project.org/documentation/): signed update packages and an embedded public key.
- [NIST NVD · CVE-2024-39698](https://nvd.nist.gov/vuln/detail/CVE-2024-39698): a bypass of electron-updater's signature check.
- [NIST NVD · CVE-2026-95625](https://nvd.nist.gov/vuln/detail/CVE-2026-95625): before 2.12.0, the Tauri updater's version manifest was unsigned and could be used to force a downgrade.
- [1Password · Windows release notes](https://releases.1password.com/windows/stable/): installing an update on quit no longer relaunches the app; silent updates no longer bring it to the foreground; secondary windows open on the active display.
- [PowerToys · Run PowerToys in administrator mode](https://learn.microsoft.com/en-us/windows/powertoys/administrator), [Bandizip · Cannot open an archive on a mapped network drive](https://cn.bandisoft.com/bandizip/help/cannot-open-an-archive-in-a-network-mapped-drive/) (Chinese): a notice when an elevated process is detected, and mapped network drives invisible to an elevated process.

## PRIVACY · Permissions, accounts, and privacy

- [Electron · safeStorage](https://www.electronjs.org/docs/latest/api/safe-storage): on Linux, credential protection depends on the secret store backend.
- [RFC 9110 · Redirection](https://www.rfc-editor.org/rfc/rfc9110.html#section-15.4): the scope of credentials across redirects.
- [KeePass · FAQ](https://keepass.info/help/kb/faq.html): clearing only what the application itself placed on the clipboard.
- [1Password · Auto-lock](https://support.1password.com/auto-lock/): app lock and idle detection.
- [RFC 6455 · WebSocket Origin Considerations](https://www.rfc-editor.org/rfc/rfc6455.html#section-10.2), [Microsoft · Named Pipe Security and Access Rights](https://learn.microsoft.com/en-us/windows/win32/ipc/named-pipe-security-and-access-rights): access boundaries for local services and inter-process communication.
- [VS Code · FAQ](https://code.visualstudio.com/docs/supporting/faq), [Firefox · Shield studies](https://support.mozilla.org/en-US/kb/shield): experiments disabled separately from telemetry; viewing and leaving active studies.
- [Audacity · Info for system administrators](https://support.audacityteam.org/au3/special-uses/info-for-system-administrators): turning off update checks and cloud modules individually.
- [Hidemaru · Privacy settings](https://help.maruo.co.jp/hidemaru/html/070_Env_Privacy.html), [Sakura Editor · General settings](https://sakura-editor.github.io/help/HLP000081.html) (Japanese): clearing each class of history separately or automatically on exit; confirmation on "close all" and on exit.
- [Adobe Acrobat · Redact and sanitize PDFs](https://helpx.adobe.com/acrobat/desktop/protect-documents/redact-pdfs/redacting-sanitizing.html), [PDF-XChange · Redacting and sanitizing](https://help.pdf-xchange.com/pdfxe11/redacting-pages-and-sanitizing-documents.html): redaction permanently removes content, distinct from marks not yet applied.

## HELP · Help, feedback, and diagnostics

- [Microsoft · Win32 UX Guide · Error Messages](https://learn.microsoft.com/en-us/windows/win32/uxguide/mess-error), [Fluent 2 · Tooltip](https://fluent2.microsoft.design/components/web/react/core/tooltip/usage): presenting errors, and explaining why a control is unavailable and when it becomes available.
- [LibreOffice · Troubleshoot Mode](https://help.libreoffice.org/latest/en-US/text/shared/01/profile_safe_mode.html), [VS Code · Resolving extension issues with bisect](https://code.visualstudio.com/blogs/2021/02/16/extension-bisect): safe mode and bisecting extensions.
- [OBS · Known Application Conflicts](https://obsproject.com/kb/known-conflicts): a maintained list of overlay, antivirus, and driver conflicts with their symptoms and handling.
- [Krita · FAQ](https://docs.krita.org/en/KritaFAQ.html): save failures caused by Controlled Folder Access, freezes caused by dictionary and sandbox software, resetting the configuration with a backup, a log viewer for tablet problems, and causes of slow startup.
- [Feishu · White screen, lag, freeze, or crash on Windows](https://www.feishu.cn/hc/zh-CN/articles/413916844794) (Chinese), [Firefox · Troubleshoot Firefox crashes](https://support.mozilla.org/en-US/kb/troubleshoot-firefox-crashes-closing-or-quitting): the Feishu article lists known conflicting software and how to handle it; Firefox's about:third-party lists loaded third-party modules with their vendors and can block them.
- [Blender · Troubleshooting · Startup](https://docs.blender.org/manual/en/latest/troubleshooting/startup.html), [Crashes](https://docs.blender.org/manual/en/latest/troubleshooting/crash.html): console output and debug launch scripts when no window appears.

## FIND · Search and filtering

- [JetBrains · Search Everywhere](https://www.jetbrains.com/help/idea/searching-everywhere.html), [Obsidian · Search](https://obsidian.md/help/plugins/search): search scope, exclusions, and query explanation.
- [Obsidian · Release notes 1.8.2](https://obsidian.md/changelog/2025-01-22-desktop-v1.8.2/): revealing the active file in the file explorer.
- [Obsidian · Bookmarks](https://obsidian.md/help/plugins/bookmarks), [Sakura Editor · Bookmarks](https://sakura-editor.github.io/help/HLP000205.html) (Japanese): personal markers on objects and lines.

## TRUST · Untrusted content

- [Microsoft 365 · What is Protected View?](https://support.microsoft.com/en-us/office/collab-files/what-is-protected-view), [VS Code · Workspace Trust](https://code.visualstudio.com/docs/editing/workspaces/workspace-trust), [LibreOffice · Macro Security](https://help.libreoffice.org/latest/en-GB/text/shared/optionen/macrosecurity.html): restricted viewing and the scope of trust grants.
- [Mozilla · Remote Content in Messages](https://support.mozilla.org/en-US/kb/remote-content-in-messages), [Thunderbird's Scam Detection](https://support.mozilla.org/en-US/kb/thunderbirds-scam-detection): network requests from untrusted content and verifying link targets.
- [MITRE · CWE-22 Path Traversal](https://cwe.mitre.org/data/definitions/22.html): archive imports writing outside the target directory.
- [Microsoft · IAttachmentExecute::Save](https://learn.microsoft.com/en-us/windows/win32/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-save): attaching origin marks when saving downloaded content.

## EXTEND · Extensions and plugins

- [Obsidian · Plugin security](https://obsidian.md/help/plugin-security), [VS Code · Extension runtime security](https://code.visualstudio.com/docs/configure/extensions/extension-runtime-security), [Extension Marketplace](https://code.visualstudio.com/docs/configure/extensions/extension-marketplace): the actual permissions of extensions, publisher trust, and disabling.
- [VS Code · Release notes 1.92](https://code.visualstudio.com/updates/v1_92): consent is asked again when an extension update adds executable code; extensions installed by hand do not auto-update by default.

## AUTOMATE · External automation

- [LibreOffice · Starting the software with parameters](https://help.libreoffice.org/latest/en-US/text/shared/guide/start_parameters.html), [Apple · Run shortcuts from the command line](https://support.apple.com/guide/shortcuts-mac/run-shortcuts-from-the-command-line-apd455c82f02/mac): command-line entry points, exit codes, and headless execution.
- [Microsoft · UI Automation Control Patterns](https://learn.microsoft.com/en-us/windows/win32/winauto/uiauto-controlpatternsoverview), [Use the AutomationId Property](https://learn.microsoft.com/en-us/dotnet/framework/ui-automation/use-the-automationid-property): object identity and actions in a drivable UI.
- [Sketch · MCP server](https://www.sketch.com/docs/mcp-server/), [1Password · CLI app integration](https://developer.1password.com/docs/cli/app-integration/): delegation interfaces that the user turns on and can revoke.

## LICENSE · Licensing, trials, and expiration

- [1Password · Frozen account](https://support.1password.com/frozen-account/), [JetBrains · Offline use and activation](https://sales.jetbrains.com/hc/en-gb/articles/206544169-Do-I-need-and-internet-connection-to-activate-and-use-JetBrains-products), [Sketch · Move a license to another device](https://www.sketch.com/support/mac-only-licenses/move-to-another-device/), [Obsidian · License](https://obsidian.md/license): retrieving work after expiration, offline validation, and moving to a new device.

## MANAGED · Organizational deployment and managed environments

- [VS Code · Enterprise](https://code.visualstudio.com/docs/enterprise/overview): [managing updates](https://code.visualstudio.com/docs/enterprise/updates) and [managing extensions](https://code.visualstudio.com/docs/enterprise/extensions).
- [Microsoft · Create an offline installation of Visual Studio](https://learn.microsoft.com/en-us/visualstudio/install/create-an-offline-installation-of-visual-studio), [JetBrains · IntelliJ IDEA installation guide](https://www.jetbrains.com/help/idea/installation-guide.html): offline layouts, silent installation, and installation scope.

## FAIR · Respecting user choice

- [Microsoft · How Microsoft identifies malware and potentially unwanted applications](https://learn.microsoft.com/en-us/defender-xdr/criteria): bundling, misleading prompts, and default options.
- [1Password · Manage your subscription](https://support.1password.com/manage-subscription/): where to cancel a subscription, including other purchase channels.
- [Apple · App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/): guideline 5.1.1(v) on account deletion.
- [VS Code · Release notes 1.96](https://code.visualstudio.com/updates/v1_96): preinstalled extensions the user removed are not reinstalled after a restart.

## COMPONENT · Bundled components and helper processes

- [FFmpeg · License and Legal Considerations](https://www.ffmpeg.org/legal.html): license notices and source availability for bundled components.
- [Microsoft · IAudioSessionControl::SetDisplayName](https://learn.microsoft.com/en-us/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setdisplayname): the display name of a helper process in the volume mixer.

## MEDIA · Playback and capture

- [Microsoft · System Media Transport Controls](https://learn.microsoft.com/en-us/windows/apps/develop/media-playback/integrate-with-systemmediatransportcontrols), [freedesktop · MPRIS](https://specifications.freedesktop.org/mpris/latest/), [Apple HIG · Playing audio](https://developer.apple.com/design/human-interface-guidelines/playing-audio): system media controls.
- [Microsoft · User-Mode Audio Components](https://learn.microsoft.com/en-us/windows/win32/coreaudio/user-mode-audio-components): how shared and exclusive access affect other applications.
- [Apple · Capturing screen content in macOS](https://developer.apple.com/documentation/screencapturekit/capturing-screen-content-in-macos): capture scope by window, application, or display.
- [mpv · Manual · --cursor-autohide](https://mpv.io/manual/stable/#options-cursor-autohide), [IrfanView · Full screen properties](https://www.irfanview.net/help/guida/hlp_propertiesx_full_screen.htm): hiding the pointer after a period of inactivity, optionally only in full screen; temporary display options in full screen do not change the saved option.

## TRANSFER · Delivering transfer results

- [aria2 · Manual](https://aria2.github.io/manual/en/html/aria2c.html): integrity checks, resuming, and RPC access control.

## Technology documentation for Appendix A

- **Microsoft**: [Job Objects](https://learn.microsoft.com/en-us/windows/win32/procthread/job-objects) (`JOB_OBJECT_LIMIT_KILL_ON_JOB_CLOSE`).
- **Linux**: [prctl(2)](https://man7.org/linux/man-pages/man2/prctl.2.html) (`PR_SET_PDEATHSIG`).
- **Electron**: [net](https://www.electronjs.org/docs/latest/api/net/), [globalShortcut](https://www.electronjs.org/docs/latest/api/global-shortcut), [BrowserWindow](https://www.electronjs.org/docs/latest/api/browser-window).
- **Tauri**: [Security](https://v2.tauri.app/security/), [Capabilities](https://v2.tauri.app/security/capabilities/).
- **Qt**: [QSaveFile](https://doc.qt.io/qt-6/qsavefile.html), [QFileSystemWatcher](https://doc.qt.io/qt-6/qfilesystemwatcher.html).
