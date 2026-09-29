# Knowledge Map Extractor · 文章知识地图萃取 Skill

将长文、方法论或规范萃取为“静态知识树 + 动态流程轨道 + 跨线映射 + 反馈回路”的交互式知识地图。

核心原则：**大模型负责语义理解和关系判断；代码负责编号、组装、环检测、校验与 HTML 渲染。**

## 安装

```bash
git clone --depth 1 https://github.com/VastFuture/knowledge-map-extractor.git ~/.agents/skills/knowledge-map-extractor
rm -rf ~/.agents/skills/knowledge-map-extractor/.git
```

## 使用

安装后直接输入类似请求：

- “把这篇文章做成知识地图。”
- “萃取这份规范的知识树和方法流程。”
- “标出这些概念如何支撑业务步骤，以及步骤如何反哺规则。”
- “为这个 Markdown 生成交互知识地图 HTML。”

默认输出：

- `model.json`：机器可读的知识骨架
- `index.html`：可交互单文件知识地图

## 结构

```text
knowledge-map-extractor/
├── SKILL.md
├── assets/map-template.html
├── references/extraction-contract.md
└── scripts/
    ├── build_map.py
    └── test_build_map.py
```

## 来源

方法论蒸馏自何明璐的微信公众号文章：[《我如何把一篇文章变成一张知识地图：从静态结构到动态流程的萃取方法》](https://mp.weixin.qq.com/s/d2naZgv1gr-gy8PUkOOHUQ)。

本仓库将文章中的方法固化为 Agent Skill、确定性数据组装脚本和交互式 HTML 模板；原文版权归原作者所有。
