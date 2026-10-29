# 旁注

[English](../side-notes.md) | 简体中文

本文收录与 [checklist.md](checklist.md) 相关、但不作为条目的内容：清单范围之外的相关主题、体现清单条目的产品实例，以及同类清单。条目所依据的来源见 [references.md](references.md)。本文不参与审查，[AUDIT.md](AUDIT.md) 不要求 Agent 逐项核对。

## 范围之外的相关主题

下列主题与清单相关，但不作为条目。每项说明原因。

- **平台视觉规范**（间距、圆角、配色、图标尺寸）：属于把已知需求做对，清单不做 HIG 符合性对照。
- **Windows 访问键的分配细则、macOS 的 Services 菜单与浮动面板、GNOME 的手势保留**：平台惯例，按对应规范实现即可。自绘界面容易缺失访问键，可参考 INPUT-03 快捷键可发现。
- **应用内剪贴板历史**：证据集中在代码与文本编辑器，且需与 PRIVACY-07 敏感内容的显示与复制的剪贴板保护一同设计。
- **列表与详情并排查看**：属于布局取舍，由产品按任务决定。
- **按住修饰键临时切换工具**：限于画布、绘图与设计类产品。
- **多设备时通知跟随正在使用的设备**：限于即时通信类产品。
- **组织外部参与者的标识**：限于协作与通信产品。
- **会过期的待取内容显示剩余期限**：目前只有聊天产品的实例。
- **商店页面与应用描述的准确性**：属于分发渠道运营。
- **地区限制与年龄分级**：属于法务与运营。
- **媒体播放器的多音轨与字幕轨切换**：属于特定产品功能。
- **设计流程自查表**（腾讯 CDC 交互自查表等）：检查设计流程是否完整，不检查产品能力。
- **LLM 前端特有的生成控制**（结果不满意时自动重新生成、按长度自动续写、逐字显示的节奏）：限于 LLM 前端这一类产品，其他类型的桌面应用中未见同类功能。通用部分已由 TASK-05 失败重试与幂等、TASK-10 流式输出的视口行为覆盖。

## 产品范例

下列产品行为对应清单中的条目，可用来向团队说明条目的含义。

