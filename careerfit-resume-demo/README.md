# CareerFit Resume Demo

一个面向求职小白的 JD 驱动型简历优化 Prompt 工具包。

用户只需要粘贴目标岗位 JD 和个人真实经历，就可以在 ChatGPT、Claude、豆包、Kimi 等 AI 工具中生成一份结构化求职分析报告：先看懂岗位要求，再挖掘个人履历，最后输出可用于简历的优化表达和单独的求职建议。

![CareerFit Resume Demo 效果示意图](assets/careerfit-effect.png)

## 这个项目能做什么

CareerFit Resume Demo 不是一个泛泛的 Prompt 合集，而是一个围绕“JD 分析 -> 履历挖掘 -> 简历优化 -> 求职建议”的小型产品 Demo。

它可以帮助用户完成：

- **看懂 JD**：提取岗位职责、必备技能、加分项、软技能和简历关键词。
- **挖掘履历**：把用户提供的实习、课程项目、社团、内容运营、AI 工具使用等经历，映射到岗位要求。
- **优化简历表达**：输出保守版和增强版简历表达，区分“可以直接写”和“需要补证据后再写”。
- **判断岗位匹配度**：按核心技能、经历相关度、工具能力、表达协作、学习潜力给出评分和依据。
- **给出求职建议**：单独输出是否建议投递、当前短板、相邻岗位、1-3 个月候选补齐项目。
- **控制真实性风险**：明确禁止编造经历，不把“建议做的事”写成“已经做过的事”。
- **标注建议来源**：说明每条关键建议来自 JD、用户履历、优化后简历还是通用求职判断。
- **支持反馈调整**：如果对任意 AI（豆包、千问、DeepSeek、ChatGPT 等）生成的结果不满意，可以把内容和不满意的地方粘回网页表单，生成一份带具体修正要求的调整 Prompt，不需要重新描述一遍需求。

## 为什么做这个项目

很多学生和转方向求职者并不是完全没有经历，而是卡在三个地方：

- 看完 JD 以后，不知道岗位到底在筛什么能力。
- 有课程、社团、内容、实习或 AI 工具使用经历，但不会写成 HR 能看懂的简历语言。
- 用 AI 改简历时，容易出现夸大、编造、把建议写成事实的问题。

所以这个项目把输出拆成两部分：

- **A. 简历优化结果**：只基于真实经历，生成可以进入简历的表达。
- **B. 求职建议**：单独说明能力差距、项目补齐和投递建议，不混进简历正文。

这个拆分是项目的核心设计原则。

## 目标用户

- 想投实习但看不懂 JD 的学生
- 想转向 AI 产品、运营、数据分析等岗位的小白
- 有经历但不会写成简历语言的求职者
- 想用 AI 辅助简历优化，但担心内容被编造的人

## 核心原则

- 不编造经历，只优化真实经历的表达方式。
- 不承诺 offer，只提供求职判断和简历改进参考。
- 先用 Prompt 工具包验证需求，再考虑网页化。
- 每个 Demo 都保留失败案例和迭代记录。

## 输出示例

用户输入：

```text
1. 目标岗位 JD
2. 个人真实经历
```

工具输出：

```text
A. 简历优化结果
- 岗位要求提取
- 履历事项挖掘
- 匹配度判断
- 简历问题诊断
- 保守版简历表达
- 增强版简历表达
- 真实性检查

B. 求职建议
- 是否建议投递
- 更适合的相邻岗位
- 当前能力短板
- 1-3 个月候选补齐项目
- 面试风险提醒
- 信息来源与判断依据
```

![CareerFit Resume Demo 输出结构示例](assets/careerfit-output-example.png)

上图是输出结构的示意图，不是真实用户简历或真实 AI 对话截图。完整的真实文字示例见 `examples/` 目录下的 8 个行业 Demo。

## 项目完成度

当前版本已经包含：

