# 快速开始

这个工具包有三种用法：

1. 网页版（推荐）：打开 `index.html`，填表单自动生成 Prompt，复制去任意 AI 使用。
2. 简单版：复制一个 Prompt，粘贴到 ChatGPT / Claude / 豆包 / Kimi 直接用。
3. 完整版：从 GitHub 下载整个工具包，按岗位方向使用不同模板和 Demo。

## 方式零：网页版（最省事，不熟悉 GitHub 也能用）

打开 `index.html`（部署到 GitHub Pages 后可以直接用链接打开，本地也能直接双击打开）。

使用步骤：

1. 填目标岗位 JD 和你的真实经历
2. 点"生成 Prompt"
3. 点"复制 Prompt"
4. 粘贴到你平时用的任意 AI（豆包、千问、DeepSeek、ChatGPT、Claude、Kimi 都可以）
5. 如果对生成结果不满意，把内容粘回网页第 4 步，勾选哪里不满意，会生成一份调整 Prompt，复制回去继续用
6. 进阶：第 5 步可以一键生成打招呼语/求职信、面试问题预测、多 JD 对比 Prompt；第 6 步可以把优化后的简历排版成打印页，浏览器"打印 → 存为 PDF"导出

全程在你的浏览器本地完成，不上传任何数据（草稿只自动保存在你自己的浏览器里，可一键清除）。完整图文说明见 `docs/user-guide.md`。

## 方式一：简单版

适合第一次使用的人、不会看 GitHub 的人。

使用步骤：

1. 打开 `docs/copy-paste-simple-prompt.md`
2. 复制里面的完整 Prompt
3. 打开 ChatGPT / Claude / 豆包 / Kimi
4. 粘贴 Prompt
5. 把你的目标岗位 JD 和个人经历补进去
6. 等 AI 输出简历优化报告

你会得到：

- A 部分：简历优化结果
- B 部分：JD 匹配建议
- 岗位要求提取
- 履历事项挖掘
- 优化后简历表达
- 能力差距和补齐建议
- 信息来源与判断依据

## 方式二：完整版

适合想系统优化简历、想参考多个行业 Demo、想下载到本地慢慢用的人。

使用步骤：

1. 打开 GitHub 仓库页面
2. 点击绿色 `Code` 按钮
3. 选择 `Download ZIP`
4. 解压文件
5. 打开 `README.md`
6. 根据你的目标岗位选择 `examples/` 里的 Demo
7. 根据需要复制 `prompts/` 里的 Prompt

建议使用顺序：

```text
templates/personal-background-template.md
↓
prompts/01-jd-parser.md
↓
prompts/02-fit-analysis.md
↓
prompts/03-resume-diagnosis.md
↓
prompts/04-resume-rewrite.md
↓
prompts/05-project-suggestion.md
↓
prompts/06-career-advice.md
↓（可选，对结果不满意时再用）
prompts/07-feedback-refine.md
```

## 适合谁

- 不知道简历怎么写的学生
- 看不懂 JD 的求职小白
- 想转产品、运营、数据分析、AI 相关岗位的人
- 有经历但不会包装成岗位语言的人

## 不适合谁

- 希望 AI 编造经历的人
- 希望工具保证拿 offer 的人
- 完全不愿意补充真实经历的人

## 使用原则

请记住一句话：

```text
这个工具包只帮你把真实经历说清楚，不帮你编经历。
```

补齐项目是候选建议，不是系统替你决定。默认可以按 1-3 个月规划，并根据你的时间、基础和目标岗位调整。
