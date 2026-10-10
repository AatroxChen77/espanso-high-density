# espanso-high-density

用 Espanso 快速插入中文提示词，帮助 AI 结论先行、减少冗余，并保留必要的依据和技术细节。

## 项目介绍

Espanso 将快捷词展开为完整提示词。输入框在哪个平台、哪种 AI 工具中都可以使用，包括 ChatGPT、Claude、Gemini、DeepSeek 和 Coding Agent。

## 为什么做这个项目

AI 回复有时会铺垫过多、重复总结，或用机械化转折和空洞设问拉长表达。自定义指令可以提供长期偏好；快捷词则方便在新对话中快速加入约束，也能在长对话中随时纠偏。

## 快捷词

| 触发词 | 功能 | 使用场景 |
| --- | --- | --- |
| <code>:hd-style</code> | 插入完整的高信息密度表达约束 | 新对话开始时使用 |
| <code>:hd-fix</code> | 要求 AI 按约束重写上一条回复 | 回复冗长、铺垫或重复较多时 |
| <code>:hd-reset</code> | 重新强调约束，要求后续回复继续遵守 | 长对话中风格逐渐偏离时 |

## 安装

1. 按照 [Espanso 官网安装说明](https://espanso.org/install/)安装并启动 Espanso。
2. 在终端运行 <code>espanso path</code>，找到当前配置目录。常见默认位置：
   - Windows：<code>%APPDATA%\espanso</code>
   - macOS：<code>$HOME/Library/Application Support/espanso</code>
   - Linux：<code>$XDG_CONFIG_HOME/espanso</code>，通常是 <code>~/.config/espanso</code>
3. 将本项目的 [<code>match/high-density.yml</code>](match/high-density.yml) 复制到配置目录的 <code>match/</code> 文件夹中。例如 Windows 路径通常为 <code>%APPDATA%\espanso\match\high-density.yml</code>。如果 <code>match/</code> 不存在，请先创建。
4. Espanso 通常会自动重新加载配置；如果没有生效，按官网文档重启 Espanso。打开任意文本输入框，输入一个触发词确认展开。

更多配置目录信息见 [Espanso 配置文档](https://espanso.org/docs/configuration/basics/)；首次运行和故障排查见 [Getting Started](https://espanso.org/docs/get-started/)。

## 使用示例

- 开始新对话：输入 <code>:hd-style</code>，让完整约束展开，再补充具体问题。
- 回复需要精简：输入 <code>:hd-fix</code>，要求 AI 重写上一条回复。
- 长对话风格偏离：输入 <code>:hd-reset</code>，要求后续回复继续遵守约束。

## 设计理念

用更低的阅读成本传递更多有效信息。简单问题简短回答；复杂问题保留必要的推理依据、证据和技术细节。它是一组实用的 Espanso 文本扩展配置，不是 AI Agent 框架。

## English

A small Espanso match set for inserting concise, high-information writing instructions into any AI chat input. It helps reduce unnecessary preambles, repetitive summaries, and formulaic contrasts while preserving useful reasoning and technical detail.

## License

[MIT](LICENSE)
