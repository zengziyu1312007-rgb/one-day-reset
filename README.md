<div align="center">

# 一天重置人生（one-day-reset）

**一个给 AI 助手用的 Skill：让 AI 当教练，带你用一天换身份，合成一页纸「人生游戏卡」。**

改编自 Dan Koe 长文《[How to fix your entire life in 1 day](https://letters.thedankoe.com/p/how-to-fix-your-entire-life-in-1)》（2025-12-23，副题 "do this before 2026"）。

</div>

---

## 这是什么

你立的 flag 活不过二月，多数时候不是不努力，是你还在用旧身份活着。这篇文章把"改行为"换成"改身份"，并给了一套一天跑完的重置协议。

这个仓库把那篇约 5800 词的英文长文蒸馏成了一个 **Agent Skill**（SKILL.md），给 Claude Code、ZCode 等支持 skill 的 AI 助手用。装上之后，AI 不再给你灌鸡汤，而是按协议当一天教练：

- **早晨 · 心理挖掘**：14 道题把自己挖一遍——痛苦 4 题、反愿景 7 题、愿景 MVP 3 题
- **白天 · 打断自动驾驶**：六个定时问题（11:00 / 13:30 / 15:15 / 17:00 / 19:30 / 21:00）设进手机提醒
- **晚上 · 合成**：把一天的记录压成一页纸**人生游戏卡**——

| 游戏卡 | 含义 |
|---|---|
| 赌注 | 反愿景一句话：你绝不让人生变成的样子 |
| 怎么赢 | 愿景 MVP 一句话：会进化的 v0.1 |
| 身份陈述 | 我是那种________的人 |
| 主线任务 | 一年内要成真的一件具体的事 |
| Boss 战 | 本月项目：学什么、做什么 |
| 每日任务 | 明天锁进日程的 2–3 件，上限 3 件 |
| 规则 | 约束：什么不愿意牺牲 |

之后 30 天只查一件事：每日任务做没做。断一天不算失败，连断三天才回头改身份陈述。30 天后重跑协议，对比两张卡。

## 核心设计：教练，不是答案机

原文原话：*"Do not attempt to outsource this contemplation to AI."*

所以这个 skill 的第一铁律是 **AI 不代答**。AI 只做四件事：提问、追问（"再看一眼，真是这样吗？"）、计时记录、晚上帮你合成。所有挖掘题的答案必须你自己写——别人替写的答案会失效，协议的全部效果来自你写出真话。

## 安装

**Claude Code / ZCode**（任选其一）：

```bash
# 方式一：装到当前项目
git clone --depth 1 https://github.com/zengziyu1312007-rgb/one-day-reset.git .claude/skills/one-day-reset

# 方式二：装到全局（所有项目可用）
git clone --depth 1 https://github.com/zengziyu1312007-rgb/one-day-reset.git ~/.claude/skills/one-day-reset
```

手动安装也可以：把 `SKILL.md` 放进 `.claude/skills/one-day-reset/`，`references/` 随行。

**触发方式**：对 AI 说「带我重置人生」「我立了 flag 总坚持不下去」「用那篇 Dan Koe 的文章带我跑一遍」即可命中；直接念 SKILL.md 里的触发词也行。

## 关于这篇文章的流传争议与核实

这篇长文在中文互联网传开后有几处说法不一，本仓库做了核实：

1. **「阅读量 1.7 亿」** ——核实成立：流传的推文截图显示该推浏览量 173M（约 1.73 亿），1.7 亿是四舍五入的说法；Substack 侧另有 8000+ 赞、1600+ 转发。
2. **「斯坦福福格在《微习惯》里讲一致性原理」** ——张冠李戴。《微习惯》作者是 Stephen Guise，福格写的是《Tiny Habits》，原文通篇没引福格。原文真实引用：Alfred Adler、Maxwell Maltz、Naval Ravikant、Mihaly Csikszentmihalyi。
3. **「原文就三个核心」** ——三点是中文博主的提炼。原文结构是 7 节＋一天协议，本 skill 按原文完整协议蒸馏。

## 免责声明

这是一个自我梳理工具，不构成医疗或心理治疗建议。如果你正处在急性心理危机（包括自杀念头），请先拨打你所在地的心理援助热线（中国大陆 12356），这个协议不能替代专业帮助。

## 版权与署名

- 原文《How to fix your entire life in 1 day》版权归 **Dan Koe** 所有，本仓库不收录原文全文，只提供链接与中文蒸馏改编；引用请注明出处并附原文链接。
- 本仓库原创内容（SKILL.md 中文协议、README）以 [CC BY 4.0](LICENSE) 提供，署名「Peter 玩 AI」并链接本仓库即可。
