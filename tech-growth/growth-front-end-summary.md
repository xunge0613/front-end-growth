@(Front End Growth)[前端开发, Vue.js, JavaScript, github]

# Growth Front-End Summary

> 前言：
> 本文主要是有关前端方面知识按照目前的认知进行的归类和整理，部分知识结构参考了 MDN，也会有相应的链接指向 MDN 方便读者查阅相关内容。
> 
> 初衷。写这篇文章主要有以下几个初衷：
>  - **梳理知识体系**。网上虽然有许多类似的内容，但每个人都有各自独特的思维方式，适合自己的才是最好的。
>  - **探索不足之处**。明确自己到底掌握了哪些，哪些本应掌握但还没有学习。
>  - **完善公司的前端培训方向**。前端技能培训的方向理应由懂前端、懂公司前端团队的人来设定最好不过了。
>  - **希望借此激发大家的一点思考**。我们都在路上，我不是成功的例子，我写下我的思考，希望借此激发大家的一点思考。
>  - **一件小事**。5 年来，我知乎上获赞最多的答案是引用他人的答案……有点尴尬：[《一名合格的前端工程师的知识结构是怎样的？》](https://www.zhihu.com/question/19588629/answer/14573765)

## 专业技能

### 前端理论

#### 浏览器

- 浏览器默认事件
- 浏览器任务调度机制
	- micro queue
	- macro queue
- 浏览器兼容性
	- 不同浏览器差异
		- CSS 私有属性前缀（注：建议使用 postcss 自动化补全）
		- Polyfill
	- HTML、CSS、Javascript 特性支持度
		- MDN 
		- Can I use ?
- 浏览器内核渲染原理
	- HTML  解析器
	- CSS 解析器
	- JavaScript 引擎
	- 渲染流程
		- 加载
		- 解析（确定结构、计算样式）
		- 构建 DOM 树、应用样式
		- 绘制
		- 回流
		- 重绘 
- 浏览器调试
	- 工具
		- F12
		- 扩展插件	
	- 调试内容
		- 元素
			- 结构
			- 属性			
		- 样式
		- 脚本
			- 日志
			- 断点
			- 事件
			- 变量监听
			- 调用堆栈
		- 性能
			- snapshot
			- 耗时
		- 网络请求
			- 模拟请求
			- 审查网络
			- 模拟网络环境
		- 内存
		- 本地存储信息
			- cookie
			- local storage
			- cache
	- 调试技巧
- 常见问题
	- 请求跨域
	- iframe 跨域通信
	- 各种兼容性问题
	- 网页加载速度慢	
	- 按钮点击没反应……

#### HTML

> 据说 HTML 和 CSS 一起学习体验最佳哦

- 语法 & 语义
	- `!DOCTYPE` HTML 文档标准
	- `head` 
		- `meta` 元数据标签
			- 网页描述
			- 设备描述
			- HTTP 请求描述
			- HTTP Client Hints		
	- `body` 
		- 装饰型标记（不推荐、部分已废弃）
		- 功能型标记
			- 无语义容器（div、span）
		- 用户交互（交互型标记）
			- 输入框
			- 选择器
			- 多选框
			- 单选框
			- 按钮
		- 数据可视化（展示型标记）
			- 定义列表
			- 无序列表
			- 表格
			- 结构化数据标记、[微数据](https://support.google.com/webmasters/answer/3069489?hl=zh-Hans)
			- 多媒体
				- 图片
				- 视频
				- 音频
			- SVG、Canvas
			- 文章（正文、摘要、段落、章节、前言、结语、引用）				
- 规范
	-  HTML 代码规范
	-  HTML 使用规范（标签嵌套规则）
		-  标签类型
- 可访问性、无障碍体验
- 常见问题
	- 图片空 src 导致页面加载两次
	- iframe 空 src 导致无限循环加载本页面

![Alt text](http://www.softwhy.com/data/attachment/ueditor/upload/image/20170131/1485839631179872.png)
上图据说是 HTML5 规范中关于 HTML 标签嵌套规则的示意图。

#### [CSS](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS)

> 吃土小2叉：用设计师的思维去理解 CSS，用程序员的思维去写 CSS

- 语法（CSS 从入门到放弃）
	- 基本用法
	- 选择器
		- 基础选择器
		- 组合选择器
		- [伪类选择器](https://developer.mozilla.org/zh-CN/docs/Web/CSS/:hover)
	- 媒体查询
	- 简写属性
	- 注释
	- 属性运算 calc()
- 规范（编写可读性良好的 CSS）
	- 用例规范
		- 权限控制
		- 最佳实践
		- 不良习惯
	- 格式规范
		- 风格
		- 复用
		- BEM 规范 
- 逻辑特性（在 CSS / Less 中运用 OO 思想和设计模式）
	- 权重（优先级）
	- 作用域
	- 封装（mixins）
	- 组合（mixins+）
	- 扩展（extend）
	- 继承（:extend）
	- CSS 变量、Less 变量
	- 模块化（import）
- 视觉设计（单一状态设计）
	- 布局
		- 盒模型（高度、宽度、边框、外边距、内边距、溢出控制）
		- 定位方式
		- [层叠上下文](https://developer.mozilla.org/zh-CN/docs/Web/Guide/CSS/Understanding_z_index/The_stacking_context)（z-index）	
		- display 类型（table、inline、inline-block、block、flex、grid）
		- 浮动		
		- [伪元素](https://developer.mozilla.org/zh-CN/docs/Web/CSS/::after)：:after、:before 
	- 字体排印（）
		- 字体（字体族、网络字体）
		- 文本（删除线、下划线、斜体、粗细、字号）
		- 段落（行高、缩进、换行方式）
		- 对齐
		- 方向
	- 装饰（神说，要有光）
		- 颜色
		- 背景
		- 边框（border、outline）
		- 圆角
		- 阴影
		- 渐变
		- 透明度
		- [变形](https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/transform)（旋转、缩放、矩阵变化）
- 交互设计（多状态设计）
 	- 动画（运动和静止是对立的统一）
		- 过渡效果
		- 动画关键帧		
	- 反馈
		- active、checked 状态		
	- 引导
		- 结合 Javascript
		- CSS 动画
	- 互动
		- hover 状态
- 多设备设计
	- 响应式设计（多套代码，多种设备）
		- 媒体查询		
	- 自适应设计（一套代码，多种设备）
		- 最小固定宽度布局
		- 百分比布局
		- 栅格布局、弹性布局		
		- js + rem 方案（rpx）
- 常见问题
	- 视觉还原度
	- 调试技巧
	- 属性“失效”问题
		- transition “失效”？
		- z-index “失效”？
	- 外边距合并
	- 边框 1px 问题
	- 垂直居中
	- 大屏幕 rem 小屏幕 px
	- 图片适配
	- 可维护性
		- 权重控制
		- 嵌套层级
		- 语义性
- 扩展内容
	- 预处理器：Less、Sass
	- 后处理器：postcss
	- 小程序的 WXSS
	- Weex、RN 中的 CSS

#### JavaScript

> 吃土小2叉：至今还没看完一遍《JavaScript 高级程序设计》的我是该好好面壁思过了。
> 
> 本段内容**大量参考**了：http://javascript.info/


- JavaScript 标准
	- 严格模式
	- 兼容模式
- 基础语法
	- 数据类型		
		- 基本数据类型 `number`、 `string`、 `boolean`、`null`、`undefined`、`object`、`symbol`
		- 数据类型检测
	- 变量
		- 声明 `var`、`let`、`const`
		- 声明提升
	- 作用域	
	- 逻辑控制
		- 循环
		- 分支
		- 判断
	- 逻辑
		- 函数
			- 函数默认值
			- 函数声明
			- 立即执行函数
			- 箭头函数
		-  运算符
			- 数值运算	
			- 逻辑运算
	- DOM
	- 网络请求
		- ajax
		- Promise
		- async、await

- 深入细节
	- `object`
	- 数据类型
	- 函数相关的进阶用法
		- 递归、调用堆栈
		- 闭包
	- 面向对象
	- 错误处理
- 代码质量
	- 注释
	- 相关工具
		- ESLint、JSLint
		- Standard.js
		- Prettify 
		- 自动化测试工具：Jest、Mocha
	- 用例规范
		- 最佳实践
		- 不良习惯
	- 格式规范	
		-  风格

#### 编程通用

> 可读性、可维护性、可复用性、易于扩展

推荐阅读：[《从达标到卓越 —— API 设计之道》](http://mp.weixin.qq.com/s/jhqzRaQOCycd2uvxttpe4Q)

- 可读性、可维护性、可复用性、易于扩展
	- 面向对象思想
	- 设计模式
	- 注释
	- DRY
	- 编码规范
	- 解耦
	- 复杂度控制
- 逻辑
	- 算法	
	- 

#### SEO & 数据统计 & 数据分析

- SEO
	- 影响因素
		- 相关性
			- title
			- 关键词密度
		- 权威性
			- 外链
			- 内链
			- 域名年限
			- 网站收录
			- 安全性
		- 用户体验
			- 广告
			- 加载速度
			- 内容真实性、内容原创性、内容质量
	- 不良行为
		- 堆叠关键词
		- 抄袭、作弊
		- 大量低价值外链
-数据统计
	- 工具
		- 统计工具：Google Analytics、百度统计、Piwik……
		- 站长工具：Google Webmaster 、百度站长工具
		- 其他工具：百度指数、SEO 各项指标助手工具……
- 数据分析
	- 工具
		- 同数据统计工具
		- 脑子是个好东西
	- 分析方法
		- 归因、排查 
		- 细分
			- 来源、渠道			
			- 用户属性
				- 人口统计学		
			- 用户行为
				- 站内搜索关键词
				- 自定义事件（埋点事件）
				- 浏览频率、时间、跳出页
				- 访问内容
				- 访问漏斗
			- 站点属性
		- 对比
			- 时间维度
			- 统计指标维度
	- 目标设置
		- 转化路径
		- 转化目标
		- 转化价值
			 		
#### 网络基础

> 此处是不是又要出现，经典问题：当你在浏览器输入 URL 并回车（非单页应用的传统网站），直到你看见这个页面，此时经历了哪些过程（略去浏览器渲染环节）。

- TCP / IP
	- HTTP
		- 请求
		- 响应
		- 过程：三次握手
	- HTTP2
	- HTTPS 
	- Web Socket
	- CORS
	- Session、Cookie
	- RESTful / RPC	
- DNS 、域名、IP
	- 域名劫持
	- 内网、公网地址段	
- 缓存
	- 服务端缓存
	- 客户端缓存
- 常用工具
	- F12 Network Panel
	- Advanced REST client
	- EditThisCookie
	- Wireshark
	- Fiddler、Charles
- 常见问题
	- HTTP 迁移到 HTTPS 站点部署问题
		- HTTPS 证书部署
			- TLS 版本问题
			- 证书作用域（是否包含子域名）
			- 证书、秘钥配置文件
		- 资源加载同协议
			- `error 级` 
				- 外部 JavaScript 加载
				- iframe
			- `warning 级` 
				- img
				- CSS
		- 网络请求同协议
			- `error` 级
				- ajax
				- jsonp 
### 交叉领域理论

> 吃土小2叉：学习交叉领域知识的一个很朴实的目的 —— 掌握如何甩锅

#### 设计相关

- 与设计师的沟通、协作
- 设计理念 => 用户体验
	- 一致性
	- 可用性
	- 易用性
	- 反馈

#### 后端基础

- 与后端开发工程师的沟通、协作
	- 明确分工
	- 文档先行
	- mock 数据
- 简单了解一门后端语言 // XX 注：如果你已经自己搭建了个人的博客站点，后端语言的语法层面足够了。


### 前端实践

实践是检验真理的唯一标准，在此引用 Vue.js 作者尤雨溪的一段话：

> 技术方案都是**先有问题**，**再有思路**，**同时伴随着取舍**。在选择衡量技术的时候，尽量去思考这个技术背后是在解决什么问题，它做了怎样的取舍。这样一方面可以帮助我们更好的理解和使用这些技术，也为以后哪天你遇到业务中的特殊情况，需要自己做方案的时候打好基础。


####  常见问题

前阵子我在 GitHub 上也开了一个项目，专门记录、收集我最近在前端开发过程中遇到的一些问题，有已经解决的，也有仍待解决的。

> https://github.com/xunge0613/front-end-practice-collections

目前整理的已解决问题有：

- [解决跨域 iframe 父子页面间通信问题](https://github.com/xunge0613/front-end-practice-collections/tree/master/solutions/iframe/iframe-cross-domain-auto-height)
- →_→ 没有更多了……

仍待解决的问题：

- 如何优雅地监听元素高度变化？

当然我也简单写了一些方法论，包括：

- [如何解决问题？](https://github.com/xunge0613/front-end-practice-collections#how-to-solve-a--problem-)
- [如何提问题？](https://github.com/xunge0613/front-end-practice-collections#how-to-ask-a-question-)

后续我也会不断完善这一块内容。重点是：**形成一套属于自己的最佳实践经验库。**

#### 学习型项目

这一部分内容更推荐大家关注 Phodal 大神的 Growth 系列

> https://github.com/phodal/growth

而我给准备入门前端的新手的建议是：

> 拥有一个完全属于自己的**博客、域名、网站、服务器**，并每周固定更新博客文章、每年为博客更新一次主题。

#### 前端工程

勿忘自己的 title：**前端工程师**

> 以下引用[张云龙 dalao 的文章：前端工程 —— 基础篇](https://github.com/fouber/blog/issues/10)

> 第一阶段：库/框架选型
> 第二阶段：简单构建优化
> 第三阶段：JS/CSS模块化开发
> 第四阶段：组件化开发与资源管理
>  
> 由于先天缺陷，前端相比其他软件开发，在基础架构上更加迫切的需要**组件化开发和资源管理**，而解决资源管理的方法其实一点也不复杂：
> 
> **一个通用的资源表生成工具 + 基于表的资源加载框架**

#### 第一阶段：框架应用

> 吃土小2叉：只要是一个文档友好的框架，遇到不会的问题，去翻翻文档，如果解决不了，再去认真翻一次。因此，第一阶段，亦可认为是：**面向文档编程**。

**此处建议再回忆一下刚才提及的尤大的话。**

以下是我个人的框架/库应用路线：

> jQuery => jQuery + artTemplate => Vue.js + lodash => Vue.js 全家桶

- jQuery // 此处参考[张鑫旭的 jQuery 1.4 中文文档](http://www.zhangxinxu.com/jq/api14/) 
	- 核心
		- 对象访问
		- 数据缓存
		- 队列控制
		- 插件机制
		- 多库共存
	- 事件
		- 页面载入
		- 事件处理
		- 事件委托
		- 事件切换
		- 常用事件
			- 鼠标事件（click、dbclick、hover、mouse*……）
			- 键盘事件（key*……）
			- 表单事件（blur、change、focus、submit、select）
			- 浏览器事件（error、resize、scroll）
			- 触摸事件（touch*……）
	- 选择器
		- 基本
		- 组合
		- 伪类
		- 内容
		- 可见性
		- 属性
		- 表单
	- 筛选器
		- 过滤
		- 查找
		- 串联
	- CSS
		- CSS
		- 位置
		- 尺寸
	- DOM 操作
		- 元素节点（增、删、移、换、复制）
		- 元素属性（增、删、改、查）	
		- 文本内容（增、删、改、查）
	- 网络请求
		- Ajax
		- when
		- deferred
	- 特效
		- 基本（显示、隐藏）
		- 滑动
		- 淡入淡出
		- 自定义动画控制
	- 辅助工具（类似于 lodash）
		- 数组、对象操作
		- 函数操作
		- 字符串操作
 		- 浏览器及特性检测
		- 类型检测
		- JSON 序列化
- artTemplate
	- 模板引擎
- Vue.js // 
	- MVVM 思想
	- 声明式渲染
	- 条件与循环
	- 处理用户输入
	- 数据绑定、响应式数据
	- 组件化应用构建
- lodash.js

**XX 注：当你学会 Vue.js 以后，你会发现小程序真的很容易上手。**

#### 第二阶段：简单自动构建优化

- 预处理
	- Less
	- Babel
- 后处理
	- postcss
- 压缩
	- 代码
	- 图片
- 合并
- 打包
- 自动化测试
- mock 接口调试
- 雪碧图生成工具

#### 第四阶段：组件化开发与资源管理

- Vue.js 组件化开发
	- 抽象业务逻辑组件
		- 组合基础 UI 组件形成业务组件
		- 独立编写业务相关组件
		- ……
	- 定制基础 UI 组件库
		- 轮播图组件
		- 弹窗组件
		- ……
- 资源管理
	- 暂无相关实践	（如果说 webpack 打包生成 组件库.js，然后扔到 NPM 也算的话……）

#### 项目技术选型

考虑因素

- 预计投入
	- 开发资源
		- 时间
		- 人手
		- 技术储备		
	- 项目资源
		- 沟通成本
		- 设计文档、功能文档、产品原型
		- 后端接口文档
		- 项目排期 
	- 产品资源
		- 用户群体
			- 浏览器兼容性
			- SEO 问题		
- 期望回报
	- 开发人员自我成长
	- 公司技术栈
	- 开发效率、可维护性
	- 性能、稳定性
	- 易于测试
	- 易于把控项目周期

#### 造轮子

- UI 组件库
- 前端工具 
- 前端微服务
- 前端框架
- ？

## 版本规划

本文会在 GitHub 上持续维护，欢迎大家提 issue ~

地址是：https://github.com/xunge0613/front-end-growth/blob/master/tech-growth/growth-front-end-summary.md

v 0.0.2 

- 完善各个概念点指向 MDN 的链接
- 更新“前端实践”内容


## 结语

其实本文亦可视作另类的 MDN 导读 ^_^

若有帮助，感谢打赏！

![如果有帮助，欢迎打赏~](http://o7q107fd8.bkt.clouddn.com/image/github/wechat-payment.jpg)
