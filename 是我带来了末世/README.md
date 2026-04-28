# 《是我带来了末世》—— AI 辅助长篇小说创作项目

> 末世确实是他带来的。但没有这场末世，蓝星连反抗诸神的资格都没有。

## 项目简介

本书是一部面向番茄小说平台的超长篇网络小说，预计 900 章、约 180 万字，分 10 卷。核心差异化在于：**男主是真正意义上的末世幕后黑手**——他主动开启了蓝星的末日时代，目的是让蓝星文明在诸神注视下获得自保之力。

这不是一个"穿越到末世求生"的故事，而是一个"亲手制造末世以拯救世界"的故事。

## 项目规模

| 维度 | 数值 |
|------|------|
| 总章节数 | 900 章 |
| 每章字数 | 约 2000 字 |
| 总字数 | 约 180 万字 |
| 分卷数 | 10 卷 |
| 每卷章节 | 18 节 × 5 章 = 90 章 |
| 目标平台 | 番茄小说 |

## 文件夹说明

```
是我带来了末世/
├─ AGENTS.md              # 项目总规则和智能体工作流
├─ opencode.json           # opencode 项目配置
├─ README.md               # 本文件
│
├─ .opencode/agents/       # 智能体角色配置
│  ├─ novelist.md          # 小说家：负责正文创作
│  ├─ editor.md            # 编辑：负责审稿和修订
│  ├─ continuity-checker.md # 连续性检查员：防止前后矛盾
│  └─ outline-planner.md   # 大纲规划师：设计分卷和章节大纲
│
├─ docs/                   # 创作圣经——所有设定和规则文档
│  ├─ 00_project_brief.md  # 项目总览
│  ├─ 01_world_bible.md    # 世界观圣经
│  ├─ 02_narrative_rules.md# 叙事规则
│  ├─ 03_style_guide.md    # 文风设定
│  ├─ 04_character_bible.md# 人物设定
│  ├─ 05_power_system.md   # 职业与力量体系
│  ├─ 06_factions.md       # 势力设定
│  ├─ 07_timeline.md       # 时间线
│  ├─ 08_volume_outline.md # 分卷大纲（10卷）
│  ├─ 09_section_outline.md# 节纲（每卷18节×5章）
│  ├─ 10_chapter_outline.md# 章节大纲
│  ├─ 11_continuity_log.md # 连载一致性记录
│  ├─ 12_glossary.md       # 专有名词词典
│  ├─ 13_quality_checklist.md # 章节质检清单
│  └─ 14_platform_strategy.md # 番茄平台连载策略
│
├─ prompts/                # 可复用提示词
│  ├─ generate_world_bible.md
│  ├─ generate_character_bible.md
│  ├─ generate_volume_outline.md
│  ├─ generate_chapter_outline.md
│  ├─ write_chapter.md
│  ├─ revise_chapter.md
│  └─ check_chapter.md
│
├─ drafts/                 # 章节草稿（按卷分目录）
├─ reviews/                # 审查意见存档
├─ final/                  # 定稿章节（按卷分目录）
└─ exports/                # 导出文件
   ├─ tomato_submission/   # 番茄小说投稿用
   └─ full_backup/         # 完整备份
```

## 推荐工作流

### 1. 初始化（已完成）
所有设定文档已在 `docs/` 目录中创建完毕。

### 2. 写新章节
```
请根据 docs/10_chapter_outline.md 中第X章的章纲，写出正文。
```

### 3. 修订章节
```
请根据 docs/13_quality_checklist.md 检查并修订 drafts/volume_XX/ch_XXXX.md
```

### 4. 连续性检查
```
请对刚完成的章节进行连续性检查，更新 docs/11_continuity_log.md
```

### 5. 扩展到下一卷
```
请为第X卷生成详细大纲，写入 docs/08_volume_outline.md
```

## 如何让智能体写章节

1. 确保智能体已加载项目配置（opencode.json 会自动加载 instructions）
2. 告诉智能体你要写哪一章（如："写第1卷第1章"）
3. 智能体会自动读取相关设定文档
4. 智能体写出正文到 `drafts/volume_01/ch_0001.md`
5. 智能体自动更新 `docs/11_continuity_log.md`
6. 你审查通过后，智能体将文件移至 `final/volume_01/ch_0001.md`

## 核心创作理念

- **幕后黑手**：男主不是传统英雄，他的每个行动都在暗中推动世界
- **真实末世**：这不是游戏，死亡是永久的，城市毁灭是真实的
- **群像叙事**：故事由多个人物的视角展开，男主只是暗线
- **文明进化**：蓝星从现代文明逐步进化为能对抗神明的战争文明
- **反神**：诸神不是不可战胜的——这是这个故事存在的根本理由

## 当前状态

- [x] 项目框架搭建完成
- [x] 创作圣经 v2.0 全部就绪（15 份核心文档）
- [x] 第一卷 90 章完整章纲（18 节 × 5 章，全部含 POV/钩子）
- [ ] 第 1 章正文待写
