---
title: WordPress 2.3.1中文显示问题解决方法
date: '2007-12-21 00:00:00'
slug: WordPress231-zhong-wen-xian-shi-wen-ti-jie-jue-fang-fa
categories:
- 转载
tags:
- jekyll
- Linux
---
把wp-includes/gettext.php 106行开始的

$this->enable_cache = $enable_cache;// $MAGIC1 = (int)0×950412de; //bug in PHP 5.0.2
$MAGIC1 = (int) - 1794895138;
// $MAGIC2 = (int)0xde120495; //bug
$MAGIC2 = (int) - 569244523;
// 64-bit fix
$MAGIC3 = (int) 2500072158;

$this->STREAM = $Reader;
$magic = $this->readint();
if ($magic == ($MAGIC1 & 0xFFFFFFFF) || $magic == ($MAGIC3 & 0xFFFFFFFF)) { // to make sure it works for 64-bit platforms
$this->BYTEORDER = 0;
} elseif ($magic == ($MAGIC2 & 0xFFFFFFFF)) {
$this->BYTEORDER = 1;
} else {
$this->error = 1; // not MO file
return false;
}

替换成:

$this->enable_cache = $enable_cache;// $MAGIC1 = (int)0×950412de; //bug in PHP 5
$MAGIC1 = (int) - 1794895138;
// $MAGIC2 = (int)0xde120495; //bug
$MAGIC2 = (int) - 569244523;
$MAGIC3 = (int) 2500072158; // STREAM = $Reader;
$magic = $this->readint();
if ($magic == $MAGIC1 || $magic == $MAGIC3) { // BYTEORDER = 0;
} elseif ($magic == $MAGIC2) {
$this->BYTEORDER = 1;
} else {
$this->error = 1; // not MO file
return false;
}

上传，刷新，竟然显示中文了。问题的根源原来是Wordpress在64位的CPU下（linux系统）运行时，由于PHP-gettext解析.mo语言文件出错，以至于Wordpress在使用中文版本时失败。这是由于PHP-gettext在加载.mo文件时，没有正确匹配验证位导致stream自动关闭。详细请看此文。
原文出自: [http://www.uugrass.com/archives/wordpress-meyu-chinese-character-solve/](http://www.uugrass.com/archives/wordpress-meyu-chinese-character-solve/)

---


