# GitHub 发布说明与对照检查

本包只在本地准备，没有替作者创建远程仓库、上传或公开发布。

## 三页主入口是否足够？

足够：README 给人读，SKILL 给模型读，EMOTIONAL_BOUNDARIES 说明判断与评审规则。Markdown 没有固定纸张页长；这里的“一页”指一个文档入口，而不是强行缩到一张 A4。案例、来源和测试作为附录，不塞满首页。

```text
before-i-spiral/
├── README.md                  五部分介绍与零技术入口
├── SKILL.md                   模型侧主指令
├── EMOTIONAL_BOUNDARIES.md     模式、触发证据、例外、指标
├── START_HERE.md               可直接复制到聊天的自包含版
├── LICENSE.md                 非商业分享与改编许可
├── CONTRIBUTING.md            反馈与隐私边界
├── agents/openai.yaml         可选宿主显示元数据
├── references/                思想来源与合成示例
├── tests/                     测试情境、评审与实际记录
└── docs/PUBLISHING.md          本文
```

## 看过哪些项目，学什么、不学什么

调研日期：2026-10-19 至 2026-10-20。选取有代表性的项目，不是对 GitHub 全站热度的完整排名；不以星数证明质量、安全或疗效。

| 来源 | 可借鉴之处 | 本项目的处理 |
| --- | --- | --- |
| [Agent Skills 规范](https://agentskills.io/specification) | 文件夹、name/description、按需加载引用 | 根目录 SKILL 与清晰触发描述，内容分层 |
| [anthropics/skills](https://github.com/anthropics/skills) | 独立技能目录、示例、使用说明与测试提醒 | 一个完整可移植目录，声明宿主差异，不冒充全平台已验证 |
| [obra/superpowers](https://github.com/obra/superpowers) 与其 [tests](https://github.com/obra/superpowers/tree/main/tests) | 按宿主说明安装，维护行为与回归检查 | 区分聊天试用／技能安装，增加反例和多轮场景；不搬入复杂编码流程 |
| [relationship-ququ-skill](https://github.com/Aubrey0806/relationship-ququ-skill) | 把心智模型、决策规则、表达方式显式化 | 学结构，不照搬“绝对确定”、资产化或矮化用户的价值观／语气 |

仅参考公开的结构与理念，没有复制这些仓库的提示词正文，因此本项目的非商业许可不声称覆盖外部作品。

## 比旧版补了什么

- 将五步流程与佛教启发映射到具体行为，而非仅列几句口号。
- 增加比较、公平、合理标准与不现实要求的区分。
- 用可观察线索取代虚构情绪指数；时间未知、夜班、拒绝暂停和新信息都有分支。
- 明确安全优先于字数／劝睡，危险词不是一键拒聊规则。
- 增加来源边界、非商业授权、零技术试用与隐私友好的反馈方式。
- 给出评审指标和实际测试记录，不把模板／静态检查说成行为验证。

## 作者如何上传（不需要命令行）

1. 解压交付 ZIP，打开里面的 `before-i-spiral` 文件夹。
2. 登录自己的 GitHub，创建名为 `before-i-spiral` 的仓库。第一次建议先设为 Private，核对完再决定公开。
3. 不自动生成另一个 README 或 MIT 许可证；本包已经包含简介与非商业授权说明。
4. 在仓库的文件上传入口，把文件夹内部的文件和子文件夹整体上传，让 README.md 与 SKILL.md 位于仓库根目录。不要只上传 ZIP，也不要多包一层同名目录。
5. 检查 README 正常显示、文件链接可打开、LICENSE 与测试状态清楚，再确认提交。
6. 需要别人一键下载时，可在 GitHub Releases 创建标记为 `v1.1.0` 的版本并附 ZIP；未完成专业安全审查与更广泛模型测试时，不宣称稳定治疗产品。

GitHub 网页的按钮名称可能变化，官方步骤见 [创建仓库](https://docs.github.com/en/get-started/start-your-journey/creating-a-repository-for-your-project-on-github)与[上传文件](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)。这些步骤不是已经执行的动作。

## 公开前逐项确认

- [ ] 署名 Eva、创作者经历与 Dana 的致谢符合作者公开意愿；致谢不被理解为背书。
- [ ] 理解 CC BY-NC 4.0：允许非商业修改／分享，不授予商用；已有合法许可通常不可追溯撤销。
- [ ] 仓库没有真实咨询记录、个人路径、密钥或可识别的第三方故事。
- [ ] 根据目标平台真实运行多轮测试；不能只看演示例句。
- [ ] 有资质的心理健康／危机支持人员审阅边界和当地资源策略。
- [ ] 如收集用户反馈，明确最小收集、保存、删除与私密报告方式；默认不收集真实聊天。
- [ ] 不宣称本包已上架任何技能商店或能够跨平台自动安装。

提示词只能影响回应，不保证模型总是遵守。若日后开发独立应用，时间、状态、权限、资源查询和安全评估都需要真实实现，不能仅在 Markdown 里写 IF 就当作已部署。
