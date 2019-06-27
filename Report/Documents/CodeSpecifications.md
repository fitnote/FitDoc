# 代码规范

## 后端代码规范

代码使用ESlint作为基本的语法检验工具。

https://zh-google-styleguide.readthedocs.io/en/latest/google-python-styleguide/contents/

## 前端代码规范

- wxml规范
    -  保证块元素、组件的开始符与结束符不在同一行，上下位置对齐，子元素在父元素内缩进两个空格。 
   - 尽量避免多余的父标签。
   - 所有wxml标签必须有结束符`</view>` `</block>` `</button>`等。
  -  标签属性顺序：
		* `class` （class是为高而复用组件设计的，所以所以应处在第一位）
		* `id`、`name`（id更加具体且应该尽量少使用，所以将它放在第二位）
		* `wx:if`、`wx:else`、`wx:for`
		* `wx:data`
    - id/class命名规则
		 - 遵循“内容优先，表现为辅”的基本原则
		   首先根据内容命名，如header、footer。若根据内容无法找到合适的命名，再结 合表现进行辅助，如col-main、blue-box。
		 - 一律小写，多个单词以'-'连接
		  不能使用下划线和驼峰命名法，如main-nav。可基于最近的父元素名称作为前缀。
		 - 在不影响语义的情况下，可适当使用缩写
		  缩写只用来表示结构，如col、nav、btn等，不可自造缩写。
		 - 避免广告拦截词
		  ad、ads、adv、banner、sponsor、gg、guangg、guanggao等，页面中尽量避免采用以上词汇来命名。
				   
- wxcs规范
   - 属性顺序
	 - 位置属性（position、top、right、z-index、display、float等）
	 - 大小（width、height、margin、padding等）
     - 背景（background、border等）
	 - 文字系列（font、line-height、letter-spacing、color、text-align等）
	 - 其他（animation、transition等）
  - 属性使用缩写
       - 在需要显示地设置所有值的情况下，应当尽量限制使用简写形式的属性声明。常见的滥用简写属性声明的情况如下： padding、margin、font、background、border、border-radius
- js规范
  - 语言规范
     - 变量：声明变量必须加上var关键字。
     - 块内函数声明：不要在块内声明一个函数。
     -  this：仅在对象构造器，方法，闭包中使用。