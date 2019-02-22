Chinese
=====

简繁体转换

# 安装方法

````
composer require hanson/chinese:dev-master
````

# 使用示例
```php
<?php
require_once __DIR__.'/../vendor/autoload.php';

use Hanson\Chinese\Chinese;

$text = '中國人中国人123abc';

// 转为简体
var_dump(Chinese::simplified($text)); // 中国人中国人123abc

// 转为繁体
var_dump(Chinese::traditional($text)); // 中國人中國人123abc

// 转为以多字节字符串分隔的数组
var_dump(Chinese::toArray($text));

// 判断是否全部为中文
var_dump(Chinese::isChinese($text)); // bool(false)

// 判断是否包含中文
var_dump(Chinese::hasChinese($text)); // bool(true)
```
