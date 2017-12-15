那你可以放到 [github](https://github.com/) 呀。如果方便使用呢，你就放到 [packagist.org]((https://packagist.org/) 呀。

比如我写了一个 [XorEncryption(异或加密)](https://packagist.org/packages/opqnext/xor-encryption) 的方法。

关于 composer 的一些知识，需要自行了解呢。

有人说贴图比较好，我就爱文字叙述/(ㄒoㄒ)/：首先你去 [github](https://github.com/) 上新建一个项目。比如我的 [opqnext/XorEncryptiono](https://github.com/opqnext/XorEncryption)

然后你在你在本地创建一个目录。把项目 clone 下来。之后你可以用 composer init 一步一步按提示添加项目名称，描述，作者，依赖包等等信息最后生成一个 composer.json 的文件。或者也可以新建一个文件，然后直接把我下面这个内容拷贝到你的 composer.json 里。然后对应的配置改一改，第一步完成了。
```
{
    "name": "opqnext/xor-encryption",
    "description": "php xor-encryption",
    "type": "library",
    "keywords": [
        "php",
        "xor"
    ],
    "license": "MIT",
    "authors": [
        {
            "name": "opqnext",
            "email": "309622694@qq.com"
        }
    ],
    "require": {
        "php": ">=5.3.0"
    },
    "autoload": {
        "psr-0": {
            "XorEncryption\\": "src/"
        }
    }
}
```
还是直接拷贝来的容易的，一定要写上 autoload