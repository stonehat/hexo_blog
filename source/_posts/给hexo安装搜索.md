---
title: 给hexo安装搜索
date: 2023-04-13 22:00:41
tags: hexo
---

## 插件
所用插件为:hexo-generator-searchdb

### 插件原理
这个插件会扫描博客文章，根据“——config.yml”的配置从文章里获取内容生成一个xml/json文件的结果，类似于博客中文章信息的摘要把，搜索的时候就搜索这个文件的内容。

### 安装插件
`npm install hexo-generator-searchdb --save`

### 全局配置
修改全局配置文件_config.yml
```
search:
    path: search.xml
    field: post
    format: html
    limit: 10000
```

### 主题配置
修改主题配置文件\themes\{theme_name}\_config.yml
```
# local search
local_search:
    enable:true
```

## 问题
安装后完全不起作用！
点击搜索框，输入文字后，敲击回车进行搜索，仍然跳转到google搜索引擎里，而且并不能搜索。
探寻了一会儿，大概原因是这个网页需要授权给google才能进行搜索。额，也不太想这么去折腾。
最后，找了一通，发现默认的主题landscape，似乎没法解决。必须要换一个主题了！