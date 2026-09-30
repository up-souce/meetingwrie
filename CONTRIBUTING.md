# 贡献指南

欢迎通过 Issue 或 Pull Request 改进本 skill。

## 修改原则

- 保持纪要对原始材料的可追溯性；不要把建议、推测或沉默升级为决议。
- 不要加入虚构责任人、期限、数据或会议信息的默认行为。
- 避免加入与会议纪要无关的工具依赖、模板或流程。
- 示例中不得包含真实会议、客户、人员或录音数据。

## 提交前检查

1. 确保 `SKILL.md` 的 YAML frontmatter 有效，且 `name` 与 skill 用途一致。
2. 若新增引用资料，必须从 `SKILL.md` 中说明其使用场景。
3. 使用 Codex 的 skill 校验器运行：

   ```powershell
   python "$env:USERPROFILE\.codex\skills\.system\skill-creator\scripts\quick_validate.py" .
   ```

4. 检查暂存区，确认未提交录音、转写稿或其他敏感材料。
