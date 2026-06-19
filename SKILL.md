---
name: feynman-cards
description: Generate 6 progressive Feynman learning cards for any topic as a beautiful HTML file. Use when the user wants to learn, understand, or explain a concept, or mentions Feynman technique, learning cards, or study materials.
---

# Feynman Cards

Generate 6 cards of increasing depth for any topic, inspired by the Feynman technique: if you can't explain it simply, you don't understand it well enough.

## Workflow

1. **Ask for a topic** if not provided (e.g. "量子纠缠", "React Hooks", "博弈论")
2. **Generate 6 cards** following the depth levels below
3. **Output a single HTML file** using the template structure
4. **Show the file** via `present_files`

## Card Levels

Each card has a distinct color scheme and increasing depth:

| # | Level | Audience | Color | Style |
|---|-------|----------|-------|-------|
| 1 | 启蒙 | 6岁小孩 | warm peach `#FFEAA7` | playful, big fonts, emoji |
| 2 | 入门 | 初中生 | mint `#55EFC4` | friendly, intro terminology |
| 3 | 进阶 | 大学生 | sky blue `#74B9FF` | academic, frameworks |
| 4 | 精通 | 同行专家 | lavender `#A29BFE` | technical, cutting-edge |
| 5 | 未知 | 自己 | light gray `#DFE6E9` | **dashed border**, honest gaps |
| 6 | 图谱 | 全景 | rose gold `#FAB1A0` | concept map, connections |

## Content Guidelines

**Card 1 — 给小孩讲**: Use vivid metaphors from daily life. No jargon. Use emoji. Think "it's like..." explanations.

**Card 2 — 给中学生讲**: Introduce 2-3 key terms with simple definitions. Use one concrete example.

**Card 3 — 给大学生讲**: Formal definitions, theoretical framework, key formulas or models. Reference foundational papers/textbooks.

**Card 4 — 给同行讲**: Technical precision, current research frontiers, open debates, practical implications.

**Card 5 — 我还不懂**: List 3-5 specific questions you (as a learner) still can't fully answer. This card uses a **dashed border** — a visual reminder that real learning begins with honest gaps.

**Card 6 — 概念地图**: Show 4-6 related concepts and how they connect. Use a simple text-based diagram or describe the relationships.

## HTML Output

Generate a **single self-contained HTML file**. Use the template from [template.html](template.html) as the base structure. Replace:

- `{{TOPIC}}` — the topic name
- `{{DATE}}` — generation date
- `{{CONTENT_1}}` through `{{CONTENT_6}}` — card content
- `{{RELATIONS}}` — concept map content for card 6

Each card's content should be semantic HTML (paragraphs, lists, emphasis). Do NOT wrap in extra `<html>` or `<body>` tags.

## Quality Checks

- Each card must have **substantively different** content, not just rephrased
- Card 5 must be genuinely humbling — real open questions, not fake ones
- Card 6 must show **connections** between concepts, not just a list
- The whole file must be valid, self-contained HTML with no external dependencies
