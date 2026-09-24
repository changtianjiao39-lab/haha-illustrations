# Prior-art research · 2026-09-24

## 本次任务的发现边界

用户要求把已经认可的一张 HaHa 与灰猫公众号配图沉淀为专属 Skill。已用内置双目录检索器搜索 `Chinese article illustration personal avatar pet visual metaphor` 和 `crayon editorial illustration consistent character`；skills.sh 与 SkillsMP 两路均返回结果，共去重为 56 个候选家族。目录只是发现工具，不能证明适合用户或输出质量。skills.sh installs 是安装量，不是评分；SkillsMP repo stars 是仓库星数，不是 Skill 的使用效果。

## 实际阅读的相关 Skill

| 候选 | 来源与证据 | 学到的机制 | 取舍 |
|---|---|---|---|
| `crayon-girl-illustrations` | [原仓库](https://github.com/dorlarosendo434-hub/crayon-girl-illustrations)，本机安装版本；已阅读 `SKILL.md`、角色、配色、提示词与 QA，原仓库采用 MIT 许可 | 图像参考优先级、每张只讲一个结构、生成后校验角色身份 | 保留工作流与校验原则；不沿用原角色、贝雷帽、固定主图、旧配色预览，也不要求把所有题材画成同类小机器 |
| `haha-dawang-illustrations` | 本机已安装的私人 Skill，已阅读根 `SKILL.md`；未见公开来源或安装量证据 | HaHa 固定身份、从文章找认知动作、灰猫作为搭档、shot list 与逐张保存 | 强化猫咪从“可选”到默认参与；补画面层级、轻微立体感和背景退后规则 |

内置目录检索中 `baoyu-article-illustrator` 的 skills.sh 安装量较高（检索时显示 31.4K），但本次未阅读其源 `SKILL.md`，所以不将其写成研究过的参考，也不借用其实现。下载量不能替代用户视觉偏好的证据。

## keep / adapt / reject / invent

- **keep**：身份标准图、按原文取图、单图一个重点、生成后 QA。
- **adapt**：将“人物 + 可选猫咪”改为“人物主动作 + 猫咪配合动作”，并把认可样图限定为关系与画风参考。
- **reject**：固定复刻 Agent Space 工作台、照搬原图左右模块、把优惠数字画成事实卡片、让背景承载过多信息。
- **invent**：四格文案提炼、双动作句、主物件与 2–3 个辅助场景的因果配合、背景退后与涂鸦材质的逐张检查顺序。

## 缺失证据

尚无跨文章、跨题材的实际生成比较，亦无外部评分或稳定性证明。认可样图仅证明用户偏好这一张的视觉结果。后续需要在真实公众号稿件中逐张检验。
