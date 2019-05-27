# 目录结构

GitBook 目录结构比较简单，所有 Markdown 文件罗列在 SUMMARY 文件，最终转换成 HTML 文件

GitBook 基本结构：

```
.
├── book.json
├── README.md
├── SUMMARY.md
├── chapter-1/
|   ├── README.md
|   └── something.md
└── chapter-2/
    ├── README.md
    └── something.md
```

文件概述：

| 文件 | 描述 |
| -------- | ----------- |
| `book.json` | 文件配置(__optional__) |
| `README.md` | 图书简介 (**required**) |
| `SUMMARY.md` | 内容 (__optional__) |
| `GLOSSARY.md` | 要注释的术语列表 (__optional__) |