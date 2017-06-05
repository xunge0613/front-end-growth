@(Front End Growth)[前端开发, Vue.js, JavaScript, github]

# Growth Front-End Summary

> 前言：
> 本文主要是有关前端方面知识按照目前的认知进行的归类和整理，部分知识结构参考了 MDN，也会有相应的链接指向 MDN 方便读者查阅相关内容。

> **注意：由于以下分类主要是基于 XX 个人对前端的认知，仅供参考。也欢迎大家指出其中不足之处。**

## 专业技能

### 前端理论

#### 浏览器

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


#### HTML

- 语法 & 语义
	- `meta` 元数据标签
		- HTTP Client Hints
	- 结构化数据标记、微数据
	- `body` 结构化文档	
		- 装饰性标记（不推荐、部分已废弃）
		- 表单
			- 输入框
			- 选择器
			- 多选框
			- 单选框
			- 按钮
		- 数据可视化
			- 定义列表
			- 无序列表
			- 表格
		- 文章（正文、摘要、前言、结语、引用）
	- 多媒体
		- 图片
		- 视频
		- 音频
	- SVG、Canvas
- 标准
- 可访问性
- 常见问题
	- 图片空 src 导致页面加载两次
	- iframe 空 src 导致无限循环加载本页面

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
	- 外边距合并
	- 边框 1px 问题
	- 垂直居中
	- transition “失效”？
	- z-index “失效”？
	- 大屏幕 rem 小屏幕 px
	- 图片适配
	- 可维护性
		- 权重控制
		- 嵌套层级
		- 语义性
- 扩展内容
	- Less、Sass
	- postcss
	- 小程序的 WXSS
	- Weex、RN 中的 CSS
#### Javascript

- 基础
	- 数据类型
	- 

#### SEO & 数据统计 & 数据分析

- SEO
	- 影响
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
			- 内容真实性、内容重复度
	- 黑帽
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

- HTTP
- Session、Cookie
- RESTful / RPC


### 交叉领域理论

> 吃土小2叉：学习交叉领域知识的一个很朴实的目的 —— 掌握如何甩锅

#### 设计相关

- 与设计师的沟通、协作
- 设计理念 => 用户体验
	- 一致性
	- 可用性
	- 易用性
	- 反馈

### 前端实践

#### 视觉

- 图片压缩
- 雪碧图

#### 交互

#### 框架应用

#### 前端工程化

#### 业务逻辑抽象

#### 项目技术选型

#### 造轮子

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
