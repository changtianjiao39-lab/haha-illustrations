# HaHa 与灰猫·公众号蜡笔配图 Skill

把文章里的关键意思转成 HaHa 与灰猫共同参与的暖纸面蜡笔插画。这个公开包包含 HaHa 人物、灰猫和用户认可的文章示例图，可直接按这些身份参考生成同画风的公众号配图。

![HaHa 与灰猫的文章配图示例](assets/approved-editorial-example.png)

这张例图用人物操作中心装置、猫咪带来会话卡、侧边场景回应文案中的成本与协作。它是**互动关系与画面层级**的示范，不是以后每张图都要复刻的布局。四张参考图的逐项用途和新文案配图说明见 [配图说明](references/illustrated-guide.md)。

## 这个 Skill 做什么

- 从中文公众号文案中找适合配图的判断、转折和动作；
- 让 HaHa 做核心动作，灰猫参与发现、递送、回应或提醒；
- 让场景物件和辅助小图案对应文案，并保持统一蜡笔质感；
- 逐张检查身份、文字、画面层级和背景是否喧宾夺主。

默认输出 16:9 横版正文图。用户要求小红书等竖版内容时采用 3:4 与纵向阅读路径；封面另设标题层级。仅在用户要求时制作不带猫咪的版本。用户只要规划时先给 shot list，不生图。

## 使用

你可以直接这样说：

- “用 `$haha-illustrations` 给这篇公众号文章做一张配图，先给我一张试图。”
- “分析这段文案，规划 HaHa 和灰猫的 4 张文章插图，先不要生成。”
- “把刚才那张背景收简单一点，保留 HaHa 和猫咪的互动。”

将文章正文放在指令后面即可。没有正文时，可先给用途、主题和想表达的判断。

## 安装

可复制以下命令安装公开 Skill：

```bash
npx skills add changtianjiao39-lab/haha-illustrations
```

也可手动安装：

```bash
git clone https://github.com/changtianjiao39-lab/haha-illustrations.git
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./haha-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

安装后确认 `skills/haha-illustrations/SKILL.md` 与 `assets/` 中的四张参考图存在，必要时重新打开 Codex。

## 最小使用示例

```text
用 $haha-illustrations 给这段公众号文案生成一张 16:9 配图。
保持 HaHa 和灰猫的外形，让他们围绕同一件事行动；背景保持安静。
[粘贴文案]
```

想先看方案时说“先给 shot list，不生成图片”。想修改现有图时附上图片并指出要改的部分。

## 参考图与配图说明

- [原始数字形象](assets/original-multiview.png)：身份参考，不能继承 3D 画法。
- [人物标准图](assets/haha-character.png)：人物外形、蓝黄配色与蜡笔比例。
- [灰猫标准图](assets/gray-cat.png)：宠物毛色、眼睛、项圈与统一笔触。
- [认可例图](assets/approved-editorial-example.png)：只学习人物、猫咪、道具和背景的叙事关系。
- [图解说明](references/illustrated-guide.md)：每张图对应的作用和三种文章题材的构图示范。

## 参考与边界

`assets/approved-editorial-example.png` 是用户喜欢的单张样图，只提供关系和画风参考。角色身份来自 `assets/original-multiview.png`，蜡笔版标准来自 `assets/haha-character.png` 和 `assets/gray-cat.png`。不要把样图中的 Agent Space 工作台或任何产品宣称复制到无关文章。产品价格、额度等说法在配图中出现前仍需来源核对。

## 验证与常见问题

安装可通过确认根目录 `SKILL.md`、两张角色参考图及 `evals/trigger_cases.json` 存在来检查；开发时可使用 `validate_skill.py` 做包结构校验。这些静态检查不替代生成后的人眼审图。

- 若出现旧版贝雷帽女孩，检查是否同时加载了其他配图 Skill，并明确调用 `$haha-illustrations`。
- 若背景过花，先删多余场景，仅保留一个主物件和少量辅助线索。
- 若猫咪只是摆设，重写猫咪动作，使其与主物件发生递送、追随或反馈关系。
- 若中文字错误，局部编辑或交付无字图；不要保留错字。

设计方法参考的公开源仓库：[crayon-girl-illustrations](https://github.com/dorlarosendo434-hub/crayon-girl-illustrations)。本仓库在此方法基础上加入 HaHa 与灰猫的固定形象、双角色互动和逐图文案映射；与原仓库独立发布。

## 授权与使用边界

本仓库按 [MIT 协议](LICENSE) 发布。参考图片中的 HaHa 标识、第三方名称和商标仍归各自权利人；开源协议不授予第三方商标使用权。生成的中文文字、价格与产品说法须在正式发布前逐字和逐项复核。
