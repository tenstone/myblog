title: 安装ImageMagick和php-imagick
date: 2016-01-12 12:58:54
tags: 快捷笔记
categories: IT技术
---

pecl安装PHP组件报错，

        Warning: Invalid argument supplied for foreach() in Command.php on line 259
        Warning: Invalid argument supplied for foreach() in Command.php on line 259

后来发现是php-pear安装版本错误，执行下列命令，删除原有旧版本的安装包，之后，结果如预期。

        yum erase php-pear
        yum install php56w-pear
        pecl install imagick
        
### PEAR 是“PHP Extension and Application Repository”的缩写，即PHP扩展和应用仓库
> PEAR 将PHP程序开发过程中常用的功能编写成类库，涵盖了页面呈现、数据库访问、文件操作、数据结构、缓存操作、网络协议、WebService 等许多方面，用户可以通过下载这些类库并适当的作一些定制以实现自己需要的功能。避免重复发明“车轮”。PEAR 的出现大大提高了PHP 程序的开发效率和开发质量。

### PECL 是“PHP Extension Community Library”的缩写，即PHP 扩展库

> PECL 可以看作PEAR 的一个组成部分，提供了与PEAR 类似的功能。不同的是PEAR的所有扩展都是用纯粹的PHP代码编写的，用户在下载到PEAR 扩展以后可以直接使用将扩展的代码包含到自己的PHP 文件中使用。而PECL是使用C 语言开发的，通常用于补充一些用PHP难以完成的底层功能，往往需要重新编译或者在配置文件中设置后才能在用户自己的代码中使用。
        
  
