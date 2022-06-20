---
title: 阿里云oss
date: 2022-06-20 19:07:00
tags: oss
categories:
  - php
  - oss
pic: 'oss.png'
---
  
### 阿里云oss相关

<!-- more -->

{% codeblock 下载oss文件 %}
$referer = "https://***.com/"; //来源仿造
$opts    = [
    'http' => [
        'header' => ["Referer: $referer\r\n"],
    ],
];
$context = stream_context_create($opts);
file_put_contents($path, file_get_contents($pdfContentPath, false, $context));
{% endcodeblock %}

{% codeblock 小程序oss白名单 %}
小程序添加oss防盗链数据  需要在oss添加白名单
https://servicewechat.com和https://short.weixin.qq
{% endcodeblock %}
