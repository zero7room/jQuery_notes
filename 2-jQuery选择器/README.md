CSS选择器、源码解析
DOM对象、jQuery对象

 如何把创建的DOM节点包装成jQuery对象？
    context.createElement创建DOM节点存储在数组中，merge方法把数组中存储的DOM节点的成员添加到jQuery实例对象上
jQuery实例对象length属性作用
    存储DOM节点的数组对象平滑地添加到jQuery实例对象上
merge方法的应用场景有哪些？
    合并数组
    把数组成员合并在有length属性的对象上
$(document).ready() 与$(function(){})的关系？
    $(document).ready()是对document.DOMContentLoaded事件封装
    $(function(){})每次调用$()传入的参数会收集在readyList数组中，
    当document.DOMContentLoaded事件触发一次执行readylis中收集处理函数