- 7 个核心 Prompt 模块（含反馈调整 Prompt）
- 1 个小白可直接复制的整合版 Prompt
- 1 个纯前端网页表单版（index.html，v2，不接 API，支持根据用户反馈生成调整 Prompt）
- 8 个完整行业 Demo，覆盖全部 8 个岗位方向
- 10 份公开 JD 测试记录，覆盖全部 8 个岗位方向
- 5 个 JD 模拟跑通记录
- 评测方法、4 个真实失败案例记录、信息来源说明和分发说明
- MIT License

## 作为作品集展示了什么

这个仓库也用于展示一个 AI 产品 Demo 从 0 到 1 的设计过程：

- **用户洞察**：从“不会写简历”拆解到“看不懂 JD、不会挖掘经历、担心 AI 编造”三个具体问题。
- **Prompt Workflow**：把任务拆成 JD 解析、匹配分析、简历诊断、简历改写、项目建议、求职建议、反馈调整 7 个模块，形成一个可以迭代的闭环而不是一次性生成。
- **结构化输出**：用表格、评分维度、A/B 分区降低用户理解成本。
- **评测意识**：用公开 JD 测试集、模拟跑通记录、真实失败案例记录效果。
- **产品边界**：明确不编造经历、不承诺 offer、不收集用户隐私。
- **分发思路**：先用 GitHub Prompt 工具包验证需求，再考虑网页表单或 API 版本。

相近项目分析见 `docs/github-competitive-analysis.md`。

## 首批 Demo 方向

1. AI/大模型产品实习
2. 互联网产品/运营
3. 数据分析
4. 新媒体/内容运营
5. 电商运营
6. 市场/品牌营销
7. 金融/商业分析
8. HR/行政/管培生

## 使用方式

### 网页版（推荐，尤其适合小红书用户）

打开 `index.html`（部署在 GitHub Pages 后可以直接用链接访问），在表单里填 JD 和个人背景，点击"生成 Prompt"，网页会在你的浏览器本地把内容拼进完整 Prompt 模板，点"复制 Prompt"后自己粘贴到 ChatGPT / Claude / 豆包 / Kimi 使用。

纯前端实现，不接任何模型 API，也不上传或保存任何数据，比手动找文件复制粘贴更省事。详见"网页表单版说明"。

### 简单版

适合想直接用纯文本 Prompt、不想用网页的人。

1. 打开 `docs/copy-paste-simple-prompt.md`
2. 复制完整 Prompt
3. 粘贴到 ChatGPT / Claude / 豆包 / Kimi
4. 补充目标岗位 JD 和个人经历
5. 生成简历优化报告

### 完整版

适合想系统优化简历的人。

1. 复制 `templates/personal-background-template.md`，填写个人背景。
2. 粘贴目标岗位 JD。
3. 按顺序使用 `prompts/` 中的 6 个核心 Prompt，对结果不满意时再用第 7 个反馈调整 Prompt。
4. 参考 `examples/` 中的行业 Demo。
5. 根据输出结果优化简历和项目计划。

更多说明见 `QUICKSTART.md`、`docs/information-sources-and-user-hooks.md` 和 `docs/distribution-notes.md`。

## 网页表单版说明

`index.html` 是这个工具包的 v2 形态：一个单文件静态网页，不依赖任何后端和模型 API。

它做的事情很简单：把 `docs/copy-paste-simple-prompt.md` 里那份固定的 Prompt 文本，用 JavaScript 在你的浏览器里拼上你填的 JD 和个人背景，生成结果后你自己复制去 ChatGPT / Claude / 豆包 / Kimi 用。所有数据处理都在浏览器本地完成，刷新页面后不会留下任何记录，服务器也不会收到你填的内容。

做这个的原因：纯文本 Prompt 对小红书这类"图省事"的用户门槛偏高，要先找到文件、再手动把 JD 和经历分别填进模板空白处；网页表单把这一步简化成"填表单 + 点按钮"，转化率会更高，但仍然坚持不接 API、不产生成本、不碰用户隐私的原则。

