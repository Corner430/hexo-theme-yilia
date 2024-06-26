[demo](blog.corner430.top) : blog.corner430.top

## 1 功能

1. TOC目录
2. 返回顶部
3. 打赏
4. 搜索
5. “更好的”标签云
6. “更好的”分享
7. 解决模块缺失问题
8. 解决本地图片不显示问题
9. 增加 [不蒜子](https://ibruce.info/2015/04/04/busuanzi/)统计
  1. 显示站点总访问量
  2. 显示阅读次数
10. 增加字数统计[WordCount](https://www.npmjs.com/package/hexo-wordcount)
  1. 字数统计
  2. 阅读时长统计
  3. 总字数统计
11. 页面点击小红心
12. 文章置顶
13. 版权声明
14. 添加文章结束标志
15. 添加[宠物](https://github.com/xiazeyu/live2d-widget-models)
16. 添加[加密文章](https://github.com/D0n9X1n/hexo-blog-encrypt)
17. ~~网易云音乐~~


## 2 安装

``` bash
$ git clone https://github.com/Corner430/hexo-theme-yilia themes/yilia
```

## 3 配置

修改hexo根目录下的 `_config.yml` ： `theme: yilia`

## 4 更新

``` bash
cd themes/yilia
git pull
```

## 5 config.yml 示例

### 5.1 插件安装

```shell
npm install --save hexo-deployer-git
npm install --save hexo-generator-json-content
npm install https://github.com/EricGerry/hexo-asset-image-0.0.5.git --save
npm install hexo-wordcount --save
npm uninstall hexo-generator-index --save
npm install hexo-generator-index-pin-top --save
npm install --save hexo-helper-live2d
npm install live2d-widget-model-hijiki
npm install --save hexo-blog-encrypt
```

### 5.2 blog/_config.yml 示例

```yml
# Hexo Configuration
## Docs: https://hexo.io/docs/configuration.html
## Source: https://github.com/hexojs/hexo/

# Site
title: Hexo
subtitle: ''
description: ''
keywords:
author: Corner
language: en
timezone: ''

# URL
## Set your site url here. For example, if you use GitHub Page, set url as 'https://username.github.io/project'
url: http://corner430.github.io
permalink: :year/:month/:day/:title/
permalink_defaults:
pretty_urls:
  trailing_index: true # Set to false to remove trailing 'index.html' from permalinks
  trailing_html: true # Set to false to remove trailing '.html' from permalinks

# Directory
source_dir: source
public_dir: public
tag_dir: tags
archive_dir: archives
category_dir: categories
code_dir: downloads/code
i18n_dir: :lang
skip_render:

# Writing
new_post_name: :title.md # File name of new posts
default_layout: post
titlecase: false # Transform title into titlecase
external_link:
  enable: true # Open external links in new tab
  field: site # Apply to the whole site
  exclude: ''
filename_case: 0
render_drafts: false
post_asset_folder: true
relative_link: false
future: true
highlight:
  enable: true
  line_number: true
  auto_detect: false
  tab_replace: ''
  wrap: true
  hljs: false
prismjs:
  enable: false
  preprocess: true
  line_number: true
  tab_replace: ''

# Home page setting
# path: Root path for your blogs index page. (default = '')
# per_page: Posts displayed per page. (0 = disable pagination)
# order_by: Posts order. (Order by date descending by default)
index_generator:
  path: ''
  per_page: 10
  order_by: 
    top: -1
    date: -1

# Category & Tag
default_category: uncategorized
category_map:
tag_map:

# Metadata elements
## https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta
meta_generator: true

# Date / Time format
## Hexo uses Moment.js to parse and display date
## You can customize the date format as defined in
## http://momentjs.com/docs/#/displaying/format/
date_format: YYYY-MM-DD
time_format: HH:mm:ss
## updated_option supports 'mtime', 'date', 'empty'
updated_option: 'mtime'

# Pagination
## Set per_page to 0 to disable pagination
per_page: 10
pagination_dir: page

# Include / Exclude file(s)
## include:/exclude: options only apply to the 'source/' folder
include:
exclude:
ignore:

# Extensions
## Plugins: https://hexo.io/plugins/
## Themes: https://hexo.io/themes/
theme: yilia

# Deployment
## Docs: https://hexo.io/docs/one-command-deployment
deploy:
  type: git
  repo: https://github.com/Corner430/corner430.github.io.git
  branch: main



# 解决模块缺失问题
jsonContent:
    meta: false
    pages: false
    posts:
      title: true
      date: true
      path: true
      text: false
      raw: false
      content: false
      slug: false
      updated: false
      comments: false
      link: false
      permalink: false
      excerpt: false
      categories: false
      tags: true


# 添加宠物
live2d:
  enable: true
  scriptFrom: local
  pluginRootPath: live2dw/
  pluginJsPath: lib/
  pluginModelPath: assets/
  tagMode: false
  debug: false
  model:
    use: live2d-widget-model-hijiki
  display:
    position: right
    width: 150
    height: 300
  mobile:
    show: true
```

## 6 文章示例

```yml
---
title: Hello World
date: 2016-03-30 21:18:02
tags:
  - hexo
  - Ubuntu
declare: true
password: hello
toc: 1
top: 1
---
```