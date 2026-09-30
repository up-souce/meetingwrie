# meetingwrie

面向 Codex 的中文会议纪要编写 skill。它将会议转写稿、笔记、议程或经转写的录音材料整理为结构化纪要，并明确区分：已经确认的事实、仍在讨论的建议，以及材料无法核实的内容。

> 仓库名为 `meetingwrie`。skill 的调用名保持为 `$meeting-minutes-writing`，以便按功能被准确发现。

## 特性

- 以材料证据为准，不补写姓名、日期、数字、责任人或期限。
- 将明确决议与讨论建议分开记录，避免把提议写成结论。
- 对缺失、听不清或相互矛盾的信息保留“待确认”标记。
- 默认输出会议基本信息、讨论内容、决议、行动项、待确认事项与风险。
- 包含一份可按需加载的 Markdown 输出模板。

## 安装

将仓库克隆到 Codex 的 skills 目录，并将本地目录命名为 skill 标识：

```powershell
git clone https://github.com/up-souce/meetingwrie.git "$env:USERPROFILE\.codex\skills\meeting-minutes-writing"
```

也可以下载 Release 压缩包并解压；请将解压后的目录命名为 `meeting-minutes-writing` 后再放入 `%USERPROFILE%\.codex\skills\`。重启或刷新 Codex 后生效。

## 使用

```text
使用 $meeting-minutes-writing，根据以下转写稿编写正式会议纪要：……
```

如果用户提供录音而没有转写稿，skill 会要求先取得可用的转写文本；它不会声称已经听取未处理的音频。

## 文件结构

```text
.
├── SKILL.md                       # 主指令
├── agents/openai.yaml             # Codex 界面元数据
└── references/output-template.md  # 默认纪要模板
```

## 适用边界

本 skill 用于生成纪要，不用于生成逐字稿或替代人工核验。姓名、数字、承诺、日期和决议会影响真实业务时，应回看原始录音或权威材料确认。

请勿将会议录音、转写稿、参会人信息、客户资料或其他敏感内容提交到公开仓库。本仓库的 `.gitignore` 已排除常见音视频和转写文件，但它不能替代提交前审查。

## 贡献

欢迎提交改进建议。请先阅读 [贡献指南](CONTRIBUTING.md)，并确保任何修改都不弱化事实边界或鼓励编造缺失信息。

## 许可证

本项目采用 [MIT License](LICENSE)。