- **Slack**：侧栏"草稿和已发送"集中列出草稿、定时消息和已发送消息。对应 DATA-14 离开后可发现未完成的工作；TASK-06 后台任务入口。
- **Telegram Desktop**：草稿显示在会话列表中并跨设备同步。对应 DATA-14 离开后可发现未完成的工作。
- **微信、QQ**：会话列表中未发送的内容显示为"[草稿]"；撤回的消息可重新编辑。对应 DATA-14 离开后可发现未完成的工作；TASK-03 停止等待、取消任务与撤回结果。
- **Telegram Desktop**：只在活动窗口中把消息标为已读，锁屏期间不标已读。对应 SYSTEM-14 未读与待处理状态如实。
- **Sublime Text**：新建且未修改的文件不显示未保存标记；文件在磁盘上变化后不恢复旧的撤销历史；恢复未保存文件时保留编码。对应 DATA-01 保存状态可见；WINDOW-06 工作区与视图上下文恢复；DATA-02 自动保存与崩溃恢复。
- **VS Code**：单击打开预览标签，编辑或双击后才固定；改版后加入布局密度设置，并在过渡期保留回到经典界面的选项。对应 INPUT-17 浏览与激活分离；APPEARANCE-04 布局密度；HELP-08 更新内容说明。
- **VS Code**：窗口失焦且需要用户确认时在 Dock 显示徽标，窗口获得焦点后消失。对应 TASK-06 后台任务入口。
- **GitHub Copilot 应用**：内容重排时按对象身份锚定阅读位置，打开文件树侧栏不使正在阅读的文件漂走。对应 DISPLAY-08 无闪烁、无跳动、操作目标稳定。
- **1Password**：副窗口在活动显示器上打开；有可用更新时退出不再自行重启。对应 WINDOW-12 从属窗口的位置与层级；INSTALL-03 更新偏好。
- **Telegram Desktop**：因与输入法冲突，默认移除了 Ctrl+Shift+数字快捷键；锁定时隐藏任务栏窗口预览。对应 INPUT-04 快捷键可自定义；PRIVACY-13 应用锁的保护范围。
- **Obsidian**：键盘删除书签后焦点移到下一项；快速切换器中按 Esc 恢复之前的选择；文件列表可自动显示当前文件的位置。对应 A11Y-02 焦点可见、顺序合理、关闭后焦点返回；INPUT-17 浏览与激活分离；FIND-02 命中可辨认、结果可遍历。
- **Obsidian、サクラエディタ、飞书**：书签、行书签与消息标记。对应 FIND-05 个人标记与稍后处理。
- **Typora**：在应用内移动图片时更新 Markdown 中的引用。对应 DATA-11 外部资源重新定位。
- **新版 Outlook**："撤消发送"把投递延迟最多 30 秒。对应 INPUT-14 以撤销代替确认。
- **Figma**：多选对象的属性取值不一致时显示混合值。对应 INPUT-11 多选与批量操作。
- **VS Code、JetBrains IDE**：分栏或终端失去焦点时变暗或换背景，用户不必试打一个字就能知道输入会落到哪个窗格。对应 A11Y-02 焦点可见、顺序合理、关闭后焦点返回。
- **飞书**：与内嵌应用或网站的快捷键冲突时，可选择内嵌内容优先、飞书优先或两者先后响应；不支持修改的快捷键在详情页有提示。对应 INPUT-04 快捷键可自定义。
- **Clibor、秀丸エディタ、Quicker**：Clibor 的剪贴板监视可延迟入库并忽略短时间内的重复更新，避免记下"正在获取数据"占位文本；秀丸エディタ与其他剪贴板工具冲突时可切换监视方式；Quicker 的常见问题列出会引起卡顿的剪贴板监视软件。对应 INPUT-10 剪贴板格式与生命周期。
- **Figma、飞书、Telegram Desktop**：从标签菜单或 Ctrl + Shift + T 重新打开最近关闭的标签或窗口，连续按下按关闭顺序恢复。对应 INPUT-14 以撤销代替确认；FILE-02 最近文件。
- **VS Code、Firefox**：标签可换行显示、固定标签单独占一行，新标签打开在当前标签旁还是末尾可设置。对应 WINDOW-06 工作区与视图上下文恢复。
- **mpv、IrfanView**：打开尺寸不同的下一个对象时，窗口是否随内容改变尺寸和位置可选；IrfanView 可让指针保持在"上一个 / 下一个"工具栏按钮上。对应 WINDOW-01 位置与尺寸恢复。
- **Raycast、Alfred**：唤起时自动切换到指定的输入源，关闭后还原。对应 WINDOW-10 快速唤起与焦点归还。
- **ShareX、Snipaste**：贴图可一次全部关闭或按组关闭，新贴图的默认位置可选边角或居中，可切换鼠标穿透并一键解除全部穿透。对应 WINDOW-09 窗口置顶。
- **Obsidian、秀丸エディタ**：当前打开的文件、面板和布局可保存为命名的工作区并一键加载。对应 APPEARANCE-05 面板可调整、可复位。
- **VS Code、Notepad++、JetBrains IDE**：菜单栏隐藏后，VS Code 与 Notepad++ 在 Windows / Linux 上按 Alt 或 F10 可临时显示；JetBrains IDE 可把主菜单收进汉堡按钮。对应 APPEARANCE-05 面板可调整、可复位。
- **Telegram Desktop、Discord、Alfred**：主题应用前可预览；Telegram Desktop 应用后倒计时内未确认保留则自动回到原主题。对应 APPEARANCE-06 自定义配色的安全性。
- **Alfred、Everything、Listary、Snipaste**：排障文档各自说明设置不保存的原因：Alfred 列出权限问题和 Dropbox 冲突文件；Everything 需启用"把设置和数据存放在 %APPDATA%"；Listary 提供从托盘"安全退出"以强制保存；Snipaste 说明程序目录下的 config.ini 不可写时配置会回到默认。对应 SETTINGS-04 持久化可靠、手动编辑容错。
- **mpv、サクラエディタ、秀丸エディタ**：按扩展名、协议或文件类型自动套用一组单独的设置。对应 SETTINGS-05 作用域明确。
- **Telegram Desktop、Zoom、SillyTavern、Blender**：下载位置、连接会议室、导入时的标签处理和保存时对未保存图像的处理，都作为设置项提供"每次询问 / 总是 / 从不"三档。对应 SETTINGS-07 按类别重置。
- **Typora**：文件列表按自然顺序排序，名称中的数字按数值比较。对应 LOCALE-05 多语言文本处理。
- **秀丸エディタ**：切换窗口时立即自动保存一次。对应 DATA-02 自动保存与崩溃恢复。
- **Blender、Krita、Affinity Photo**：撤销步数或撤销内存上限可设置；Blender 说明关闭全局撤销会连带禁用"调整上一步操作"。对应 DATA-04 撤销与重做的作用对象。
- **Obsidian、VS Code**：历史快照可显示与当前版本的差异，可只复制旧内容而不整体恢复。对应 DATA-05 历史版本与备份。
- **Blender、Krita、LibreOffice**：覆盖保存时保留上一版本副本（`.blend1`、`~`、`.BAK`）；Krita 可选存放在同目录、用户目录或临时目录，并警告临时目录会被清空；LibreOffice 在同目录不可写时改存备份目录；Blender 说明临时目录中的自动保存文件可能在重启或磁盘清理后消失。对应 DATA-05 历史版本与备份。
- **JetBrains IDE、VS Code**：文件监听超出系统限制时提示并回退为扫描目录；可排除不需要监听的目录。对应 DATA-07 外部变化与冲突。
- **Obsidian、Typora**：Obsidian 的每台设备有用户可改的名称，同步日志和冲突副本的文件名用它标识；Typora 的许可页面列出已激活设备并可远程停用。对应 DATA-07 外部变化与冲突；LICENSE-04 更换设备与设备丢失。
- **Firefox、Audacity**：Firefox 可设置只为查看而打开的文件存放在临时目录而不是下载目录；Audacity 选择临时目录时显示可用空间，不接受 FAT 卷并劝阻网络盘与 U 盘。对应 DATA-09 数据位置透明、可迁移。
- **Firefox**：崩溃后的"恢复会话"页列出上次的窗口和标签，可勾选恢复哪些；再次崩溃时可选择开始新会话。对应 DATA-14 离开后可发现未完成的工作。
- **Audacity、Blender、LibreOffice、Notepad++、IrfanView**：打开、保存、导入、导出或字体、纹理、渲染输出等不同用途各自记住目录或指定固定目录，留空则沿用上次位置；Notepad++ 可选跟随当前文档，取消对话框不更新上次目录；IrfanView 的幻灯片和批处理对话框可选在上次目录还是当前目录打开；Blender 的临时目录不存在时改用系统临时目录。对应 FILE-01 平台文件对话框与持久授权。
- **Typora、Notepad++**：常用文件夹可固定在最近列表中不被淘汰，清除时可选是否连固定项一起清除；网络盘上暂时不可达的文件可不在启动时移出最近列表。对应 FILE-02 最近文件。
- **Listary、Everything**：可指定用第三方文件管理器及其参数打开所在文件夹；Listary 的常见问题说明"找不到应用程序"来自其他文件管理器接管了文件夹关联。对应 FILE-06 在系统中定位。
- **JetBrains IDE**：关闭仍有进程运行的工具窗口时，可选择终止进程、断开连接或每次询问。对应 TASK-06 后台任务入口。
- **Krita**：FAQ 说明系统启动后接入显示器或数位板导致的偏移如何校正。对应 TASK-09 睡眠唤醒、网络与设备变化。
- **Obsidian、Zotero**：同步日志可按"冲突"筛选并列出被跳过的文件及原因；Zotero 在同步错误图标上显示状态和报告 ID。对应 NETWORK-04 待同步队列可见。
- **Telegram Desktop**：内置传输连接失败时说明正在后台重试，并提供在浏览器中打开的替代。对应 NETWORK-02 超时与重连。
- **Telegram Desktop、企业微信、Discord、Steam**：Telegram Desktop 与 Discord 的自动下载可按内容类型、来源和大小上限分别设置并有例外名单；企业微信的机密文件不自动下载；Steam 可限定自动更新的时段，并按游戏设置玩游戏时是否允许下载其他更新。对应 NETWORK-06 流量控制。
- **Slack、Telegram Desktop**：通知设置中可发送一条示例通知；Telegram Desktop 检测到 Windows 设置中关闭了随系统启动时说明原因，并提供打开系统设置的入口。对应 SYSTEM-03 系统通知与注意力。
- **Zoom、飞书**：快捷键列表中每一项可单独勾选为全局生效。对应 SYSTEM-04 全局快捷键。
- **CLaunch、Alfred、Snipaste、PowerToys**：CLaunch 在托盘隐藏且全部功能禁用前警告将无法再显示，再次运行程序可强制显示；Alfred 与 Snipaste 的文档说明隐藏菜单栏图标或托盘图标后如何打开设置；PowerToys Keyboard Manager 的 FAQ 说明改错键后如何停止映射，并警告会失去对应的按键。对应 SYSTEM-11 系统能力不可用时的替代入口。
- **OBS Studio、Audacity**：应用内集中列出所需的屏幕录制、摄像头、麦克风和辅助功能权限及用途，并给出各平台的授权步骤。对应 PRIVACY-02 权限撤销后的处理。
- **Ditto、Alfred、Clibor**：Ditto 遵循 Windows 的剪贴板排除标记，带标记的内容不存入历史，并可按正则和进程名排除；Alfred 的剪贴板历史默认关闭，默认忽略钥匙串访问、1Password 等应用；Clibor 可在启动时停止监视、退出时删除历史并加密保存的数据。对应 PRIVACY-10 剪贴板读取的时机与用途。
- **Telegram Desktop、Syncthing**：Telegram Desktop 的应用锁可用 Windows Hello 或系统密码解锁，首次仍需输入应用密码，并说明设了密码后无法最小化启动；Syncthing 的 FAQ 说明忘记界面密码时的重置办法。对应 PRIVACY-13 应用锁的保护范围。
- **VS Code、Notepad++**：打开查找时用选中文本填充查询框，超过长度阈值的选区不填入，大段选区自动启用"在选区内查找"。对应 FIND-04 重复检索；FIND-01 范围与排除条件可见。
- **Bandizip、7-Zip**：解压带来源标记的压缩包时，产出的文件同样带上标记。对应 TRUST-06 下载内容的来源标记交接。
- **Thunderbird、foobar2000**：Thunderbird 可在更新会禁用附加组件时先警告；foobar2000 的 FAQ 列出拒绝加载组件时的每种错误信息及处理。对应 EXTEND-03 更新可控。
- **VS Code、JetBrains IDE**：从图标启动时读取登录 shell 的环境以找到终端里可用的工具，读取超时或失败时提示原因。对应 COMPONENT-01 随附组件与系统副本共存。
- **Slack**：组织下发的设置分"默认值"（用户仍可改）与"强制值"（锁定）两档。对应 MANAGED-03 策略控制可见。
- **Zoom**：共享桌面期间静音系统通知，共享画面中是否包含本应用的工具栏和会议通知可选。对应 MEDIA-05 屏幕采集范围确认。
- **Zoom**：会议中计算机锁屏或屏保启动时自动停止音频和视频。对应 MEDIA-04 实际采集状态与停止入口。

