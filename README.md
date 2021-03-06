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
 - vue-resource:类似于ajax实现后台交互
 - v-model:主要是在表单元素的双向数据绑定中使用。比如文本框、下拉框、单选、复选、textarea等等。因为v-model是双向绑定的，所以文本框输入以后，模型也会发生改变。反之模型改变了文本框也会改变。
 - v-text：主要用于文本的渲染。和{{}}功能一样。但是{{}}在第一次页面Vue没有初始化完成时，会显示{{}}字符。故文本渲染多用v-text。
 - v-show：控制显示隐藏。不用v-if，使用v-show的情况下，dom是存在的。v-show通过指定CSS样式给元素添加display block或者display none进行控制。
 - v-if：控制显示隐藏。如果if不成立，则整个dom不进行渲染，即不存在。
 - v-bind：绑定属性。给一个dom元素添加属性。比如：在做图片的渲染过程中，如果图片的src地址是动态的，那么就可以利用v-bind去绑定src属性来实现src的赋值。
 - v-for：循环。主要用于表格<li> 标签，去循环一个数组。
 - v-on：事件绑定。(v-on:同等于@)
 - filter : 过滤器。格式化数据。对接口返回的字段进行业务转换。比如金额，加上金额货币符号，如后台返回金额19数字。页面显示：￥19.00元。
 - component ：组件。在做单页面过程中使用多些。把每一个网页做成多个组件然后拼接。起到组件复用。如页面头部底部和轮播等。

#### 项目描述：
 1，创建一个vue实例。页面采用CDN内容分发网络引入vue库文件，后台数据采用json格式模拟，使用resource插件$http方法调用json。

 2，通过v-for指令渲染产品数据，从json文件中读取商品信息，商品金额，商品数量，总金额和编辑。

 3，使用filter对金额进行格式化，为金额前加上金额货币符号。

 4，使用v-on绑定点击事件实现产品金额的动态计算，vmodel添加到商品数量上，当商品数量发生变化的时候，总金额也会随之发生变化。

 5，实现选中，全选功能，添加类，对象中的变量不存在，用set()全局注册，局部注册$set()

 #### 遇到的问题：
 1，json数据不能直接展现出来，报错说没有存到数据，调试发现返回的是空，根据断点显示，resource插件返回的并不是直接的json数据，而是封装了一层，将封装层属性添加上，解决了json数据无法显示的问题。

 2，图片无法动态渲染，采取vbind添加属性时，图片渲染的时候不能使用{{}},如果图片的src地址是动态的。会当成路径解析。

 3，创建实例，调用实例的时候，控制台报错为定义，原因是2.0版本的钩子函数不能保证实例已经插入文档，添加vue.nextTick解决。
 
 4，在渲染文本的时候，如果使用{{}},vue没有粗俗化完成时，会显示{{}},最好用v-text。
 5，同时使用v-bind去判断添加class类。



