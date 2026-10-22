新手Vibe Coding 快速做出一个 App，真正上线用起来，后面还有一大堆坑。代码能跑，只是开始。 做 Demo 和把一个产品长期跑下去，至少现在来看还是两回事。

中高级程序员抱怨：古法编程时代自己琢磨架构设计，研究怎么写出优雅的代码是很爽的，现在指挥AI写反倒有点枯燥。但是事实是，大部分程序员用AI写的代码也是一团糟。

到底问题出在哪里，该怎么提高AI 编程能力？

最近，TypeScript 领域的知名开发者 Matt Pocock 开源了一套 AI Skill 项目。这套项目在极短的时间内获得了超过 30 万颗星，下载量更是突破 **2900 万次**（整个 skills 仓库累计）。

其中讨论度最高的，莫过于能让 AI 反向提问、协助开发者厘清需求的 grill-me。但是这个skills只有短短5行字？？

这是一个发人深思的问题。

其实grill-me 只是一整套庞大工作流的“入口”。在过去的一年里，Matt 几乎全程依赖 AI 进行开发；而他将这段期间摸索出的系统化工作流，毫无保留地打包进了这个项目中。从最初使用 grill-me 锁定需求，到后续的规格撰写、任务拆解、代码开发、自动化测试，乃至最后的代码审查（Code Review），他把二十多年的软件工程方法论，压缩成一整套「小而模块化」的 skill 流水线（grill-me → to-spec → to-tickets → implement → Code Review → improve-codebase-architecture），用来控制 AI 的随机性。这条生产线上的每一个节点，他都安排了专属的 Skill 来严格把关。

这一切的心血，都指向同一个核心目标：将充满随机性与不确定性的 AI 黑盒子，驯服成精准、可靠且完全可控的专业生产力工具。

虽然上述的主线逻辑许多人已大致熟悉，但这套项目中真正具备高价值不是浮于skill表面，而是如何将软件工程智慧迁移至 AI 协作，**Matt Pocock 传统软件工程领域底蕴深厚，他反复提到的哲学都来自于这些经典工程经验书籍：《程序员修炼之道》《重构》《领域驱动设计》《软件设计的哲学》等，他这一年来的成就，实则是将这些成熟的工程智慧，原封不动地移植到 AI 协作上，并且整理成了 AI 可以反复执行的 Skills

具体对应如下列表

| 书籍                                               | 作者                       | 在 Skills 里怎么用                                                                                                                                               |
| ------------------------------------------------ | ------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **《程序员修炼之道》**（The Pragmatic Programmer）          | David Thomas、Andrew Hunt | 开工前追问需求、消除理解偏差；通过小步修改和及时反馈验证代码。[出处](https://github.com/mattpocock/skills#why-these-skills-exist)                                                            |
| **《领域驱动设计：软件核心复杂性应对之道》**                         | Eric Evans               | 提取“统一语言”，让业务讨论、文档和代码命名使用同一套术语，落实在 `grill-with-docs` 中。[出处](https://github.com/mattpocock/skills#2-the-agent-is-way-too-verbose)                             |
| **《解析极限编程：拥抱变化》**（Extreme Programming Explained） | Kent Beck                | 持续投入系统设计，避免 AI 快速堆出难以修改的代码。[出处](https://github.com/mattpocock/skills#4-we-built-a-ball-of-mud)                                                              |
| **《软件设计的哲学》**（A Philosophy of Software Design）   | John Ousterhout          | 深模块、简单接口，以及“设计两次”：先探索不同方案再决定接口。[出处](https://github.com/mattpocock/skills/blob/main/skills/engineering/codebase-design/DESIGN-IT-TWICE.md)                   |
| **《重构：改善既有代码的设计》**                               | Martin Fowler            | `code-review` 明确采用第 3 章的代码坏味道，包括重复代码、霰弹式修改、基本类型偏执等 12 类，作为审查线索。[出处](https://github.com/mattpocock/skills/blob/main/skills/engineering/code-review/SKILL.md) |

所以驾驭 AI 编程的天花板，肯定是工程功底。

