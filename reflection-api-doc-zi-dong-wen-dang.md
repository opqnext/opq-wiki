# reflection_api_doc

将会是一个基于 thinkphp5 的PHP自动生成api文档的库

1. 使用方法：

在 extra 目录下创建文件名为 documents.php 的配置文件。

配置文件内容如下：

```
<?php
return [
    &#39;title&#39; => "北京想得美科技有限公司",
    &#39;description&#39; => &#39;"想的美app" | APi接口文档等等。&#39;,
    &#39;template&#39; => &#39;apple&#39;, // 苹果绿:apple 葡萄紫:grape
    &#39;class&#39; => [
        &#39;app\index\controller\Demo&#39;,
        &#39;app\index\controller\Product&#39;,
        &#39;app\index\controller\Store&#39;,
    ],
];
```
其中 template 为模板类型，暂时提供两种模板风格，分别为苹果绿和葡萄紫，虽然两套模板都是巨丑无比。所以使用的过程中也可以自己开发模板。

**重点:** class 为将要生成文档的类(带命名空间)