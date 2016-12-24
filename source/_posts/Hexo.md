---
title: Hexo
categories: guide
date: 2016-12-23 16:12:35
tags: 
	- tags
	- hexo
	- guide
---

## New Page --About

### create `about` 

```bash
hexo new page about
```

This generates a folder `about/` `under source/` 

### Edit `index.md`

```md
Hi

This is the note on everything

I mean everything

I mean maybe

```

### add to menu

<span id='add'>
modify the file `_config.yml` under the `theme/`
</span>

```yml
# make it visible
menu:
  home: /
  about: /about

# change the icons
menu_icons:
  enable: true
  #KeyMapsToMenuItemKey: NameOfTheIconFromFontAwesome
  home: home
  about: user 

```


## display one categoires

for example guide

### create `categories` 

```bash
hexo new page categories
```

This generates a folder `categories/` `under source/` 


### categories post

```
---
title: Hello World
categories: guide
tags: 
	- guide 
	- hexo
---

```


### add to menu

modify the file `_config.yml` under the `theme/`
[as describe up](#add)

### change languages file

`themes/next/languages/zh-Hans.yml`

```
menu:
  home: 首页
  archives: 归档
  categories: 分类
  schedule: 日程
  tags: 标签
  about: 关于
  search: 搜索
  commonweal: 公益404
  guide: 教程

```

