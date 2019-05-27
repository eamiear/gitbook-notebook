# 目录

GitBook 通过 SUMMARY 文件来实现和管理目录结构，通过该文件可以实现多种目录效果：

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

### 按章节/部划分

```markdown
# Summary

### 第一回

* [Introduction](part1/README.md)

* [安装](part1/installation/README.md)
    * [安装 Node.js](part1/installation/nodejs-install.md)
    * [安装Gitbook命令行](part1/installation/gitbook-install.md)
    * [Gitbook命令概览](part1/installation/gitbook-cli.md)

### 第二回

* [安装](part2/installation/README.md)
    * [安装 Node.js](part2/installation/nodejs-install.md)
    * [安装Gitbook命令行](part2/installation/gitbook-install.md)

```