网页第 4 步是"反馈调整"功能：用户不管用的是哪个 AI，只要把生成结果和不满意的地方（勾选或自己描述）贴回来，网页会结合上面已经填好的 JD 和背景，生成一份带具体修正指令的调整 Prompt，用户复制回原对话或新对话继续用，不需要重新描述一遍背景。这个功能同样是纯前端模板拼装，没有接入任何模型 API 去"理解"用户的不满，问题类型是用户自己勾选的，工具只负责把勾选翻译成结构化的修正要求。对应的 Prompt 设计文档见 `prompts/07-feedback-refine.md`。

部署到 GitHub Pages（免费）：

1. 仓库发布到 GitHub 后，进入 `Settings -> Pages`。
2. `Source` 选择 `Deploy from a branch`，分支选 `main`，目录选 `/ (root)`。
3. 保存后几分钟内会生成一个 `https://你的用户名.github.io/仓库名/` 的访问链接。
4. 把这个链接放进小红书正文或评论区，用户点开就能直接填表单，不需要下载或懂代码。

本地也可以直接双击打开 `index.html` 预览效果，不需要任何安装或构建步骤。

## 仓库结构

```text
careerfit-resume-demo/
├── LICENSE
├── README.md
├── QUICKSTART.md
├── index.html
├── roadmap.md
├── assets/
│   ├── careerfit-effect.png
│   └── careerfit-output-example.png
├── docs/
│   ├── product-brief.md
│   ├── evaluation-method.md
│   ├── failure-cases.md
│   ├── copy-paste-simple-prompt.md
│   ├── github-competitive-analysis.md
│   ├── information-sources-and-user-hooks.md
│   ├── distribution-notes.md
│   ├── jd-test-set.md
│   └── simulation-5-jds.md
├── examples/
│   ├── README.md
│   ├── ai-product-intern.md
│   ├── data-analyst.md
│   ├── content-ops.md
│   ├── internet-product-ops.md
│   ├── ecommerce-ops.md
│   ├── marketing-branding.md
│   ├── business-analysis.md
│   └── hr-management-trainee.md
├── prompts/
│   ├── README.md
│   ├── 01-jd-parser.md
│   ├── 02-fit-analysis.md
│   ├── 03-resume-diagnosis.md
│   ├── 04-resume-rewrite.md
│   ├── 05-project-suggestion.md
│   ├── 06-career-advice.md
│   └── 07-feedback-refine.md
└── templates/
    ├── jd-demo-template.md
    └── personal-background-template.md
```

## 当前状态

项目处于 MVP 发布前整理阶段。

已完成：

- 项目定位
- 文件结构
- 首批 8 个岗位方向
- 模板和评测文档骨架
- 7 个核心 Prompt（新增反馈调整 Prompt，见 prompts/07-feedback-refine.md）
- 8 个完整行业 Demo：AI/大模型产品实习、数据分析、新媒体/内容运营、互联网产品/运营、电商运营、市场/品牌营销、金融/商业分析、HR/行政/管培生
- 10 份公开 JD 测试记录，覆盖全部 8 个岗位方向
- 5 个 JD 模拟测试样例
- 4 个真实失败案例记录（docs/failure-cases.md）
- 展示 A/B 输出结构的效果图（assets/careerfit-output-example.png）
- 纯前端网页表单版 index.html（v2，不接模型 API，本地生成 Prompt，含第 4 步反馈调整功能）
- GitHub 相近项目分析
- 信息来源与用户吸引点说明
- 分发说明
- MIT License

下一步：

- 把仓库发布到 GitHub 并开启 GitHub Pages，拿到 index.html 的正式访问链接
- 根据真实反馈继续校正 Demo 的语气和真实性
- 发布小红书第一篇，正文/评论区放网页表单链接，收集真实使用反馈
