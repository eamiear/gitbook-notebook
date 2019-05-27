# 配置

GitBook 通过 `book.json` 文件进行自定义配置。

### 常规配置

| 变量 | 描述 |
| -------- | ----------- |
| `root` | 包含所有图书文件的根目录路径, `book.json` 除外|
| `structure` | 定义 `Readme`, `Summary`, `Glossary` 路径. |
| `title` | 图书标题，默认从README.md中提取. |
| `description` | 图书简介，默认从README中提取 |
| `author` | 图书作者 |
| `isbn` | 图书 ISBN |
| `language` | 图书语言 |
| `direction` | 文本方向( `rtl` 或 `ltr`), 默认由图书语言决定 |
| `gitbook` | `gitbook`  |

### 插件

| 变量 | 描述 |
| -------- | ----------- |
| `plugins` | 插件列表 |
| `pluginsConfig` |插件配置 |

### 结构

除根(root)变量外，可以指定`Readme`, `Summary`， `Glossary`, `languages`的文件名称，以修改GitBook默认文件名。这些文件需要放在图书根目录下。

| 变量 | 描述 |
| -------- | ----------- |
| `structure.readme` | Readme文件名 (默认是 `README.md`) |
| `structure.summary` | Summary文件名 (默认`SUMMARY.md`) |
| `structure.glossary` | Glossary文件名 (默认 `GLOSSARY.md`) |
| `structure.languages` | Languages文件名 (默认 `LANGS.md`) |