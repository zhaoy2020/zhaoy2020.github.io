---
title: "Github Pages + Jekyll + Typora 快速搭建个人博客"
layout: post
date: 2022-01-21 22:44
image: /assets/images/markdown.jpg
headerImage: false
tag:
- Github Pages
- Jekyll
- Typora
- Blog
star: true
category: blog
author: ZhaoY
description: 10 mins learning Shell
---

---

利用Github搭建个人博客的方式有很多，这里为了快速直接的完成搭建，我选用了**Github Pages**配合**JekyLL**和**Typora**的方式来高效实现。Github托管脚本，使用已布置好主题的JekyLL网页框架，可以实现一步搭建博客。最后只需要修改Jekyll相关配置以及利用Typora写作blog就可以得到一个属于自己的博客。

---

```shell
# 第一步在Github上新建一个repository，名称格式为：Github_Name.github.io
```

![image-20220127183342702](2022-01-21-GithubPages+Jekyll+Typora.assets/image-20220127183342702.png)

```shell
# 配置本地repository
git clone git@github.com:zhaoy2020/zhaoy2020.github.io.git
cd zhaoy2020.github.io
# 此时只有README文件
```

![image-20220127183628858](2022-01-21-GithubPages+Jekyll+Typora.assets/image-20220127183628858.png)

```shell
# 从Jekyll下载相关主题并解压：http://jekyllthemes.org/
# 我选的是Indigo主题
wget https://github.com/sergiokopplin/indigo/raw/gh-pages/indigo-gh-pages.zip
gzip -d indigo-gh-pages.zip
```

![image-20220127183853330](2022-01-21-GithubPages+Jekyll+Typora.assets/image-20220127183853330.png)

```shell
# 布置
cp -rf /indigo-gh-pages/* /zhaoy2020.github.io/
# 发布
git add -A && git commit -m "upload framework" && git push origin main
```

![image-20220127184333818](2022-01-21-GithubPages+Jekyll+Typora.assets/image-20220127184333818.png)

```shell
# 修改配置
vim _config.yml # 依据相关提示进行配置
# _post文件夹下都是blog，利用Tyora写作markerdown blog，然后发布即可
```

![image-20220127184532887](2022-01-21-GithubPages+Jekyll+Typora.assets/image-20220127184532887.png)
