# 命令行概念

### 初始化

初始化一本书

```
 gitbook init

 gitbook init ./directory
```

在当前目录初始化一本书或创建一个空目录并初始化

### 本地预览

```
 gitbook serve

 gitbook serve ./{book_name}
```

本地文件修改后，实时预览文件变化

### 发布电子书

```
gitbook build

# 将书籍构建结果存放到{destination}目录下
gitbook build {resource} {destination}

gitbok build ./ --log=debug --debug
```

书籍编写完后，可构建生成静态站点。

--log=debug --debug 进入调试模式，输出更友好的堆栈错误信息