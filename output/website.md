# 静态站点

有两种方式生成静态站点

### 本地编辑预览

```bash
 gitbook serve ./{book_name}
```

在图书编写的过程中，可用该模式进行实时预览。 GitBook 在图书目录下解析生成一个 _book 目录，并监听4000端口，实时感知文件变化并更新。

下面在 `gitbook-notebook` 图书目录下，执行 `gitbook serve`

```bash
>gitbook serve
Live reload server started on port: 35729
Press CTRL+C to quit ...

info: 7 plugins are installed
info: loading plugin "livereload"... OK
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 15 pages
info: found 17 asset files
info: >> generation finished with success in 1.2s !

Starting server ...
Serving book on http://localhost:4000

```

打开浏览器，输入`http://localhost:4000`查看站点

![website](snapshot/website.png)

### 构建输出

```bash
GitBook build {resource} {destination}

```

如将 `gitbook-notebook` 构建存放到 `gitbook-notebook/docs` 目录下：

```bash
>gitbook build . ./docs
info: 7 plugins are installed
info: 6 explicitly listed
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 15 pages
info: found 18 asset files
info: >> generation finished with success in 2.7s !
```

命令执行结束后，`gitbook-notebook` 目录下会生成一个 `docs` 目录，里面的内容即为解析生成的静态站点