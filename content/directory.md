# 目录 SUMMARY

`SUMMARY.md` 用来定义章节或子章节目录结构，并用于生成图书目录。

`SUMMARY.md` 是一组链接列表，链接标题为章节标题，链接路径指向章节文件。

嵌套链接列表即为在父章节下创建子章节。

### 多级目录

```markdown
# Summary

* [Introduction](README.md)

* [安装](installation/README.md)
    * [安装 Node.js](installation/nodejs-install.md)
    * [安装Gitbook命令行](installation/gitbook-install.md)
    * [Gitbook命令概览](installation/gitbook-cli.md)
```

**注意**： 如果一级目录的链接为空，表现结果为不可点击。

### 部分

章节目录可以通过标题或者水平分割线划分成不同的部分，即为一组章节

```markdown
# Summary

### Part I

* [Writing is nice](part1/writing.md)
* [GitBook is nice](part1/gitbook.md)

### Part II

* [We love feedback](part2/feedback_please.md)
* [Better tools for authors](part2/better_tools.md)

----

* [Last part without title](part3/title.md)
```

### 锚点

目录中的章节可以通过锚点指向文章特殊部分。

```markdown
# Summary

### Part I

* [Part I](part1/README.md)
    * [Writing is nice](part1/README.md#writing)
    * [GitBook is nice](part1/README.md#gitbook)
* [Part II](part2/README.md)
    * [We love feedback](part2/README.md#feedback)
    * [Better tools for authors](part2/README.md#tools)
```