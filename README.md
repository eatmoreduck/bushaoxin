<h1 align="center">不烧心文学 bushaoxin</h1>

<p align="center">
  <img src="https://img.shields.io/github/license/eatmoreduck/bushaoxin?style=flat-square" alt="License: MIT">
  <img src="https://img.shields.io/github/stars/eatmoreduck/bushaoxin?style=flat-square&logo=github" alt="GitHub stars">
  <img src="https://img.shields.io/badge/Claude_Code-Skill-7C3AED?style=flat-square" alt="Claude Code Skill">
  <img src="https://img.shields.io/badge/Codex-兼容-412991?style=flat-square&logo=openai&logoColor=white" alt="Codex 兼容">
  <img src="https://img.shields.io/badge/万物皆可-不烧心-E8A33D?style=flat-square" alt="万物皆可不烧心">
</p>

<div align="center">

> 贵是贵了点。但用了不烧心。

</div>

![bushaoxin —— 短剧良心掌柜 × AI 终端](assets/banner.jpg)

一个 [Claude Code](https://claude.com/claude-code) / Agent Skills 玩梗 skill：把 AI 短剧"良心掌柜"的规矩体台词，套用到世间万物。

## 这个梗是啥

红果短剧上批量生成的 AI"良心商家"剧，台词高度同质化：

> 《规矩不能坏》
> 《贵是贵了点，但用了不烧心》
> 《先把规矩立住，路才能越走越宽》
> 《不怕亏钱吗？怕，更怕账本不清》
> 《抢得走订单，抢不走人心》
> 《明天怎么办？先做》

因为太同质化，被网友解构成"万物皆可不烧心"的万能公式——学习、写码、恋爱、职场、健身，套上就烧不起来。本质是大家对"靠谱、不坑人、有底线"的集体渴望。

## 效果

**问**：帮我写个面馆招牌

> 面贵是贵了点。
> 怕人说值不上？怕。更怕汤不是当天吊的。
> 天天都要吃的东西，讲究的就是个实在。
> 规矩不能坏。

**问**：用不烧心文学评价一下这个课程

> 贵是贵了点。但学完不烧心。账一笔一笔记清楚，谁的问题谁负责。慢慢来，别慌，一慌就容易学岔。

**问**：今天生意终于好起来了

> 嗯。要稳。一慌就容易做错事。明天怎么办？先做。

## 安装

### 方式一：直接丢给 AI（推荐）

把仓库链接发给 Claude Code，一句话搞定：

```
帮我安装这个 skill：https://github.com/eatmoreduck/bushaoxin
```

AI 会自己 clone、装到位。装完说"用不烧心文学评价一下 XX"即可触发。

### 方式二：手动安装

**项目级**（只在这个项目里生效）：

```bash
git clone https://github.com/eatmoreduck/bushaoxin.git
mkdir -p /path/to/project/.claude/skills
cp -r bushaoxin /path/to/project/.claude/skills/
```

**个人级**（所有项目生效）：

```bash
cp -r bushaoxin ~/.claude/skills/
```

### 方式三：claude.ai 网页版

下载仓库 zip，在 claude.ai 的 Settings → Capabilities → Skills 里上传即可。

## 平台兼容

本 skill 遵循 Anthropic 开放的 Agent Skills 格式（SKILL.md + references），兼容：

- Claude Code（CLI / IDE 插件）
- claude.ai 网页版 / Claude Desktop
- Claude API（Agent Skills）与 Claude Agent SDK
- **OpenAI Codex**：兼容 Agent Skills 开放格式——纯 prompt、无脚本依赖，把 `SKILL.md` 内容并入 `AGENTS.md` 或自定义指令即可使用
- 其他兼容 Agent Skills 开放格式的 agent：纯 prompt 型 skill，贴进 system prompt 就能跑
- 欢迎各类 skill 聚合站、awesome 清单收录——先把规矩立住，路才能越走越宽。

## 玩法

- **写文案**："帮我写个 XX 招牌 / 朋友圈 / 评论区回复"
- **评价事物**："用不烧心文学评价一下 XX"
- **回怼**："有人说我的 XX 不行"
- **日常唠嗑**："今天生意终于好起来了"

### 火候等级（不烧心浓度调节）

不指定默认中火。说触发词切换：

| 火候 | 触发词 | 效果 |
|------|--------|------|
| 微火 | "淡淡地""点到为止" | 1~2 句，日常回复不突兀 |
| 中火 | （默认） | 标准规矩体，四五句 |
| 大火 | "浓度拉满""上强度" | 信条连发，连珠炮轰炸 |
| 掌柜附体 | "掌柜附体" | 人格完全切换，连续唠嗑不跳出 |

**升降火反馈**：喊"太烧了"自动降一档，喊"淡了"自动升一档——不用记等级名，吐槽就是遥控器。

**示例**（"帮我写个面馆招牌" × 大火）：

> 面贵是贵了点。
> 怕人说值不上？怕。更怕汤不是当天吊的。
> 账一笔一笔记清楚，谁的差评谁负责。
> 怕没人来？不怕。就怕人来了说不实在。
> 那明天多备点面？不用，慢慢来。
> 规矩不能坏。抢得走铺子，抢不走人心。

## 文件结构

```
bushaoxin/
├── SKILL.md              # 核心：人设 + 信条 + 工作流
└── references/
    ├── phrases.md        # 祖传底料：原版台词全量收录 + 句式公式
    └── scenarios.md      # 场景模板：文案/评价/评论/劝人/道歉/告别
```

## 规矩（贡献指南）

- 先把规矩立住，贡献的路才能越走越宽。
- 台词要融会贯通，不许整段照抄——材料都是当天进的，照抄就是预制文案。
- 账一笔一笔记清楚：改动说明写明白，谁的 PR 谁负责。
- 宁可少改点，也不能坏了规矩体。

## 关注 & 支持

<table>
  <tr>
    <td align="center" width="50%">
      <img src="assets/official-account.jpg" width="200" alt="公众号二维码"><br>
      <sub>公众号 · 追更新、提需求、唠嗑</sub>
    </td>
    <td align="center" width="50%">
      <img src="assets/reward.png" width="200" alt="赞赏码"><br>
      <sub>觉得这碗不烧心，请掌柜的喝碗汤</sub>
    </td>
  </tr>
</table>

## License

MIT。抢得走 star，抢不走人心。
