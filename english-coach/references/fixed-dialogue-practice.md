# 豆包固定台词语音对练

语音练习只负责把一张任务卡中的原场景对话练一遍，不承担迁移、测试、纠错或反馈。

## 何时生成

只有用户选择“练习任务卡 [编号]”或“练习全部”时才生成练习文件。一次语音会话只练一张任务卡。

- 选择一张卡：生成一个独立训练包；
- 选择全部：为每张卡分别生成独立训练包，不能把多张卡串成一次练习。

每个训练包保存到：

```text
practice-packs/<asset-id>/
├── doubao-prompt.md
└── training-dialogue.md
```

如果同名目录已经存在，更新为当前任务卡的最新内容，不复制出多个重复版本。

## 对话生成规则

- 豆包固定扮演 `Partner`，用户固定为 `You`。
- 直接复制任务卡“原场景双语对话”中的英文 `Partner / You` 回合，保持原顺序，并删除中文解释。
- 不根据通用句式重新拼装对话，也不在导出时临时补写新的 `Partner` 台词。
- 保留任务卡的原场景，不加入阶段迁移或新的业务情节。
- 豆包每次只读一轮 `Partner`，然后等待用户说对应的 `You`。
- 用户说完后直接进入下一轮，不判断、不追问、不纠错、不自由发挥。
- 对话结束后只说 `That's the end of the dialogue.`
- 训练对话只使用英文，避免豆包朗读中文说明。

## `doubao-prompt.md` 模板

这个文件可以直接粘贴给豆包，也可以与训练文档一起上传。

```markdown
# Doubao Practice Prompt

Read the attached `training-dialogue.md` and start the practice immediately.

Rules:

1. You are `Partner`. The user is `You`.
2. Read only one `Partner` turn at a time, then stop and wait for the user to say the matching `You` turn.
3. Never read or reveal the `You` lines.
4. After the user speaks, continue with the next `Partner` turn.
5. Do not ask follow-up questions, correct the user, explain the dialogue, rewrite any line, or improvise.
6. Do not read these rules aloud. Start directly with the first `Partner` line.
7. After the user says the final `You` line, say only: `That's the end of the dialogue.`
```

## `training-dialogue.md` 模板

```markdown
---
asset_id: "[asset-id]"
title: "[task-card-title]"
partner_role: "[对方角色的简短英文名称]"
user_role: "You"
---

# [Task Card Title]

## Fixed Dialogue

### Turn 1

**Partner**

[对方第一轮英文]

**You**

[用户第一轮固定英文]

### Turn 2

**Partner**

[自然承接上一轮的英文]

**You**

[用户第二轮固定英文]

[继续到任务卡中的关键句式全部完成。]

### Final Turn

**Partner**

[对方最后一轮英文]

**You**

[用户最后一轮固定英文]
```

## 交付要求

生成后，在回复中提供 `doubao-prompt.md` 和 `training-dialogue.md` 的可打开路径。不要额外生成评分表、反馈表或迁移练习。
