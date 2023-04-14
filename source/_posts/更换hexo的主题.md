---
title: 更换hexo的主题
date: 2023-04-13 23:16:54
tags: 
    - hexo
---

## next主题
在网上搜了一下，发现好多教程都用的next主题。嗯，那我也用它试试吧。用一个大家都用的，翻车就会少些。

## 下载
```
git clone https://github.com/theme-next/hexo-theme-next themes/next
```

需要注意的是，注意文件夹的名字。
由于我一般用git clone都不带目的地址（也就是这里的themes/next），所以下载下来的文件夹是“hexo-theme-next”。结果导致按照后续步骤，整个网页都无法显示了。将文件夹改为next后才正常。

## 修改配置
修改全局配置_config.yml
```
# Extensions
## Plugins: https://hexo.io/plugins/
## Themes: https://hexo.io/themes/
theme: next
```

## 修改主题配置
更换完主题后哦，必须要做一些配置。

### 启用tags
默认主题landscape，默认就可以用tags。但是next主题需要一些额外的配置。
1. 修改menu配置
在主题配置/themes/next/_config.yml中，找到“Menu Settings”，进行修改内容。
目前，我只启用了home、tags、archives三个按钮：
```
home: / || fa fa-home
tags: /tags/ || fa fa-tags
archives: /archives/ || fa fa-archive
```
2. 新建tags页面
在终端输入
```
$ hexo new page tags
```
找到/source/tags/index.html，内容修改如下：
```
---
title: tags
date: 2023-04-13 22:53:12
type: tags
comments: false
---
```

### 修改sheme
默认的scheme是Muse，菜单在顶部，不太喜欢。修改为Pisces。在主题配置/themes/next/_config.yml中找到“Scheme Settings”，修改如下：
```
# Schemes
#scheme: Muse
#scheme: Mist
scheme: Pisces
#scheme: Gemini
```