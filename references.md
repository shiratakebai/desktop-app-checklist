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

## TYPO · Fonts and text

- [Apple HIG · Typography](https://developer.apple.com/design/human-interface-guidelines/typography): system fonts, dynamic type sizes, and legibility.

## A11Y · Accessibility

- [W3C · ARIA Authoring Practices Guide · Patterns](https://www.w3.org/WAI/ARIA/apg/patterns/), [Developing a Keyboard Interface](https://www.w3.org/WAI/ARIA/apg/practices/keyboard-interface/): keyboard models for composite controls, single Tab stops, and the distinction between focus and selection.
- [W3C · Understanding Label in Name](https://www.w3.org/WAI/WCAG22/Understanding/label-in-name.html): accessible names match the visible text.
- [W3C · WCAG 2.2 · Three Flashes or Below Threshold](https://www.w3.org/TR/WCAG22/#three-flashes-or-below-threshold), [Understanding Pause, Stop, Hide](https://w3c.github.io/wcag/understanding/pause-stop-hide.html): control of flashing and continuous motion.
- [Apple HIG · Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility), [GNOME HIG · Accessibility](https://developer.gnome.org/hig/guidelines/accessibility.html): platform accessibility requirements.
- [Microsoft · Win32 UX Guide · Keyboard](https://learn.microsoft.com/en-us/windows/win32/uxguide/inter-keyboard): Tab order and initial focus.
- [Microsoft · Accessibility Insights for Windows](https://accessibilityinsights.io/docs/windows/overview/): a tool for checking UI Automation semantics and Tab stops.
- [Game Accessibility Guidelines](https://gameaccessibilityguidelines.com/full-list/), [Microsoft · Xbox Accessibility Guidelines](https://learn.microsoft.com/en-us/gaming/accessibility/guidelines): input alternatives, remembered settings, and motion control that carry over to ordinary applications.

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

## WINDOW · Windows

- [Qt · QWindow](https://doc.qt.io/qt-6/qwindow.html): platforms such as Wayland do not let applications set window positions.
- [Apple · applicationShouldTerminateAfterLastWindowClosed](https://developer.apple.com/documentation/appkit/nsapplicationdelegate/applicationshouldterminateafterlastwindowclosed(_:)): whether to quit after the last window closes.
- [Microsoft · Win32 UX Guide · Window Management](https://learn.microsoft.com/en-us/windows/win32/uxguide/win-window-mgt), [GNOME HIG · Windows](https://developer.gnome.org/hig/patterns/containers/windows.html), [Apple HIG · Modality](https://developer.apple.com/design/human-interface-guidelines/modality): main and owned windows, and document-level modality.
- [Microsoft · Kernel object namespaces](https://learn.microsoft.com/en-us/windows/win32/termserv/kernel-object-namespaces), [Apple · LSMultipleInstancesProhibited](https://developer.apple.com/documentation/bundleresources/information-property-list/lsmultipleinstancesprohibited): the scope of single-instance checks across user sessions.
- [Microsoft · Navigation history and backwards navigation](https://learn.microsoft.com/en-us/windows/uwp/layout/navigation-history-and-backwards-navigation), [JetBrains · Recent files and locations](https://www.jetbrains.com/help/idea/recent-files-and-changes.html): Back and Forward along the visited path.
- [Sublime Text · Changelog](https://www.sublimetext.com/download): external open requests run after loading finishes; old undo history is not restored after the file changed on disk; recovered unsaved files keep their encoding.

## APPEARANCE · Appearance

- [W3C APG · Window Splitter](https://www.w3.org/WAI/ARIA/apg/patterns/windowsplitter/): keyboard control of splitters and restoring position after collapsing.
- [Microsoft · Win32 UX Guide · List Views](https://learn.microsoft.com/en-us/windows/win32/uxguide/ctrl-list-views), [Semi Design · Table](https://semi.design/design/zh-CN/show/table) (Chinese): choosing columns, resizing columns, and fixed headers and columns.
- [VS Code · Modernizing the VS Code UI](https://code.visualstudio.com/blogs/2026/10/15/modern-ui): a layout density setting added after a redesign, with the classic interface kept for a transition period.

## SETTINGS · Settings

- [Qt · QSettings](https://doc.qt.io/qt-6/qsettings.html), [QStandardPaths](https://doc.qt.io/qt-6/qstandardpaths.html): native storage locations for configuration.
- [VS Code · Settings Sync](https://code.visualstudio.com/docs/configure/settings-sync), [Profiles](https://code.visualstudio.com/docs/configure/profiles): machine-specific settings are not overwritten by sync, and shortcuts sync per platform.
- [GNOME HIG · Switches](https://developer.gnome.org/hig/patterns/controls/switches.html): switches show whether a feature has actually taken effect.
- [Microsoft · Win32 UX Guide · Confirmations](https://learn.microsoft.com/en-us/windows/win32/uxguide/mess-confirm): where "Don't show again" belongs, and not asking to save changes the user did not make.

## LOCALE · Language and region

- [Microsoft · Handling a new era in the Japanese calendar in .NET](https://devblogs.microsoft.com/dotnet/handling-a-new-era-in-the-japanese-calendar-in-net/): handling a change of Japanese era.

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

## FILE · Files and resources

- [Apple · Accessing files from the macOS App Sandbox](https://developer.apple.com/documentation/security/accessing-files-from-the-macos-app-sandbox): persistent access and security-scoped bookmarks in the sandbox.
- [Microsoft · Build a Cloud Sync Engine that Supports Placeholder Files](https://learn.microsoft.com/en-us/windows/win32/cfapi/build-a-cloud-file-sync-engine): online-only placeholder files.
- [KDE HIG · Simple by default](https://develop.kde.org/hig/simple_by_default/): files opened without the Open dialog also enter recent files; irreversible deletion is postponed while an undo prompt is shown.

## TASK · Tasks, responsiveness, and resources

- [Microsoft · Win32 UX Guide · Progress Bars](https://learn.microsoft.com/en-us/windows/win32/uxguide/progress-bars), [GNOME HIG · Progress bars](https://developer.gnome.org/hig/patterns/feedback/progress-bars.html): overall progress, remaining time, and Cancel versus Stop.
- [JetBrains · Experimental zero-latency typing](https://blog.jetbrains.com/idea/2015/08/experimental-zero-latency-typing-in-intellij-idea-15-eap/): latency from input to display.
- [Microsoft Edge · Performance features](https://support.microsoft.com/en-us/edge/learn-about-performance-features-in-microsoft-edge): exceptions to background throttling for playback and capture.
- [OBS · Hybrid MP4 / MOV](https://obsproject.com/kb/hybrid-mp4): what main content and metadata survive an interrupted recording.
- [VS Code · Release notes 1.102](https://code.visualstudio.com/updates/v1_102): a Dock badge when an unfocused window needs confirmation.

## NETWORK · Network, offline, and sync

- [RFC 8252 · OAuth 2.0 for Native Apps](https://www.rfc-editor.org/rfc/rfc8252.html): signing in through the system browser and returning to the app.
- [Electron · Security](https://www.electronjs.org/docs/latest/tutorial/security): secure transport and certificate validation.
- [Apple · App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/): guideline 2.5.5 requires apps to work on IPv6-only networks.

## SYSTEM · System integration

- [XDG Desktop Portal](https://flatpak.github.io/xdg-desktop-portal/docs/): [Background](https://flatpak.github.io/xdg-desktop-portal/docs/doc-org.freedesktop.portal.Background.html) and [Global Shortcuts](https://flatpak.github.io/xdg-desktop-portal/docs/doc-org.freedesktop.portal.GlobalShortcuts.html), launch at login and global shortcuts in a sandbox.
- [Microsoft · Win32 UX Guide · Notifications](https://learn.microsoft.com/en-us/windows/win32/uxguide/mess-notif), [GNOME HIG · Notifications](https://developer.gnome.org/hig/patterns/feedback/notifications.html): withdrawing notifications, foreground behavior, and how often to raise them again.
- [Slack · Troubleshoot Slack notifications](https://slack.com/help/articles/360001559367-Troubleshoot-Slack-notifications): badges remaining on conversations already read.
- [Microsoft · WM_QUERYENDSESSION](https://learn.microsoft.com/en-us/windows/win32/shutdown/wm-queryendsession), [ShutdownBlockReasonCreate](https://learn.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-shutdownblockreasoncreate), [RegisterApplicationRestart](https://learn.microsoft.com/en-us/windows/win32/api/winbase/nf-winbase-registerapplicationrestart): saving before shutdown, stating why shutdown is blocked, and restarting after a system update.

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

## PRIVACY · Permissions, accounts, and privacy

- [Electron · safeStorage](https://www.electronjs.org/docs/latest/api/safe-storage): on Linux, credential protection depends on the secret store backend.
- [RFC 9110 · Redirection](https://www.rfc-editor.org/rfc/rfc9110.html#section-15.4): the scope of credentials across redirects.
- [KeePass · FAQ](https://keepass.info/help/kb/faq.html): clearing only what the application itself placed on the clipboard.
- [1Password · Auto-lock](https://support.1password.com/auto-lock/): app lock and idle detection.
- [RFC 6455 · WebSocket Origin Considerations](https://www.rfc-editor.org/rfc/rfc6455.html#section-10.2), [Microsoft · Named Pipe Security and Access Rights](https://learn.microsoft.com/en-us/windows/win32/ipc/named-pipe-security-and-access-rights): access boundaries for local services and inter-process communication.

## HELP · Help, feedback, and diagnostics

- [Microsoft · Win32 UX Guide · Error Messages](https://learn.microsoft.com/en-us/windows/win32/uxguide/mess-error), [Fluent 2 · Tooltip](https://fluent2.microsoft.design/components/web/react/core/tooltip/usage): presenting errors, and explaining why a control is unavailable and when it becomes available.
- [LibreOffice · Troubleshoot Mode](https://help.libreoffice.org/latest/en-US/text/shared/01/profile_safe_mode.html), [VS Code · Resolving extension issues with bisect](https://code.visualstudio.com/blogs/2021/02/16/extension-bisect): safe mode and bisecting extensions.

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

## TRANSFER · Delivering transfer results

- [aria2 · Manual](https://aria2.github.io/manual/en/html/aria2c.html): integrity checks, resuming, and RPC access control.

## Technology documentation for Appendix A

- **Microsoft**: [Job Objects](https://learn.microsoft.com/en-us/windows/win32/procthread/job-objects) (`JOB_OBJECT_LIMIT_KILL_ON_JOB_CLOSE`).
- **Linux**: [prctl(2)](https://man7.org/linux/man-pages/man2/prctl.2.html) (`PR_SET_PDEATHSIG`).
- **Electron**: [net](https://www.electronjs.org/docs/latest/api/net/), [globalShortcut](https://www.electronjs.org/docs/latest/api/global-shortcut), [BrowserWindow](https://www.electronjs.org/docs/latest/api/browser-window).
- **Tauri**: [Security](https://v2.tauri.app/security/), [Capabilities](https://v2.tauri.app/security/capabilities/).
- **Qt**: [QSaveFile](https://doc.qt.io/qt-6/qsavefile.html), [QFileSystemWatcher](https://doc.qt.io/qt-6/qfilesystemwatcher.html).
