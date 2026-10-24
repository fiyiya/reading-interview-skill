# English Coach

把真实职场对话变成可复用的英语沟通任务卡，并生成固定台词语音练习。

## 安装到 Codex

将本仓库克隆到临时目录，再把其中的 `english-coach/` 文件夹复制到 `~/.codex/skills/english-coach/`（若设置了 `CODEX_HOME`，则放到 `$CODEX_HOME/skills/english-coach/`）。重新打开 Codex 会话后调用 `$english-coach`。

也可以直接把以下指令发给 Codex：

```text
请使用 skill-installer 安装 https://github.com/fiyiya/reading-interview-skill/tree/main/english-coach ，技能名为 english-coach。
```

本仓库根目录的 Skill 是 Reading Interview；安装 English Coach 时请选择 `english-coach` 子目录。

## 使用

1. 上传已获授权使用的职场对话转录，输入：“调用 $english-coach，处理这份工作对话。”
2. 技能会整理对话、筛选高价值沟通任务，并生成最多三张双语任务卡；证据不足时减少卡片数量。
3. 输入“练习任务卡 02”，生成豆包 Prompt 与英文训练对话。上传训练文件并粘贴 Prompt 后开启语音练习。
4. 遇到新场景时，描述人物、目标和限制，让技能检索自己的卡库，准备适合当下的英语对话。

固定台词练习中，语音工具扮演 Partner，使用者扮演 You；不自由发挥、不评分、不纠错。

## 文件与隐私

公开安装包只包含技能说明、五份通用参考、界面配置与空资产索引，没有预装的真实对话、个人卡片或学习记录。每位使用者从自己的材料建立卡库。

任务卡默认保存于安装目录下的 `library/cards/`，练习包保存于 `practice-packs/`。需要只在对话中使用时，请明确说“不保存”。生成内容默认保存在本地；将内容交给其他语音服务时，请自行确认材料可被该服务处理。

仓库忽略规则排除生成的卡片和练习包。索引会随使用而变化，也可能包含敏感描述；发布或贡献前应恢复为空索引并检查全部待提交文件。

## 环境要求

需要支持本地 Skill 的 Codex 环境和本地文件读写能力。核心流程不需要 API Key，也不要求安装 Python 或其他依赖。豆包仅用于可选的外部语音对练，不会由技能自动连接。
