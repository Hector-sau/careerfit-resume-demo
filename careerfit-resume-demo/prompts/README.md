# Prompts

这里存放本项目的核心 Prompt。

## 计划中的 Prompt 模块

1. `01-jd-parser.md`
   - 作用：提取 JD 中的岗位职责、必备技能、加分项和关键词。

2. `02-fit-analysis.md`
   - 作用：根据用户背景和 JD 生成匹配度、优势、短板和风险点。

3. `03-resume-diagnosis.md`
   - 作用：分析用户原始简历表达中存在的问题。

4. `04-resume-rewrite.md`
   - 作用：在不编造经历的前提下，把用户经历改写成更贴近岗位的简历表达。

5. `05-project-suggestion.md`
   - 作用：根据能力差距推荐可补齐的练手项目。

6. `06-career-advice.md`
   - 作用：在简历优化完成后，单独生成 JD 匹配建议、候选补齐项目、信息来源和面试准备。

7. `07-feedback-refine.md`
   - 作用：当用户对任意 AI 工具生成的结果不满意时，把用户勾选/描述的问题类型翻译成具体修正指令，生成一份带原始 JD、原始背景和上一次输出的调整 Prompt。网页表单版（`index.html`）第 4 步是这个 Prompt 的可视化实现。

8. `08-greeting-cover-letter.md`
   - 作用：基于 JD 和真实经历生成 Boss 直聘/实习僧风格打招呼语（3 版）和邮件求职信（2 版），每个版本标注引用经历并附真实性检查。借鉴 Resume-Matcher / JadeAI 的 Cover Letter 功能，针对国内平台场景调整。网页表单版第 5 步"进阶工具"提供一键拼装。

9. `09-interview-prep.md`
   - 作用：基于 JD 和优化后简历表达预测高概率面试问题（标注推导来源和风险等级），并提供"一次一题"的模拟面试模板。借鉴 JadeAI 的 JD-based interview simulation，保持纯 Prompt 形态。网页表单版第 5 步提供问题预测的一键拼装。

10. `10-multi-jd-compare.md`
    - 作用：一份真实背景对比 2-3 个 JD，输出岗位要求对比表、匹配度排序（带依据）、投递策略和每个岗位的简历调整点。Resume-Matcher 的 roadmap 功能，本项目用纯 Prompt 先行实现。网页表单版第 5 步支持粘贴额外 JD 一键拼装。

11. `11-interview-review.md`
    - 作用：面试后把被问的问题记成流水账，生成逐题复盘（区分内容/表达/疑似夸大）、短板补齐动作、追问预测更新和下次面试检查清单。与 09 面试预测形成"预测 → 实战 → 复盘"闭环。网页表单版第 5 步提供一键拼装。

## 当前完成情况

- [x] `01-jd-parser.md`
- [x] `02-fit-analysis.md`
- [x] `03-resume-diagnosis.md`
- [x] `04-resume-rewrite.md`
- [x] `05-project-suggestion.md`
- [x] `06-career-advice.md`
- [x] `07-feedback-refine.md`
- [x] `08-greeting-cover-letter.md`
- [x] `09-interview-prep.md`
- [x] `10-multi-jd-compare.md`
- [x] `11-interview-review.md`

## Prompt 设计原则

- 要求模型先提取信息，再给建议。
- 输出尽量表格化，方便用户理解。
- 明确禁止编造用户没有提供的经历。
- 对不确定内容标注“需要用户补充”。
- 对匹配度评分给出理由，而不是只给数字。
