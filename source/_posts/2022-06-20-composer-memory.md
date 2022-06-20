---
title: composer内存不足解决方法
date: 2022-06-20 18:54:38
tags: composer
categories: composer
pic: 'composer.png'
---

### composer内存不足报错

<!-- more -->

````
php -d memory_limit=-1 `which composer` update/install -vvv

php -d memory_limit=-1 `which composer` require endroid/qr-code -vvv
````