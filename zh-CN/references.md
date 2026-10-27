# 参考资料

[English](../references.md) | 简体中文

本文列出 [checklist.md](checklist.md) 中条目所依据的来源，核对日期为 2026 年 10 月。来源以平台方、标准组织、政府机构和软件公司发布的文档为主；规范性来源已覆盖的事实，不再列出社区讨论或个人报告。条目正文不引用来源，本文按领域组织，每项说明其支撑的行为。

## 通用原则与标准

- [Nielsen Norman Group · 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/)：状态可见、用户控制与恢复、识别优于回忆等检查角度。
- [W3C · WCAG 2.2](https://www.w3.org/TR/WCAG22/)、[WCAG2ICT](https://www.w3.org/TR/wcag2ict/)：无障碍要求及其在非 Web 软件中的解释。
- [ISO 9241-110:2020](https://www.iso.org/standard/75258.html)：人机交互的对话原则。
- [Google · Site Reliability Engineering · Reliable Product Launches at Scale](https://sre.google/sre-book/reliable-product-launches/)：发布检查清单的增长控制，新增问题以真实事故为依据。CONTRIBUTING.md 的"有出处"标准据此设立。
- [AWS Builders' Library · Making retries safe with idempotent APIs](https://aws.amazon.com/builders-library/making-retries-safe-with-idempotent-APIs/)：有副作用的操作在重试时不产生重复结果。

## 平台指南与质量清单

- [Microsoft · UX checklist for desktop applications](https://learn.microsoft.com/en-us/windows/win32/uxguide/top-violations) 与 [Windows User Experience Interaction Guidelines](https://learn.microsoft.com/en-us/windows/win32/uxguide/)：Windows 桌面界面的逐项检查，覆盖窗口、对话框、控件、键盘、错误与帮助。为 Windows 7 编写，此后未更新。
- [Microsoft · Windows app design](https://learn.microsoft.com/en-us/windows/apps/design/)、[Windows app development best practices](https://learn.microsoft.com/en-us/windows/apps/get-started/best-practices)：当前的 Windows 应用设计与开发实践。
- [Microsoft · Certification requirements for Windows desktop apps](https://learn.microsoft.com/en-us/previous-versions/windows/win32/win_cert/certification-requirements-for-windows-desktop-apps)：已归档的桌面应用认证要求，含安装失败回滚、多用户与关机前保存。
- [Apple · Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/)：macOS 的窗口、菜单栏、撤销、拖放、文件管理与通知约定。
- [GNOME · Human Interface Guidelines](https://developer.gnome.org/hig/)、[Integrating with GNOME](https://developer.gnome.org/documentation/guidelines/maintainer/integrating.html)：GNOME 应用的交互约定与桌面集成检查。
- [KDE · Human Interface Guidelines](https://develop.kde.org/hig/)：[Simple by default](https://develop.kde.org/hig/simple_by_default/)、[Powerful when needed](https://develop.kde.org/hig/powerful_when_needed/)、[Communicating status changes](https://develop.kde.org/hig/status_changes/)。
- [Google · Adaptive app quality · Desktop](https://developer.android.com/docs/quality-guidelines/adaptive-app-quality/experiences/desktop)：Android 应用在桌面环境下的分层质量要求，附测试编号。
- [华为 · HarmonyOS 应用 UX 体验标准](https://developer.huawei.com/consumer/cn/doc/doccenter-ux-design/ux-guidelines-overview-0000001760867048)：鸿蒙通用、大屏与电脑应用的体验标准，附测试方法与判定标准。
- [日本数字厅 · UI 检查表](https://www.digital.go.jp/resources/standard_guidelines)：输入、错误、识别与说明类的具体检查项。
- [韩国 · KRDS 数字政府设计系统](https://www.krds.go.kr/html/site/outline/outline_04.html)：按必需、推荐、优秀分级的服务模式。

## DISPLAY · 显示与布局

- [Microsoft · High DPI Desktop Application Development on Windows](https://learn.microsoft.com/en-us/windows/win32/hidpi/high-dpi-desktop-application-development-on-windows)：系统缩放、混合 DPI 与远程桌面引起的 DPI 变化。
- [Microsoft · Support snap layouts for desktop apps](https://learn.microsoft.com/en-us/windows/apps/desktop/modernize/ui/apply-snap-layout-menu)：自绘标题栏与最小窗口尺寸对贴靠布局的影响。
- [Microsoft · Win32 UX Guide · Layout](https://learn.microsoft.com/en-us/windows/win32/uxguide/vis-layout)：窗口变大时显示更多内容，正文设最大宽度。
- [GNOME HIG · Adaptive Design](https://developer.gnome.org/hig/guidelines/adaptive.html)：窗口尺寸变化时的布局适应。
- [Microsoft · Win32 UX Guide · Tooltips and Infotips](https://learn.microsoft.com/en-us/windows/win32/uxguide/ctrl-tooltips-and-infotips)：被截断的名称可查看全文。
- [GitHub · Rendering huge pull requests in the GitHub Copilot app](https://github.blog/engineering/user-experience/rendering-huge-pull-requests-in-the-github-copilot-app/)：内容高度变化时按对象锚定阅读位置。
- [Krita · Color Management Settings](https://docs.krita.org/en/reference_manual/preferences/color_management_settings.html)：画布色彩空间、显示配置与 HDR 输出的区分。

## TYPO · 字体与文本

- [Apple HIG · Typography](https://developer.apple.com/design/human-interface-guidelines/typography)：系统字体、动态字号与可读性。

## A11Y · 无障碍

- [W3C · ARIA Authoring Practices Guide · Patterns](https://www.w3.org/WAI/ARIA/apg/patterns/)、[Developing a Keyboard Interface](https://www.w3.org/WAI/ARIA/apg/practices/keyboard-interface/)：复合控件的键盘模型、单一 Tab 停靠、焦点与选中的区分。
- [W3C · Understanding Label in Name](https://www.w3.org/WAI/WCAG22/Understanding/label-in-name.html)：无障碍名称与可见文字一致。
- [W3C · WCAG 2.2 · Three Flashes or Below Threshold](https://www.w3.org/TR/WCAG22/#three-flashes-or-below-threshold)、[Understanding Pause, Stop, Hide](https://w3c.github.io/wcag/understanding/pause-stop-hide.html)：闪烁与持续动态内容的控制。
- [Apple HIG · Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility)、[GNOME HIG · Accessibility](https://developer.gnome.org/hig/guidelines/accessibility.html)：平台的无障碍要求。
- [Microsoft · Win32 UX Guide · Keyboard](https://learn.microsoft.com/en-us/windows/win32/uxguide/inter-keyboard)：Tab 顺序与初始焦点。
- [Microsoft · Accessibility Insights for Windows](https://accessibilityinsights.io/docs/windows/overview/)：UI Automation 语义与 Tab 停靠的检查工具。
- [Game Accessibility Guidelines](https://gameaccessibilityguidelines.com/full-list/)、[Microsoft · Xbox Accessibility Guidelines](https://learn.microsoft.com/en-us/gaming/accessibility/guidelines)：输入替代、设置记忆和动效控制，可迁移到普通应用。

## INPUT · 键盘、鼠标、输入法与剪贴板

- [W3C · UI Events](https://www.w3.org/TR/uievents/)：组合输入期间的按键事件与 `isComposing`。
- [VS Code · Keyboard layouts in keybindings](https://code.visualstudio.com/docs/configure/keybindings#keyboard-layouts)：按当前键盘布局显示快捷键。
- [Apple HIG · Keyboards](https://developer.apple.com/design/human-interface-guidelines/keyboards)、[The menu bar](https://developer.apple.com/design/human-interface-guidelines/the-menu-bar)：macOS 标准快捷键与完整菜单栏。
- [W3C APG · Dialog (Modal)](https://www.w3.org/WAI/ARIA/apg/patterns/dialog-modal/)、[Combobox](https://www.w3.org/WAI/ARIA/apg/patterns/combobox/)：嵌套浮层的关闭顺序与候选列表中的 Enter。
- [KDE · KActionCollection](https://api.kde.org/kactioncollection.html)：动作、默认快捷键与可配置性的统一管理。
- [Microsoft · Shell Clipboard Formats](https://learn.microsoft.com/en-us/windows/win32/shell/clipboard)、[Clipboard Formats](https://learn.microsoft.com/en-us/windows/win32/dataxchg/clipboard-formats)、[Clipboard Operations](https://learn.microsoft.com/en-us/windows/win32/dataxchg/clipboard-operations)：多格式剪贴板、虚拟文件与延迟渲染。
- [Apple · Supporting Drag and Drop Through File Promises](https://developer.apple.com/documentation/appkit/supporting-drag-and-drop-through-file-promises)：尚未生成本地文件时的拖放。
- [Apple HIG · Drag and drop](https://developer.apple.com/design/human-interface-guidelines/drag-and-drop)：移动与复制的规则、拖动中自动滚动、放下后的选择、不可撤销拖放前确认。
- [Microsoft · Win32 UX Guide · Mouse and Pointers](https://learn.microsoft.com/en-us/windows/win32/uxguide/inter-mouse)：Esc 取消拖动，点击在松开时生效。
- [PatternFly · Bulk selection](https://www.patternfly.org/patterns/bulk-selection/)、[eBay Playbook · Selection](https://playbook.ebay.com/design-system/patterns/selection)、[Adobe · React Aria · Selection](https://react-aria.adobe.com/selection)：跨页选择的计数、范围与清除。
- [W3C APG · Checkbox](https://www.w3.org/WAI/ARIA/apg/patterns/checkbox/)：混合状态的表示。
- [Microsoft · PowerToys PowerRename](https://learn.microsoft.com/en-us/windows/powertoys/powerrename)、[VS Code · Basic Editing](https://code.visualstudio.com/docs/editing/codebasics)：批量重命名与替换前预览新旧差异。
- [VS Code · User interface](https://code.visualstudio.com/docs/editing/getting-started/userinterface)：预览标签与常驻标签。
- [Krita · Tablet Settings](https://docs.krita.org/en/reference_manual/preferences/tablet_settings.html)：压感输入与鼠标事件的区分。
- [GNOME HIG · Text fields](https://developer.gnome.org/hig/patterns/controls/text-fields.html)、[KDE HIG · Getting input](https://develop.kde.org/hig/getting_input/)、[Apple HIG · Entering data](https://developer.apple.com/design/human-interface-guidelines/entering-data)：输入约束、就地纠错，以及精确数值的直接输入。
- [W3C · Understanding Accessible Authentication (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/accessible-authentication-minimum.html)：认证流程接受粘贴和凭据管理器。
- [GNOME · Evolution 拼写检查](https://teams.pages.gitlab.gnome.org/Websites/help.gnome.org/evolution/mail-composer-spellcheck.html)：按语言选择词典。

## WINDOW · 窗口

- [Qt · QWindow](https://doc.qt.io/qt-6/qwindow.html)：Wayland 等平台不允许应用设置窗口位置。
- [Apple · applicationShouldTerminateAfterLastWindowClosed](https://developer.apple.com/documentation/appkit/nsapplicationdelegate/applicationshouldterminateafterlastwindowclosed(_:))：最后一个窗口关闭后是否退出。
- [Microsoft · Win32 UX Guide · Window Management](https://learn.microsoft.com/en-us/windows/win32/uxguide/win-window-mgt)、[GNOME HIG · Windows](https://developer.gnome.org/hig/patterns/containers/windows.html)、[Apple HIG · Modality](https://developer.apple.com/design/human-interface-guidelines/modality)：主窗口与从属窗口的关系、文档级模态。
- [Microsoft · Kernel object namespaces](https://learn.microsoft.com/en-us/windows/win32/termserv/kernel-object-namespaces)、[Apple · LSMultipleInstancesProhibited](https://developer.apple.com/documentation/bundleresources/information-property-list/lsmultipleinstancesprohibited)：单实例在多用户会话中的范围。
- [Microsoft · Navigation history and backwards navigation](https://learn.microsoft.com/en-us/windows/uwp/layout/navigation-history-and-backwards-navigation)、[JetBrains · Recent files and locations](https://www.jetbrains.com/help/idea/recent-files-and-changes.html)：按访问路径后退与前进。
- [Sublime Text · 更新日志](https://www.sublimetext.com/download)：外部启动请求在加载完成后执行；文件在磁盘上变化后不恢复旧的撤销历史；恢复未保存文件时保留编码。

## APPEARANCE · 外观

- [W3C APG · Window Splitter](https://www.w3.org/WAI/ARIA/apg/patterns/windowsplitter/)：分隔条的键盘操作与折叠后的恢复。
- [Microsoft · Win32 UX Guide · List Views](https://learn.microsoft.com/en-us/windows/win32/uxguide/ctrl-list-views)、[Semi Design · 表格](https://semi.design/design/zh-CN/show/table)：列选择、列宽调整、固定表头与固定列。
- [VS Code · Modernizing the VS Code UI](https://code.visualstudio.com/blogs/2026/10/15/modern-ui)：改版后增加布局密度设置，并在过渡期保留经典界面。

## SETTINGS · 设置

- [Qt · QSettings](https://doc.qt.io/qt-6/qsettings.html)、[QStandardPaths](https://doc.qt.io/qt-6/qstandardpaths.html)：配置的原生存储位置。
- [VS Code · Settings Sync](https://code.visualstudio.com/docs/configure/settings-sync)、[Profiles](https://code.visualstudio.com/docs/configure/profiles)：机器相关设置不随同步覆盖，快捷键按平台同步。
- [GNOME HIG · Switches](https://developer.gnome.org/hig/patterns/controls/switches.html)：开关显示功能是否已实际生效。
- [Microsoft · Win32 UX Guide · Confirmations](https://learn.microsoft.com/en-us/windows/win32/uxguide/mess-confirm)："不再显示"的适用范围；不为用户没做过的修改询问保存。

## LOCALE · 语言与地区

- [Microsoft · Handling a new era in the Japanese calendar in .NET](https://devblogs.microsoft.com/dotnet/handling-a-new-era-in-the-japanese-calendar-in-net/)：日本改元时的纪年处理。

## DATA · 数据保护、保存与恢复

- [Microsoft · ReplaceFileW](https://learn.microsoft.com/en-us/windows/win32/api/winbase/nf-winbase-replacefilew)、[MoveFileExW](https://learn.microsoft.com/en-us/windows/win32/api/winbase/nf-winbase-movefileexw)：替换保存时保留属性与访问控制，写穿缓存。
- [SQLite · Atomic Commit](https://sqlite.org/atomiccommit.html)、[Online Backup API](https://www.sqlite.org/backup.html)、[Write-Ahead Logging](https://www.sqlite.org/wal.html)：原子提交、运行中数据库的一致备份、WAL 文件属于数据库状态。
- [Apple HIG · File management](https://developer.apple.com/design/human-interface-guidelines/file-management)：自动保存、版本浏览与未保存标记。
- [Apple HIG · Undo and redo](https://developer.apple.com/design/human-interface-guidelines/undo-and-redo)：撤销项写明动作、撤销结果可见。
- [Syncthing · Understanding Synchronization](https://docs.syncthing.net/users/syncing.html)：文件监听会遗漏事件，需要定期扫描；大小写冲突。
- [Obsidian · Back up your files](https://obsidian.md/help/backup)、[Troubleshoot Obsidian Sync](https://obsidian.md/help/sync/troubleshoot)：同步不是备份；不同文件类型的冲突处理。
- [GIMP · Export File](https://docs.gimp.org/3.0/en/gimp-export-dialog.html)、[LibreOffice Calc · Importing and Exporting CSV](https://help.libreoffice.org/latest/en-US/text/scalc/guide/csv_formula.html)、[1Password · Export your data](https://support.1password.com/export/)：完整工程与交换格式的区别，导出范围的说明。
- [Zotero · Data directory in cloud storage](https://www.zotero.org/support/kb/data_directory_in_cloud_storage_folder)：数据库放在同步盘中的损坏风险。
- [Zotero · Why can't Zotero find a linked file?](https://www.zotero.org/support/kb/missing_linked_file)、[Typora · Images](https://support.typora.io/Images/)：外部资源的重新定位，应用内移动资源时更新引用。
- [Slack · Send and read messages](https://slack.com/help/articles/201457107-Send-and-read-messages)、[Telegram · Drafts](https://telegram.org/blog/drafts)：草稿与定时消息的集中入口，会话列表中的草稿标记。

## FILE · 文件与资源

- [Apple · Accessing files from the macOS App Sandbox](https://developer.apple.com/documentation/security/accessing-files-from-the-macos-app-sandbox)：沙箱下的持久授权与安全作用域书签。
- [Microsoft · Build a Cloud Sync Engine that Supports Placeholder Files](https://learn.microsoft.com/en-us/windows/win32/cfapi/build-a-cloud-file-sync-engine)：仅联机的占位文件。
- [KDE HIG · Simple by default](https://develop.kde.org/hig/simple_by_default/)：不经打开对话框的文件同样进入最近文件；撤销提示期间推迟不可逆删除。

## TASK · 任务、响应与资源

- [Microsoft · Win32 UX Guide · Progress Bars](https://learn.microsoft.com/en-us/windows/win32/uxguide/progress-bars)、[GNOME HIG · Progress bars](https://developer.gnome.org/hig/patterns/feedback/progress-bars.html)：总进度、剩余时间、取消与停止的区别。
- [JetBrains · Experimental zero-latency typing](https://blog.jetbrains.com/idea/2015/08/experimental-zero-latency-typing-in-intellij-idea-15-eap/)：输入到显示的延迟。
- [Microsoft Edge · Performance features](https://support.microsoft.com/en-us/edge/learn-about-performance-features-in-microsoft-edge)：后台节流对播放和采集等活动的例外。
- [OBS · Hybrid MP4 / MOV](https://obsproject.com/kb/hybrid-mp4)：录制中断后主体内容与附属信息的可恢复范围。
- [VS Code · 1.102 更新说明](https://code.visualstudio.com/updates/v1_102)：窗口失焦且需要确认时在 Dock 显示徽标。

## NETWORK · 网络、离线与同步

- [RFC 8252 · OAuth 2.0 for Native Apps](https://www.rfc-editor.org/rfc/rfc8252.html)：通过系统浏览器登录并返回应用。
- [Electron · Security](https://www.electronjs.org/docs/latest/tutorial/security)：安全传输与证书验证。
- [Apple · App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)：2.5.5 要求在 IPv6-only 网络中正常工作。

## SYSTEM · 系统集成

- [XDG Desktop Portal](https://flatpak.github.io/xdg-desktop-portal/docs/)：[Background](https://flatpak.github.io/xdg-desktop-portal/docs/doc-org.freedesktop.portal.Background.html)、[Global Shortcuts](https://flatpak.github.io/xdg-desktop-portal/docs/doc-org.freedesktop.portal.GlobalShortcuts.html)，沙箱中的登录启动与全局快捷键。
- [Microsoft · Win32 UX Guide · Notifications](https://learn.microsoft.com/en-us/windows/win32/uxguide/mess-notif)、[GNOME HIG · Notifications](https://developer.gnome.org/hig/patterns/feedback/notifications.html)：通知的撤回、前台行为与重提节奏。
- [Slack · Troubleshoot Slack notifications](https://slack.com/help/articles/360001559367-Troubleshoot-Slack-notifications)：已读会话仍显示徽标的失步情况。
- [Microsoft · WM_QUERYENDSESSION](https://learn.microsoft.com/en-us/windows/win32/shutdown/wm-queryendsession)、[ShutdownBlockReasonCreate](https://learn.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-shutdownblockreasoncreate)、[RegisterApplicationRestart](https://learn.microsoft.com/en-us/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)：关机前保存、说明阻止原因、系统更新后自动重启。

## INSTALL · 安装、更新与卸载

- [Homebrew · Cask Cookbook](https://docs.brew.sh/Cask-Cookbook)：`auto_updates` 声明与 `zap` 清理范围。
- [VS Code · Portable mode](https://code.visualstudio.com/docs/setup/portable)：便携分发与自动更新的关系。
- [Mozilla · Install an older version of Firefox](https://support.mozilla.org/en-US/kb/install-older-version-firefox)：降级保护与配置数据。
- [Microsoft · SmartScreen reputation and code signing](https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/smartscreen-reputation)：已签名的新版本在积累信誉前仍可能触发警告。
- [Microsoft · WebView2 distribution](https://learn.microsoft.com/microsoft-edge/webview2/concepts/distribution)：运行时依赖的分发方式。
- [Tauri · Updater](https://v2.tauri.app/plugin/updater/)、[Sparkle · Documentation](https://sparkle-project.org/documentation/)：更新包签名与内置公钥。
- [NIST NVD · CVE-2024-39698](https://nvd.nist.gov/vuln/detail/CVE-2024-39698)：electron-updater 的签名校验可被绕过。
- [NIST NVD · CVE-2026-95625](https://nvd.nist.gov/vuln/detail/CVE-2026-95625)：Tauri updater 2.12.0 之前的版本清单未签名，可被诱导降级。
- [1Password · Windows 发布说明](https://releases.1password.com/windows/stable/)：退出时安装更新不自行重启；静默更新后不跳到前台；副窗口在活动显示器打开。

## PRIVACY · 权限、账号与隐私

- [Electron · safeStorage](https://www.electronjs.org/docs/latest/api/safe-storage)：Linux 上的凭据保护取决于 secret store 后端。
- [RFC 9110 · Redirection](https://www.rfc-editor.org/rfc/rfc9110.html#section-15.4)：重定向时的凭据作用范围。
- [KeePass · FAQ](https://keepass.info/help/kb/faq.html)：只清除应用自己写入剪贴板的内容。
- [1Password · Auto-lock](https://support.1password.com/auto-lock/)：应用锁与空闲判断。
- [RFC 6455 · WebSocket Origin Considerations](https://www.rfc-editor.org/rfc/rfc6455.html#section-10.2)、[Microsoft · Named Pipe Security and Access Rights](https://learn.microsoft.com/en-us/windows/win32/ipc/named-pipe-security-and-access-rights)：本机服务与进程通信的访问边界。

## HELP · 帮助、反馈与诊断

- [Microsoft · Win32 UX Guide · Error Messages](https://learn.microsoft.com/en-us/windows/win32/uxguide/mess-error)、[Fluent 2 · Tooltip](https://fluent2.microsoft.design/components/web/react/core/tooltip/usage)：错误的呈现方式，说明控件不可用的原因与条件。
- [LibreOffice · Troubleshoot Mode](https://help.libreoffice.org/latest/en-US/text/shared/01/profile_safe_mode.html)、[VS Code · Resolving extension issues with bisect](https://code.visualstudio.com/blogs/2021/02/16/extension-bisect)：安全模式与扩展二分排查。

## FIND · 搜索与筛选

- [JetBrains · Search Everywhere](https://www.jetbrains.com/help/idea/searching-everywhere.html)、[Obsidian · Search](https://obsidian.md/help/plugins/search)：搜索范围、排除条件与查询说明。
- [Obsidian · 1.8.2 更新说明](https://obsidian.md/changelog/2025-01-22-desktop-v1.8.2/)：在文件列表中自动显示当前文件的位置。
- [Obsidian · Bookmarks](https://obsidian.md/help/plugins/bookmarks)、[サクラエディタ · ブックマーク](https://sakura-editor.github.io/help/HLP000205.html)：对象与行的个人标记。

## TRUST · 外来内容

- [Microsoft 365 · What is Protected View?](https://support.microsoft.com/en-us/office/collab-files/what-is-protected-view)、[VS Code · Workspace Trust](https://code.visualstudio.com/docs/editing/workspaces/workspace-trust)、[LibreOffice · Macro Security](https://help.libreoffice.org/latest/en-GB/text/shared/optionen/macrosecurity.html)：受限模式查看与放行范围。
- [Mozilla · Remote Content in Messages](https://support.mozilla.org/en-US/kb/remote-content-in-messages)、[Thunderbird's Scam Detection](https://support.mozilla.org/en-US/kb/thunderbirds-scam-detection)：外来内容的网络请求与链接目标核验。
- [MITRE · CWE-22 Path Traversal](https://cwe.mitre.org/data/definitions/22.html)：归档导入越界写入。
- [Microsoft · IAttachmentExecute::Save](https://learn.microsoft.com/en-us/windows/win32/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-save)：保存下载内容时附加来源标记。

## EXTEND · 扩展与插件

- [Obsidian · Plugin security](https://obsidian.md/help/plugin-security)、[VS Code · Extension runtime security](https://code.visualstudio.com/docs/configure/extensions/extension-runtime-security)、[Extension Marketplace](https://code.visualstudio.com/docs/configure/extensions/extension-marketplace)：扩展的实际权限、发布者信任与停用管理。
- [VS Code · 1.92 更新说明](https://code.visualstudio.com/updates/v1_92)：扩展更新后包含可执行代码时重新征求同意；手动安装的扩展默认不自动更新。

## AUTOMATE · 外部自动化

- [LibreOffice · Starting the software with parameters](https://help.libreoffice.org/latest/en-US/text/shared/guide/start_parameters.html)、[Apple · Run shortcuts from the command line](https://support.apple.com/guide/shortcuts-mac/run-shortcuts-from-the-command-line-apd455c82f02/mac)：命令行入口、退出码与无界面执行。
- [Microsoft · UI Automation Control Patterns](https://learn.microsoft.com/en-us/windows/win32/winauto/uiauto-controlpatternsoverview)、[Use the AutomationId Property](https://learn.microsoft.com/en-us/dotnet/framework/ui-automation/use-the-automationid-property)：可驱动界面中的对象标识与操作。
- [Sketch · MCP server](https://www.sketch.com/docs/mcp-server/)、[1Password · CLI app integration](https://developer.1password.com/docs/cli/app-integration/)：由用户开启、可撤销的委托接口。

## LICENSE · 许可、试用与到期

- [1Password · Frozen account](https://support.1password.com/frozen-account/)、[JetBrains · Offline use and activation](https://sales.jetbrains.com/hc/en-gb/articles/206544169-Do-I-need-and-internet-connection-to-activate-and-use-JetBrains-products)、[Sketch · Move a license to another device](https://www.sketch.com/support/mac-only-licenses/move-to-another-device/)、[Obsidian · License](https://obsidian.md/license)：到期后取回工作、离线验证与设备迁移。

## MANAGED · 组织部署与受管环境

- [VS Code · Enterprise](https://code.visualstudio.com/docs/enterprise/overview)：[更新管理](https://code.visualstudio.com/docs/enterprise/updates)与[扩展管理](https://code.visualstudio.com/docs/enterprise/extensions)。
- [Microsoft · Create an offline installation of Visual Studio](https://learn.microsoft.com/en-us/visualstudio/install/create-an-offline-installation-of-visual-studio)、[JetBrains · IntelliJ IDEA installation guide](https://www.jetbrains.com/help/idea/installation-guide.html)：离线布局、静默安装与安装范围。

## FAIR · 尊重用户选择

- [Microsoft · How Microsoft identifies malware and potentially unwanted applications](https://learn.microsoft.com/en-us/defender-xdr/criteria)：捆绑、误导与默认选项。
- [1Password · Manage your subscription](https://support.1password.com/manage-subscription/)：取消订阅的入口与不同购买渠道。
- [Apple · App Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)：5.1.1(v) 账号删除。
- [VS Code · 1.96 更新说明](https://code.visualstudio.com/updates/v1_96)：用户卸载的预装扩展重启后不再重装。

## COMPONENT · 随附组件与辅助进程

- [FFmpeg · License and Legal Considerations](https://www.ffmpeg.org/legal.html)：随附组件的许可说明与源码获取。
- [Microsoft · IAudioSessionControl::SetDisplayName](https://learn.microsoft.com/en-us/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setdisplayname)：辅助进程在音量合成器中的显示名称。

## MEDIA · 播放与采集

- [Microsoft · System Media Transport Controls](https://learn.microsoft.com/en-us/windows/apps/develop/media-playback/integrate-with-systemmediatransportcontrols)、[freedesktop · MPRIS](https://specifications.freedesktop.org/mpris/latest/)、[Apple HIG · Playing audio](https://developer.apple.com/design/human-interface-guidelines/playing-audio)：系统媒体控制。
- [Microsoft · User-Mode Audio Components](https://learn.microsoft.com/en-us/windows/win32/coreaudio/user-mode-audio-components)：共享与独占访问对其他应用的影响。
- [Apple · Capturing screen content in macOS](https://developer.apple.com/documentation/screencapturekit/capturing-screen-content-in-macos)：窗口、应用与显示器的采集范围。

## TRANSFER · 传输结果的交付

- [aria2 · 手册](https://aria2.github.io/manual/en/html/aria2c.html)：完整性校验、续传与 RPC 访问控制。

## 附录 A 的技术栈文档

- **Microsoft**：[Job Objects](https://learn.microsoft.com/en-us/windows/win32/procthread/job-objects)（`JOB_OBJECT_LIMIT_KILL_ON_JOB_CLOSE`）。
- **Linux**：[prctl(2)](https://man7.org/linux/man-pages/man2/prctl.2.html)（`PR_SET_PDEATHSIG`）。
- **Electron**：[net](https://www.electronjs.org/docs/latest/api/net/)、[globalShortcut](https://www.electronjs.org/docs/latest/api/global-shortcut)、[BrowserWindow](https://www.electronjs.org/docs/latest/api/browser-window)。
- **Tauri**：[Security](https://v2.tauri.app/security/)、[Capabilities](https://v2.tauri.app/security/capabilities/)。
- **Qt**：[QSaveFile](https://doc.qt.io/qt-6/qsavefile.html)、[QFileSystemWatcher](https://doc.qt.io/qt-6/qfilesystemwatcher.html)。
