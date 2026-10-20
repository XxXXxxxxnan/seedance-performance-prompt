# Seedance 2.5 真实表演提示词 Skill

为 Seedance 2.5 写人物表演 / 微表情视频提示词的 skill。把一句镜头描述转成带**人物内心、物理因果链、节拍节奏**的真实表演提示词，适用于任意视角（面部特写、中近景、过肩、全身、背影跟拍、第一视角、远景）。

## 核心理念

1. **演员演的是“对抗情绪”**：写人物想要什么、在压抑什么，让情绪从细节里泄漏出来。
2. **细节来自因果链**：环境 → 身体 → 画面 / 声音；情绪叠加在生理反应之上。
3. **节奏靠“紧迫目标 + 动作重叠 + 一个主停顿”**。

## 包含内容

- `SKILL.md`：工作流程、核心规则、提示词模板、输出格式、自检清单
- `references/viewpoints.md`：视角与表演载体对照、载体转换规则、面部微表情词汇
- `references/conditions.md`：物理条件库（温度天气、身体状态、特殊空间、心理状态）及因素相互作用
- `references/debugging.md`：节奏、物理反应、画面一致性、平台审核的调试对照
- `examples/`：5 个完整示例（输入 → 选择说明 → 提示词 → 测试观察点）
  - 面部特写 · 老友提起已故母亲
  - 第一视角 · 长征雪山捡起战友的红旗（含节奏修改过程）
  - 第一视角·静 · 微山湖芦苇荡发现日军
  - 第一视角·动 · 捷克式轻机枪扫射
  - 第一视角·面对角色 · 白刃战

## 使用方法

将 `seedance-performance-prompt/` 文件夹放入你的 skills 目录（或在 Claude 中导入该 skill），之后直接描述镜头即可，例如：

> 镜头（第一视角）：红军长征，主角从冻死的战士遗体上捡起红旗，抬头望见风雪中的队伍。

## 文件结构

```
seedance-performance-prompt/
├── SKILL.md
├── references/
│   ├── viewpoints.md
│   ├── conditions.md
│   └── debugging.md
└── examples/
    ├── 01-face-closeup-friend.md
    ├── 02-pov-long-march-flag.md
    ├── 03-pov-weishan-reeds.md
    ├── 04-pov-machine-gun.md
    └── 05-pov-bayonet-duel.md
```

另附 `dist/seedance-performance-prompt-single.md`：把以上内容合并成单个 SKILL.md 的版本，适用于只支持单文件的平台。
