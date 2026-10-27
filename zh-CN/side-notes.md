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
