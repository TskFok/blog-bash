---
title: php-fpm-log
date: 2022-06-20 14:36:05
tags: php
categories: 
  - log
  - php
pic: 'php.png'
---

### php-fpm日志查看

<!-- more -->

````
cat /usr/local/php/var/log/php-fpm.log

超时日志
cat /usr/local/php/var/log/php-fpm.log | grep "timed out"

慢日志
cat /usr/local/php/var/log/php-fpm.log | grep "slow"
````