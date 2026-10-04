# make-knowledge-cards

## 解决什么问题

将用户粘贴的文章、笔记或本地 Markdown/TXT 文件，提炼成适合复习的知识卡片。每张卡片聚焦一个重要且不重复的概念，避免把长文直接改写成冗长摘要。

## 主要功能

- 从输入中识别并优先覆盖核心概念。
- 根据内容的独立概念数量生成 5–8 张卡片；信息不足时不虚构内容凑数。
- 每张卡片均包含标题、核心知识、简明解释，以及源内容支持的例子或自测问题。
- 合并重叠内容，保留原文术语与意图。
- 仅处理用户提供的文本和本地 `.md` / `.txt` 文件；不处理网页、PDF、Anki 导出或图形卡片。

## 安装方法

此项目不需要额外安装依赖。将 `skills/make-knowledge-cards` 保留在 Codex 可发现的 Skill 目录中即可使用。

如需在本项目中查看或维护 Skill 文件：

```text
skills/make-knowledge-cards/SKILL.md
skills/make-knowledge-cards/agents/openai.yaml
```

## 使用方法

在 Codex 中调用 Skill，然后直接粘贴文本，或提供本地 Markdown/TXT 文件路径：

```text
Use $make-knowledge-cards to turn the following notes into study cards:

Photosynthesis converts light energy into chemical energy. Chlorophyll absorbs light...
```

也可以指定文件：

```text
Use $make-knowledge-cards to convert ./notes/article.md into knowledge cards.
```

## 输入与输出示例

**输入：**

```text
Photosynthesis converts light energy into chemical energy. Chlorophyll absorbs light.
```

**输出：**

```markdown
## Card 1 — Photosynthesis purpose

**Core knowledge:** Photosynthesis converts light energy into chemical energy stored in organic molecules.

**Brief explanation:** It lets plants use captured light to build energy-rich compounds.

**Example / self-check:** What form of energy does photosynthesis capture, and what does it produce?
```
