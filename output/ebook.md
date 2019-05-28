# 输出电子书

输出电子书（`pdf`、`ePub`、`mobi`）依赖 `ebook-convert`，需要安装 [Calibre 应用](https://calibre-ebook.com/download)

### window

下载安装`calibre-64bit-3.42.0.msi`，并将`calibre`安装目录下的`ebook-convert`路径添加到**环境变量 --> 系统变量**的`PATH`路径中。

如 `calibre` 安装在 `D://Calibre/` 目录，则将 `D://Calibre/ebook-convert`添加系统`PATH`变量中

```shell
> ebook-convert
用法: ebook-convert.exe input_file output_file [options]
```

### 生成PDF

使用下面命令生成PDF文件

```shell
gitbook pdf {resource} {file}

gitbook pdf ./ ./mybook.pdf
```

`{resource}` 资源路径可以相对路径或绝对路径
`{file}` 生成文件路径

```shell
gitbook-notebook>gitbook pdf
info: 7 plugins are installed
info: 6 explicitly listed
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 15 pages
info: found 19 asset files
info: >> generation finished with success in 8.1s !
info: >> 1 file(s) generated
```

### 生成ePub

```shell
gitbook-notebook>gitbook epub . ./myBook.epub
info: 7 plugins are installed
info: 6 explicitly listed
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 15 pages
info: found 20 asset files
info: >> generation finished with success in 3.5s !
info: >> 1 file(s) generated
```

### 生成mobi

```shell
gitbook-notebook>gitbook mobi .
info: 7 plugins are installed
info: 6 explicitly listed
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 15 pages
info: found 21 asset files
info: >> generation finished with success in 4.3s !
info: >> 1 file(s) generated
```