## 同类清单

下列清单与本清单部分重叠，可用作对应平台或领域的补充。在已核查的中、英、日、韩公开来源中，没有找到同时覆盖跨平台桌面能力、数据与任务交接和隐性 QoL 的通用清单。

| 清单 | 范围 | 与本清单的差异 |
| --- | --- | --- |
| [Microsoft UX checklist for desktop applications](https://learn.microsoft.com/en-us/windows/win32/uxguide/top-violations) | Windows 桌面界面 | 偏控件与平台一致性，不含数据保护、恢复、输入法、安装与隐私 |
| [Google Adaptive app quality · Desktop](https://developer.android.com/docs/quality-guidelines/adaptive-app-quality/experiences/desktop) | Android 应用在桌面上的表现 | 按层级编号、附测试方法；约 30 条，只针对 Android |
| [HarmonyOS 应用 UX 体验标准](https://developer.huawei.com/consumer/cn/doc/doccenter-ux-design/ux-guidelines-overview-0000001760867048) | 鸿蒙通用、大屏与电脑应用 | 键鼠与窗口细致，数据与生命周期类能力较少 |
| [デジタル庁 UI チェックリスト](https://www.digital.go.jp/resources/standard_guidelines) | 政府网页与服务 | 输入与表单行为具体，不含桌面窗口、托盘、安装与文件交接 |
| [KRDS](https://www.krds.go.kr/html/site/outline/outline_04.html) | 韩国数字政府服务 | 按必需、推荐、优秀分级，主体是政府服务 |
| [Vercel web-interface-guidelines](https://github.com/vercel-labs/web-interface-guidelines) | Web 界面 QoL | 附 Agent 说明文件，形式与本清单接近，只针对 Web |
| [Front-End-Checklist](https://github.com/thedaviddias/Front-End-Checklist) | Web 前端发布前检查 | 附 MCP server，只针对 Web |
| [mac-arsed-mac-app](https://github.com/bartreardon/skills/blob/main/mac-arsed-mac-app/SKILL.md) | macOS 原生惯例 | 写给 AI Agent 的技能文件，约 30 个要点，只针对 macOS |
| [SmartHR UIデザイン使用性チェックリスト](https://smarthr.design/products/usability/usability-checklist/) | SaaS Web 设计评审 | 对应 JIS X 25010，22 项 |
| [checklist.design](https://www.checklist.design/) | 页面、组件与流程 | 回答"这一页该有什么"，没有桌面类别 |
| [支付宝体验设计走查表](https://developer.aliyun.com/article/82295) | 移动产品 | 按场景因素和异常分支组织，社区转载 |
