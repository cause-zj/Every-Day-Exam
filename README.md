# 每日技术问答

本仓库是「每日技术问答」的文档归档，与「架构早问答」的落盘约定对齐。这里只保存 Markdown 记录，不包含应用程序、构建脚本或可运行服务。

## 目录结构

```text
.
├── archive/                      # 每日正式归档
│   └── .gitkeep
├── templates/
│   └── daily-exam.md             # 空白模板
├── examples/
│   └── 2000-01-01.example.md     # 版式示例，不是真实归档
├── .gitignore
└── README.md
```

| 目录 | 用途 |
| --- | --- |
| `archive/` | 按日期存放已提交的每日记录 |
| `templates/` | 复制用的空白模板 |
| `examples/` | 只演示版式的假文示例 |

## 文件命名

每日记录放在 `archive/` 下，文件名使用 ISO 日期：

`archive/YYYY-MM-DD.md`

例如 `archive/2026-11-06.md`。一天一份。`examples/` 里的文件带 `.example.md` 后缀，只用于看版式，不要放进 `archive/`。

## 必需章节

每份每日文件按下面的顺序使用这三个二级标题，标题文字保持一致：

1. `## 问题`
2. `## 标准答案`
3. `## 用户回答`

「用户回答」只记录实际作答。当天还没有作答时保留这一节，留下占位即可，不要编造作答内容。

## 如何新增并提交一天的记录

1. 从模板复制到归档目录，并把文件名改成当天日期：

   ```bash
   cp templates/daily-exam.md archive/YYYY-MM-DD.md
   ```

   将 `YYYY-MM-DD` 换成当天日期，例如 `archive/2026-11-06.md`。

2. 填写三个章节：题目写入「问题」，参考答案写入「标准答案」，实际作答写入「用户回答」。

3. 提交并推送到 `main`：

   ```bash
   git add archive/YYYY-MM-DD.md
   git commit -m "archive: YYYY-MM-DD"
   git push origin main
   ```
