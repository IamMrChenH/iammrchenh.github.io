---
title: Hexo的使用和配置
categories: hexo #分类
tags:
  - hexo
  
---
[toc]

# hexo 的使用

## 安装命令

* sudo npm install --unsafe-perm --verbose -g hexo
* npm install hexo-generator-searchdb --save
* npm install `--`save hexo-deployer-git

## 创建一个项目

* hexo init  项目名称

## 运行项目(hexo s)
* hexo server

此时访问 http://localhost:4000/ 就会出现hexo的默认网页

## 编译发布命令

* hexo clean 
* hexo generate 
* hexo deploy

## 发布设置

* 进入项目_config.yml文件

* 修改deploy配置

```yaml
#发布选择
deploy:
  type: 'git'
  branch: master #你的分支
  message: 提交信息
  repo:
    gitee: https://gitee.com/IamMrChen/IamMrChen  
```

---
## 标签页

* 添加标签页
* 运行 hexo new page tags
* 生成 source/tags/index.md 文件和文件夹
* 配置index.md
```markdown
---
title: tags
date: 2019-12-19 20:22:08
type: "tags"
---
```

* 重新运行 hexo s,就可以进入标签页面了



---

## 分类页

* 添加标签页
* 运行 hexo new page categories
* 生成 source/categories/index.md 文件和文件夹
* 配置index.md

```markdown
---
title: tags
date: 2019-12-19 20:22:08
type: "categories"
---
```

* 重新运行 hexo s,就可以进入分类页面了



## 归档页

* 添加标签页
* 运行 hexo new page archives
* 生成 source/archives/index.md 文件和文件夹
* 配置index.md

```markdown
---
title: tags
date: 2019-12-19 20:22:08
type: "archives"
---
```

* 重新运行 hexo s,就可以进入归档页面了



## 关于页

* 添加标签页
* 运行 hexo new page about
* 生成 source/about/index.md 文件和文件夹
* 配置index.md

```markdown
---
title: tags
date: 2019-12-19 20:22:08
type: "about"
---
```

* 重新运行 hexo s,就可以进入关于页面了，https://iammrchen.gitee.io/about/









---

# 切换next主题和配置

## 下载主题

* 进入hexo项目目录

* 下载主题

* git clone https://gitee.com/zhaoguiyang/hexo-theme-next theme/next

* 修改hexo项目下_config.yml 文件配置

 ```yaml
title: 博客名称
subtitle: '博客副名称.'
description: '博客说明！'
keywords: 用于被搜索引擎抓取的关键字
author: 文章作者名称
language: zh-CN #选择中文
timezone: ''
# 文章底部版权信息地址
url: https://iammrchen.gitee.io/
 ```

## 修改导航栏显示
* 进入项目主题下的next目录，选择文件themes/next/_config.yml
* 找到menu配置，修改配置
* 不显示可以选择删除或者注释掉
```yaml
menu:
  home: / || home	#首页
  tags: /tags/ || tags #标签
  archives: /archives/ || archive #归档
  categories: /categories/ || th #分类
  about: /about/ || user #关于
  schedule: /schedule/ || calendar #时间表
  sitemap: /sitemap.xml || sitemap #不知道
  commonweal: /404/ || heartbeat #404页面
```



---

## 开启博客外链(github、微博等)

* 进入项目主题下的next目录，选择文件themes/next/_config.yml
* 找到social配置，修改配置
* 不显示可以选择删除或者注释掉,自由添加删除。

```yaml
social:
  GitHub: https://github.com/Gyang18 || github
  gitee: https://gitee.com/zhaoguiyang || gitee
  QQ邮箱: 2770723534@qq.com || envelope
  Weibo: https://weibo.com/yourname || weibo
```



---

## 开启博客右上角github图标

* 进入项目主题下的next目录，选择文件themes/next/_config.yml
* 找到social配置，修改配置
* 不显示可以选择删除或者注释掉,自由添加删除。

```yaml
github_banner:
  enable: true
  permalink: https://你的github地址。
  title: Follow me on GitHub
```



---







