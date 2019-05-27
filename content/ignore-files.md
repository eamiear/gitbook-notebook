# 忽略文件

GitBook读取并排除 `.gitignore`, `.bookignore` 和 `.ignore` 文件中列举的文件或文件夹，格式与 `.gitignore` 一致。

```markdown
# This is a comment

# Ignore the file test.md
test.md

# Ignore everything in the directory "bin"
bin/*
```