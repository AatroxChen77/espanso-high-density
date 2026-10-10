# espanso-high-density

用三个 Espanso 快捷词，将高信息密度表达约束插入任意 AI 聊天输入框。

AI 回复常有长铺垫、机械转折、空洞设问和重复总结；这些快捷词可用于新对话，也能在长对话中快速纠偏。

## 快捷词

| 触发词 | 用途 |
| --- | --- |
| `:hd-style` | 插入完整表达约束，适合新对话 |
| `:hd-fix` | 按约束重写上一条回复 |
| `:hd-reset` | 重申约束，要求后续回复持续遵守 |

## 安装

### 交给 Coding Agent

将下面的提示词复制给 Codex、Claude Code 或其他能操作本机文件的 Coding Agent：

```text
请在这台电脑安装 Espanso 的 espanso-high-density 配置：
https://github.com/AatroxChen77/espanso-high-density

1. 识别操作系统并检查 Espanso 是否已安装、正在运行。未安装时，按 Espanso 官方安装说明安装；如需管理员权限或系统授权，告诉我需要完成的操作，不要绕过授权。
2. 运行 `espanso path` 获取实际配置目录，不要猜路径。只检查活动 match 配置中的三个目标 trigger，并获取仓库里的 `match/high-density.yml`。若仓库暂不可访问，说明原因并等我提供文件；不要输出无关个人配置。
3. 安装前比较三个 trigger 和完整替换文本。相同定义视为已安装；若只缺少部分定义，只补缺少项，避免重复 trigger。若同名 trigger 的替换内容不同，或目标文件含有其他配置，不要覆盖；报告冲突文件和 trigger，等我决定。
4. 无冲突时，只将缺少的定义写入实际配置目录的 `match/high-density.yml`，保留已有文件内容。目标文件已存在时，确认其中仅有本项目定义后再补齐；含有无关配置则按第 3 条停止。若三个定义均已存在且相同，不做写入。
5. 安装后确认 Espanso 正在运行并已加载配置；可用 `espanso status` 或系统托盘、进程状态检查运行情况。若未运行则启动；若运行中但未加载则按需重启，再检查日志或 CLI 结果。使用当前版本支持的 `espanso match list` 命令核实三个 trigger 均已注册，且替换文本正确。
6. 若无法安全地自动验证实际展开，请告诉我在空白文本框中逐个输入三个 trigger 手动测试；不要把测试文本发送到 AI 对话。
7. 汇报安装路径、修改内容、运行与加载状态、trigger 检查结果，以及仍需我手动完成的步骤。不要改动其他 Espanso 配置。
```

### 手动安装

1. 按照 [Espanso 官方说明](https://espanso.org/install/)安装并启动 Espanso。
2. 运行 `espanso path` 获取配置目录。常见默认位置：Windows `%APPDATA%\espanso`；macOS `$HOME/Library/Application Support/espanso`；Linux `$XDG_CONFIG_HOME/espanso`（通常为 `~/.config/espanso`）。
3. 将 [`match/high-density.yml`](match/high-density.yml) 复制到配置目录的 `match/` 文件夹。等待自动重载；若未生效，运行 `espanso restart`。在空白文本框中输入三个 trigger 检查展开。

配置路径详见 [Espanso 配置文档](https://espanso.org/docs/configuration/basics/)；运行与故障排查见 [Getting Started](https://espanso.org/docs/get-started/)。

## 表达原则

简单问题简短回答；复杂问题保留必要的依据、推理和技术细节。

## English

A small Espanso match set for concise, high-information AI replies across chat tools. It reduces unnecessary preambles and repetition while preserving useful reasoning and technical detail.

## License

[MIT](LICENSE)
