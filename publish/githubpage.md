# 发布到GitHub Pages

编写完的图书可以发布到GitHub Pages服务。

### 手动将静态站点资源发布到GitHub Pages

* 每次编辑提交图书文件(`Markdown`)前，构建生成静态站点文件到`./docs`目录，并将`./docs`目录提交到GitHub。

* 在GitHub平台上，项目面板中找到 `Settings` --> `GitHub Pages`，选择`GitHub Pages`资源来源 `master branch /docs folder`，这里将 `/docs`目录作为 `GitHub Pages` 资源。

缺点是每次提交都要手动构建生成静态站点。

### Travis CI 自动发布到GitHub Pages

在使用 `Travis CI` 自动发布时，需先在Travis平台注册关联GitHub账户，并在[仓库列表](https://travis-ci.org/account/repositories)中选择目标项目并启动持续集成服务。

在GitHub项目中创建`.travis.yml`文件，并填写相关脚本，细节查看 [**`GitHub Pages Deployment`**](https://docs.travis-ci.com/user/deployment/pages/)

示例：

```yml
language: node_js

node_js:
  - "10"

# 缓存依赖
cache:
  directories:
    - $HOME/.npm

before_install:
  - export TZ='Asia/Shanghai' # 更改时区

# 依赖安装
install:
  - npm install gitbook-cli -g
  # 安装 gitbook 插件
  - gitbook install

# 构建脚本
script:
    # 自定义输出目录 gitbook build src dest
  - gitbook build . ./docs
  # - gitbook build . ./build/$CUSTOM_PATH

# 分支白名单
branches:
  only:
    - master # 只对 master 分支进行构建

# GitHub Pages 部署
deploy:
  provider: pages
  skip_cleanup: true
  # 在项目仪表盘的 Settings -> Environment Variables 中配置
  github_token: $GITHUB_TOKEN
  # 将 build 目录下的内容推送到默认的 gh-pages 分支上，并不会连带 build 目录一起
  local_dir: ./docs/
  #fqdn: $CUSTOM_DOMAIN
  name: $GIT_NAME
  email: $GIT_EMAIL
  on:
    branch: master
```

配置完后，每次提交文件到GitHub服务，`Travis`会自动发布到`GitHub Pages`