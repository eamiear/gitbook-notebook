# 插件

GitBook 通过插件可以附加更多能力，所有插件可以从[`https://plugins.gitbook.com/`](tps://plugins.gitbook.com/ )获取。

**注意** 新版GitBook对插件系统做了调整

### 安装插件

插件先在`book.json`文件中进行配置：

```json
{
    "plugins": [ 
        "-search",
        "search-pro",
        "advanced-emoji",
        "emphasize",
        "include-codeblock",
        "ace",
        "splitter",
        "favicon",
        "expandable-chapters-small",
        "sitemap-general",
        "tbfed-pagefooter"
    ],
    "pluginsConfig": {
        "tbfed-pagefooter": {
            "copyright":"Copyright © eamiear",
            "modify_label": "该文件修订时间：",
            "modify_format": "YYYY-MM-DD HH:mm:ss"
        },
        "sitemap-general": {
            "prefix": "https://eamiear.gitbooks.io"
        },
        "favicon": {
            "shortcut": "assets/images/favicon.ico",
            "bookmark": "assets/images/favicon.ico",
            "appleTouch": "assets/images/apple-touch-icon.png"
        },
        "include-codeblock": {
            "template": "ace",
            "theme": "monokai"
        }
    }
}
```

配置完后，通过命令进行安装：

```shell
gitbook install
```

### 样式插件

### 功能插件

### 统计插件