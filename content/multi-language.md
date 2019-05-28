# 多语言

GitBook 支持构建用多种语言编写的图书，每种语言应该是一个子目录，并遵循正常的 GitBook 格式。此外，仓库根目录下需包含一个 `LANGS.md` 文件，并按照下面格式编写：

```markdown
# Languages

* [English](en/)
* [French](fr/)
* [Español](es/)
```

### 各种语言的配置

当一本语言书包含 `book.json` 文件时，它的配置会继承覆盖主配置。

但 `plugins` 插件除外，插件只能全局配置，其他语言不能进行特定配置。