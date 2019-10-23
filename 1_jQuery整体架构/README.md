

JQuery整体架构-百度脑图
```
    (function(window, undefined) {
        
    })(window)

```
自执行函数，生成单独作用域，未传undefined，保证undefined的值

- JQuery无new构建实例
- 共享原型设计
- extend源码分析


```
    var JQuery = function(){
        return new JQuery.prototype.init()
        
    }
    JQuery.fn = JQuery.prototype = {
        init: function(){
            
        },
        css: function(){
            
        }
    }
    jQuery.prototype.init.prototype = JQuery.fn;

```
给JQuery扩展方法 $.extend()
给实例对象扩展 $.fn.extend()

```
    JQuery.fn.extend = JQuery.extend = function(){
        
    }
    
```
通过参数个数来判断哪种用途 arguments.length
判断数据类型
通过this指向 JQuery 或者 JQuery实例对象