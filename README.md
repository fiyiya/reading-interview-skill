# Reading Interview

一个用于读后访谈的 Codex Skill。

它会完整浏览读物的目录、原文、划线和个人批注，先梳理全书结构与读者的注意力，再沿章节共同研读。AI 负责找回材料、连接证据和提出临时理解，读者可以通过确认、选择或修正轻松参与，最后回看整场访谈留下了什么。

适用于书籍、文章、报告，以及带文字稿的音视频。不用于普通摘要、单纯导出笔记或代写书评。

## 本仓库的 Skills

| Skill | 路径 | 用途 |
|---|---|---|
| Reading Interview | 仓库根目录 | 阅读材料梳理与共同研读 |
| [English Coach](english-coach/README.md) | `english-coach/` | 职场英语任务卡与固定台词语音练习 |

安装 English Coach：

```text
请使用 skill-installer 安装 https://github.com/fiyiya/reading-interview-skill/tree/main/english-coach ，技能名为 english-coach。
```

English Coach 支持 Codex、TRAE、WorkBuddy 等 Agent 的技能或文档加载方式，并提供完整单文件版。从空卡库开始，不包含个人对话、任务卡或学习记录。[跨产品安装说明](english-coach/README.md) · [下载独立 ZIP](https://github.com/fiyiya/reading-interview-skill/releases/latest/download/english-coach.zip)。

## 安装 Reading Interview

把本仓库地址发给 Codex，并告诉它：

```text
请安装这个 Skill：https://github.com/fiyiya/reading-interview-skill
```

也可以下载 ZIP，解压后将文件夹交给 Codex，并告诉它安装根目录的 `reading-interview`；其中 `english-coach/` 是另一个独立 Skill。

## 使用

准备好目录、原文、划线和个人批注后，可以直接说：

```text
获取《书名》的目录、完整划线和个人想法，再用 reading-interview 对我进行访谈。
```

如果材料已经在当前对话中，可以说：

```text
使用 reading-interview，结合这些材料对我进行读后访谈。
```

## 工作方式

1. 回顾与全书结构梳理
2. 沿章节进行阅读访谈
3. 回看整场访谈留下了什么

“往深、往宽、退后一步”是访谈中的后台视角，不会变成固定问题清单。

## 隐私

本仓库只包含 Skill 指令，不包含书籍原文、个人划线、个人批注、历史会话、API Key 或其他账户信息。实际使用时，阅读材料如何获取和保存取决于用户所使用的阅读服务及其授权设置。
