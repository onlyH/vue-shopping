# vue-shopping
用vue.js开发购物车
### Vue是一个MVVM的渐进式前端框架。
 - 声明式渲染 Declarative Rendering
 - 组件系统 Components
 - 客户端路由 Vue-router
 - 大规模状态管理 Vuex
 - 构建工具 Webpack/Vue-cli
 - 服务端通信 Axios(resource)

 ### Vue基础语法
 - v-model:主要是在表单元素的双向数据绑定中使用。比如文本框、下拉框、单选、复选、textarea等等。因为v-model是双向绑定的，所以文本框输入以后，模型也会发生改变。反之模型改变了文本框也会改变。
 - v-text：主要用于文本的渲染。和{{}}功能一样。但是{{}}在第一次页面Vue木有初始化完成时，会显示{{}}字符。故文本渲染多用v-text。
 - v-show：控制显示隐藏。不用艺v-if，使用v-show的情况下，dom是存在的。v-show通过指定CSS样式给元素添加display block或者display none进行控制。
 - v-if：控制显示隐藏。如果if不成立，则整个dom不进行渲染，即不存在。
 - v-bind：绑定属性。给一个dom元素添加属性。比如：在做图片的渲染过程中，如果图片的src地址是动态的，那么就可以利用v-bind去绑定src属性来实现src的赋值。
 - v-for：循环。主要用于表格<li> 标签，去循环一个数组。
 - v-on：事件绑定。(v-on:同等于@)
 - filter : 过滤器。格式化数据。如后台返回金额19数字。页面显示：￥19.00元。
 - component ：组件。在做单页面过程中使用多些。把每一个网页做成多个组件然后拼接。起到组件复用。如页面头部底部和轮播等。

