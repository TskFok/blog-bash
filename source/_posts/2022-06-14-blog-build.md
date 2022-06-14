---
title: 搭建blog
date: 2022-06-14 14:02:51
tags: blog
---

### 安装hexo

{% codeblock hexo安装 https://hexo.io/zh-cn/docs/ hexo安装 %}
npm install -g hexo-cli
echo 'PATH="$PATH:./node_modules/.bin"' >> ~/.profile
{% endcodeblock %}

### 创建项目

{% codeblock 创建项目 https://hexo.io/zh-cn/docs/setup 创建项目 %}
blog为项目名称

hexo init blog 
cd blog
npm install
{% endcodeblock %}


### 配置

{% codeblock 配置 https://hexo.io/zh-cn/docs/ 配置 %}
修改_config.yml的title,url,root,new_post_name

title: 标题
url: github page的地址
root: github page的项目名称 和 url一样的时候填写/
new_post_name: 生成新文章的自动名称
{% endcodeblock %}

### 生成新文章

{% codeblock 生成新文章 https://hexo.io/zh-cn/docs/commands 生成新文章 %}
生成名称为title的新文章
hexo new post title

生成名称为title的新草稿
hexo new draft title

发表草稿(把草稿转移到post中)
hexo publish post title
{% endcodeblock %}

### 一键部署

{% codeblock 一键部署 https://hexo.io/zh-cn/docs/one-command-deployment 一键部署 %}
安装 hexo-deployer-git
npm install hexo-deployer-git --save

修改_config.yml的配置
deploy:
type: 'git' //使用git发布
repo: 'git@github.com:TskFok/tskfok.github.io.git' //要发布的github repo的地址,一般是新建一个repo
branch: 'master' //要发布的分支
message: '发布新日记' //git发布时的message


生成站点文件并推送至远程库,过一会就能看到新发布的内容
hexo clean && hexo deploy
{% endcodeblock %}

### github的配置

````
重命名库名称
````
![](/images/general.png)
````
修改pages的分支 选择的分支要和部署配置里的branch相同
````
![](/images/page.png)

### 各种主题

````
不同主题语法不同,需要调试
````
[下载地址](https://hexo.io/themes/)
