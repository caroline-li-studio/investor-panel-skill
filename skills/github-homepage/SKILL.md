---
name: github-homepage
description: Create or improve a GitHub repository homepage/README for an open-source project. Use when Codex should write, rewrite, review, or polish README.md, README.zh-CN.md, README.en.md, GitHub project landing pages, hero sections, badges, quick-start instructions, installation prompts, feature summaries, diagrams, social launch copy, or repo promotion text. Trigger on requests like "make the GitHub homepage", "rewrite the README", "make this repo easier to understand", "write a Chinese GitHub README", "add a logo/hero image", "make the project more promotable", "write one-line Codex install instructions", "prepare the repo homepage before push", or "help me promote this GitHub project".
---

# GitHub Homepage

Use this skill to turn a repository into a clear, compelling GitHub homepage. The goal is not to document everything; the goal is to make a stranger understand the project quickly and want to try it.

## Core Rule

Lead with the project's sharpest selling point, not its implementation flow.

Before editing, identify:

- **Audience**: who should care.
- **Promise**: what this project uniquely gives them.
- **Moment of recognition**: the sentence that makes them think "I get it".
- **Try path**: the shortest way to install, run, or ask Codex to install it.

If the README starts with architecture, folder structure, or internal workflow before the value proposition, rewrite the top.

## Workflow

1. **Read the repo first**: inspect `README*`, key source files, assets, and package metadata.
2. **Find the hook**: summarize the project in one sentence that a busy reader understands in 3 seconds.
3. **Design the first screen**: title, short tagline, hero/logo image if useful, and one paragraph of plain-language value.
4. **Write the try path**: one command or one Codex prompt. Avoid long setup before the user knows why they care.
5. **Explain what it does**: benefits first, features second.
6. **Show the workflow**: use Mermaid when it clarifies the mental model.
7. **Set boundaries**: what it is not, what it will not do, and any safety or accuracy limits.
8. **Keep structure scannable**: short sections, tables only when they reduce complexity, no wall of text.
9. **Validate**: check links, image paths, Mermaid syntax shape, and repo-relative paths.

## Default README Order

Use this order unless the repo clearly needs something else:

1. Project name
2. One-line promise
3. Hero/logo image
4. Short value paragraph
5. Install / try now
6. What you get
7. How it works
8. Examples
9. Structure
10. Boundaries / license / status

For Chinese README files, use natural Chinese product language rather than translated English. See `references/chinese-style.md`.

## Visual Guidance

Prefer a strong first visual when the project is abstract:

- A hero image that communicates the product promise.
- A simple logo if the repo needs identity.
- A Mermaid diagram when the flow or mental model matters.

Do not let the visual explain the wrong thing. If the selling point is "many experts debate", do not use a pipeline image as the hero. If the selling point is "one command deploy", do not lead with an architecture map.

For visuals, read `references/visuals.md`.

## Installation Copy

For Codex skills, prefer a one-message install prompt:

```text
请从这个仓库安装 Codex skills：
<repo-url>

请把 skills/ 下的完整技能文件夹安装到我的 Codex skills 目录中。
不要只复制 SKILL.md。
```

If the repo contains shared files such as `skills/_shared`, mention them explicitly:

```text
请把 skills/ 下的完整技能文件夹安装到我的 Codex skills 目录中，包括 skills/_shared。
不要只复制 SKILL.md。
```

## Output Modes

When asked to create or rewrite a homepage:

- Edit the README and relevant assets directly.
- Preserve the user's existing project facts.
- Keep unsupported claims out of the README.
- If a repo URL is unknown, use a clear placeholder and mention it in the final answer.

When asked for a review:

- Lead with specific issues and suggested changes.
- Prioritize clarity, selling point, install path, and visual fit.

When asked for promotion:

- Read `references/social-promotion.md`.
- Write natural launch posts and friendly comment templates, not corporate copy.

## Resources

Load only what is needed:

- `references/readme-patterns.md`: homepage structure, examples, and anti-patterns.
- `references/chinese-style.md`: Chinese README tone and copy patterns.
- `references/visuals.md`: hero image, logo, Mermaid, and asset guidance.
- `references/social-promotion.md`: launch tweet/post and comment styles.
