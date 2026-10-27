# Neurocomputing 模板迁移说明

## 已完成

- 将原稿从 `elsarticle` 迁移到 Elsevier CAS 单栏类 `cas-sc`。
- 保留原论文的标题、摘要、正文、公式、表格、图件、附录和参考文献内容。
- 将作者、单位、通讯作者、摘要、关键词和 highlights 改为 CAS 前置信息语法。
- 参考文献改用模板附带的 `cas-model2-names.bst`，并完成 BibTeX 编译。
- 将所有论文依赖文件平铺到同一目录，避免 Editorial Manager 无法处理子目录。
- 移除旧模板中的强制浮动屏障，使图表由 CAS 版式自动排布，减少大块空白。
- 已完成 LaTeX、BibTeX 和多轮 LaTeX 编译，并逐页检查最终 PDF。

## 投稿前仍须人工确认

- 第二作者姓名。
- 通讯作者姓名和电子邮箱。
- 两个作者单位的完整信息。
- 数据来源和预处理链的原始记录。
- 伦理审查或豁免信息。
- CRediT 作者贡献。
- 利益冲突声明。
- 资金和致谢信息。
- 代码、划分文件、模型权重及逐图像预测的公开方式。

这些内容在 `main.tex` 中以红色 `TO BE CONFIRMED` 保留，未擅自补写。

## 建议上传

- `main.pdf` 作为 Manuscript。
- `Neurocomputing_submission_source.zip` 作为 LaTeX source files。
- 若投稿系统单独要求 Highlights，可再上传 `HIGHLIGHTS.txt`。

## 本地编译顺序

```text
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```
