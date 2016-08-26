# （四）Zepto的使用

## 本节课目标

熟练使用Zepto和部分代替Zepto的js，并用js和CSS3做动画

## 本节课涉及知识点

* Zepto
* 部分代替Zepto的js
* CSS3动画

## Zepto介绍

Zepto是一个轻量级的针对现代高级浏览器的JavaScript库， 它与jQuery有着类似的api。 如果你会用jQuery，那么你也会用Zepto。

[Zepto官网](http://zeptojs.com/)

Zepto的特点就是体积小，gzip压缩小于10kb。为了这个特性，Zepto使用模块化处理，默认只加入了5个基础模块，还有12个模块可以根据需求打包。

![Zepto模块](images/zepto_modules.png)

上图右侧描述里有写对应模块的用法。目前我们一直都是用的官网默认5个模块的精简版本，基本够用。

## 精简版Zepto的使用

### 常用的方法

* .on() .off() .one() .trigger()
* .css() .addClass() .removeClass() .hasClass()
* .hide() .show()
* .val() .text() .html()
* .width() .height() .index() .scrollTop() .scrollLeft()
* .attr() .data()
* .find() .children() .siblings() .parent() .parents()
* .append() .appendTo() .prepend() .prependTo()
* .is() .not() .prop()
* .ajax()

（只是常用的，没写全部）

用习惯了jQuery，相信有这些方法，用精简版Zepto基本上问题不大，能实现80%以上的需求。

### 需要加模块的方法

* animate()
* fade*()
* $('div:first')
* touch事件
（只是部分，没写全部）

这部分主要是一些CSS3的选择器、动画、touch事件等。虽然使用频率也多，但基本上可以用其他办法代替，后面有介绍。

## 部分代替Zepto(jQuery)的js

PC端使用jQuery是因为js兼容的浏览器太多，特别是一些陈旧的浏览器IE6、IE7等，jQuery已经帮我们做了兼容处理。而手机上支持的js非常多，所以其实手机上如果不用Zepto等库，也可以用一些简单的js来代替，只要考虑IE10及以上即可。

[YOU MIGHT NOT NEED JQUERY(你可能不需要jQuery)](http://youmightnotneedjquery.com/)

最简单的js选择器：`element.querySelector()`、`element.querySelectorAll()`，选择ID和类名，返回单个对象和数组，完全可以代替jQuery里的`$('#element')`、`$('.element')`。

例如传统jQuery里操作class的几个方法：`.addClass()`→`.classList.add()` `.removeClass()`→`.classList.remove()` `.hasClass()`→`.classList.contains()`，基本上原生js都可以实现。

用的最多的监听事件`$(element).on('click',function(){})`也可以用原生js来写：`document.querySelector('').addEventListener('click',function(){},false);`。

等等，大家可以去上面网站查看。

## js和CSS3做jQuery动画

基本原则：js只操作dom，不做动画，动画交给CSS3处理。

![用CSS实现slideToggle滑动效果](code_01.png)
[用CSS实现slideToggle滑动效果](https://ximan.github.io/mobile-lesson/lesson04/01_slide_toggle.html)

![用CSS实现animate动画](code_02.png)
[用CSS实现animate动画](https://ximan.github.io/mobile-lesson/lesson04/02_animate.html)

![用CSS实现弹窗渐隐效果](dialog.png)
[用CSS实现弹窗渐隐效果](http://ximan.github.io/mobile-layout-example/dialog.html)

## 扩展阅读

[Zepto.js API 中文版](http://www.css88.com/doc/zeptojs_api/)、[YOU MIGHT NOT NEED JQUERY](http://youmightnotneedjquery.com/)

## 课下作业

稍后添加