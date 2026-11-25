# Job — Distributed System

存放求职需要掌握的一致性、复制、分区、容错、共识、事务、存储与分布式系统设计原理知识点和练习笔记。

## 学习计划

- [分布式系统学习计划](Distributed-Systems-Learning-Plan.md)：结合 van Steen 与 Tanenbaum《Distributed Systems》第 4 版和 Kleppmann《Designing Data-Intensive Applications》，按主题组织的学习路线、双语讲解规则、图表规则，以及 Hadoop 与 Cassandra 贯穿案例。
- [Review Notes](notes.md)：中英双语核心结论，供快速复习。
- [Session Log](session-log.md)：每次讲解的记录和当前 checkpoint。
- [Mastery](mastery.md)：评估证据。
- [Session Log 归档（2026-11）](session-log-archive-2026-11.md)：旧计划下的讲解记录，只作背景。

### Review Notes 使用说明 / Review Notes Guide

`notes.md` 只保留每个知识点最重要的结论，采用中英双语，便于理解概念并练习专业英语表达。完整讲解过程记录在 Session Log，掌握度与评估证据记录在 Mastery。

- 每次完成一个知识点后，补充该知识点的核心结论；不复述课堂过程。
- 每条结论先中文、后英文，保留关键英文术语；不在笔记中标注教材出处。
- 只记录必要的关键机制或限制；避免冗长解释、重复例子和大段问答。
- 教材结论与自拟工程案例要明确区分；案例仅在确实有助于理解时保留。
- 默认每个知识点控制在约 3–7 条核心结论；若一个结论已足够，不为凑数量而扩写。

`notes.md` is a concise bilingual reference containing only the essential takeaways. Lesson details belong in Session Log; mastery and assessment evidence belong in Mastery.

从 [instructions/router.md](instructions/router.md) 查找学习、复习与测试指令。优先链接已有 [CS 资料](../CS/README.md)，新专题笔记可直接放在本目录；不自动复制或迁移旧资料。模拟面试及答题表现走 [interview](../interview/README.md)。返回 [Job](../README.md)。

## 教材 PDF 读取记录

以下信息于 2026-11-24（America/New_York）验证，供跨会话查阅。开始需要教材原文或图表的任务时，先检查此记录中的路径，再实际打开文件；不能仅凭旧对话断言 PDF 无法读取。

- 教材：Maarten van Steen、Andrew S. Tanenbaum，*Distributed Systems*，4th Edition，Version 02（DS 4.02）。
- 文件名：`02-Distributed-Systems-Maarten-van-Steen-Andrew-Tanenbaum.pdf`。
- 最近验证可读的位置：`/workspace/scratch/ecf9a195a3ac/project_sources/02-Distributed-Systems-Maarten-van-Steen-Andrew-Tanenbaum.pdf`。
- 此位置属于临时运行环境，不是永久文件地址。若路径不存在，使用 `rg --files` 在当前可访问的工作目录中按上述文件名查找，再检查可访问的项目附件或文件来源；仍找不到时，说明具体查找结果并请求教材来源。
- 已验证：共 685 个 PDF 页面；Figure 1.3 位于 PDF 第 28 页（Python 索引 27），对应印刷页 12。其他页码应逐页核实，不假定全书偏移恒定。
- 读取工具：Python 的 PyMuPDF（`fitz`）。以下代码提取对应页文字；`page.get_pixmap()` 可渲染原页，必要时用 `clip` 裁剪图表。引用教材图表时展示原图；只有实际无法获取原图时才使用明确标注的重绘图，并说明原因。

```python
from pathlib import Path
import fitz

pdf = Path("/workspace/scratch/ecf9a195a3ac/project_sources/02-Distributed-Systems-Maarten-van-Steen-Andrew-Tanenbaum.pdf")
if not pdf.is_file():
    raise FileNotFoundError("已记录的临时路径失效；请重新查找教材 PDF。")

with fitz.open(pdf) as doc:
    print("PDF 页数：", len(doc))
    page = doc[27]  # PDF 第 28 页；已核对为印刷页 12
    print(page.get_text())
```

本记录只保存定位和读取方法，不代表教材 PDF 已永久备份，也不改变学习进度或掌握度。
