# SeedShine 深度研究 Skill

技术名：`wechat-deep-research-skill`

默认展示名统一为「SeedShine 深度研究 Skill」；技术名继续保留，以兼容已有调用和项目引用。

一个面向公众号深度文章的研究与写作 workflow。它把产品/行业桌面研究、事实核验和 Writing DNA 结合起来，也支持持续加入新文章语料，蒸馏新的编辑规则并优化 skill。

## 安装

```bash
git clone https://github.com/JoyaJames/wechat-deep-research-skill.git ~/.codex/skills/wechat-deep-research-skill
```

重启 Codex 后，可直接使用 `$wechat-deep-research-skill`。

## 适合什么

- 从公开来源研究产品、公司或行业，并写成有证据链的公众号深度文章
- 分析某个账号/作者的稳定写作风格
- 沉淀自己的写作风格资产
- 对比不同作者在同一议题上的表达差异
- 给 agent/AI 提供更稳定的风格复刻上下文

## 语料要求

真实蒸馏建议准备：

- 至少 30 篇完整文章
- 理想 80-100 篇完整文章
- 单篇最好大于 1000 字
- 文件格式建议为 `.md` 或 `.txt`

`examples/format-only/` 只用于演示目录格式，不代表真实蒸馏效果。不要用少量短文评估这个 skill 的上限。

## 怎么用

1. 复制 `templates/author-corpus/` 作为你的作者语料目录。
2. 把完整文章放入 `raw/` 或 `raw-corpus/`。
3. 让 agent 使用 `wechat-deep-research-skill`，或阅读 `SKILL.md` / `公众号深度研究.skill.md`，并按流程蒸馏所有文章。
4. 等待 agent 输出：
   - `语言DNA.md`
   - `文章结构模板.md`
   - `写作视角与认知框架.md`
   - `视觉风格指南.md`
   - `Writing-DNA.md`
5. 后续写作前，让 agent 先重新阅读所有蒸馏产物，再按该风格写作。

## 重要边界

这个项目用于学习、分析、风格研究和个人写作资产沉淀。请不要用于冒充作者本人、误导读者，或侵犯他人版权。

开源仓库不应包含未经授权的原文语料。你可以放目录模板、字段模板、说明文档和自己拥有版权的示例文本。

## 文件结构

```text
wechat-deep-research-skill/
├── SKILL.md
├── README.md
├── LICENSE
├── agents/
│   └── openai.yaml
├── 公众号深度研究.skill.md
├── docs/
│   ├── release-checklist.md
│   └── usage-boundaries.md
├── templates/
│   └── author-corpus/
│       ├── raw/
│       ├── _meta/
│       ├── 语言DNA.md
│       ├── 文章结构模板.md
│       ├── 写作视角与认知框架.md
│       ├── 视觉风格指南.md
│       └── Writing-DNA.md
└── examples/
    └── format-only/
```

## License

MIT
