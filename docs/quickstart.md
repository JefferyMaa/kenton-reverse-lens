# kenton-reverse-lens Quickstart

本指南用于完成一次最短的首次成功：让 Agent 发现 `kenton-reverse-lens`，基于一份可验证材料完成两段式分析，并把外部方法转换成适合“一个人 + AI”的品牌行动。

## 1. 确认宿主和材料

你的 Agent 宿主需要支持目录式 `SKILL.md`。首次测试还需要：

- 一条可完整读取的视频、转写稿或文章；
- 可确认的创作者身份或账号背景；
- 一个具体品牌目标；
- 你在会话中参与判断和纠偏。

本项目没有声明兼容的宿主名称和版本，也不包含抓取、下载或 ASR 实现。

## 2. 安装 Skill

```bash
git clone https://github.com/JefferyMaa/kenton-reverse-lens.git
cp -R kenton-reverse-lens <YOUR_AGENT_SKILLS_DIR>/
```

不要把 `<YOUR_AGENT_SKILLS_DIR>` 原样执行；它代表宿主要求的 Skills 目录。

安装后重新启动宿主或开启新会话，检查可用 Skill 列表中是否出现：

```text
kenton-reverse-lens
```

## 3. 准备首次输入

建议用以下最小输入：

```text
分析对象：<CREATOR_NAME_AND_BACKGROUND>
账号类型：<INTERVIEW_OR_TEACHING_OR_FACELESS>
原始材料：<URL_OR_TRANSCRIPT>
我的品牌目标：<BRAND_GOAL>
```

身份或账号类型不确定时可以写“不确定”，要求 Agent 在分析中保留证据边界。

## 4. 发送测试请求

```text
请用 kenton-reverse-lens 完整分析以上材料。

第一部分还原他的想法、做法和方向；
第二部分先剥时代外壳，再回答我该怎么做、怎么搭建、怎么思考。
事实要锚定材料，推断标记为“⚪ 推断”。
```

## 5. 验收结果

首次成功至少满足：

1. 正确识别或谨慎标注人物与账号类型；
2. 第一部分包含真实方法、顺序、数字或判断证据；
3. 第二部分明确先做“剥时代外壳”；
4. 建议适配“一个人 + AI”，没有直接复制资本级组织；
5. 有“怎么做、怎么搭建、怎么思考”三个落点；
6. 至少给出一个非显然连接；
7. 事实、ASR 噪声和战略推断没有混写。

若缺少其中任一项，见 [故障排查](troubleshooting.md)。

## 6. 从单条扩展到 corpus

单条测试通过后，再按相同结构逐条增加材料：

1. 每条内容形成一个独立分析节点；
2. 记录来源、人物、账号类型和证据；
3. 跨节点寻找因果、叠加关系和矛盾；
4. 最后再汇总为思维导图或品牌商业版图。

不要在没有来源清单的情况下声称“已经吃透全部内容”。
