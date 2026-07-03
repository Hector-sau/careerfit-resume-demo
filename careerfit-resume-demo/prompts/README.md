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

## 当前完成情况

- [x] `01-jd-parser.md`
- [x] `02-fit-analysis.md`
- [x] `03-resume-diagnosis.md`
- [x] `04-resume-rewrite.md`
- [x] `05-project-suggestion.md`
- [x] `06-career-advice.md`
- [x] `07-feedback-refine.md`

## Prompt 设计原则

- 要求模型先提取信息，再给建议。
- 输出尽量表格化，方便用户理解。
- 明确禁止编造用户没有提供的经历。
- 对不确定内容标注“需要用户补充”。
- 对匹配度评分给出理由，而不是只给数字。
