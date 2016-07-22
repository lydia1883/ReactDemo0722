#React 示例分享

###React是什么

React是FaceBook公司的开源框架，设计思想独特，方式创新，性能出众
是一款颠覆式前端UI开发框架

####React特点
#####仅仅是UI
######------作为MVC架构的V层
#####虚拟DOM
######------性能更高，不需要过重的DOM支持
#####数据流
######------单向数据绑定，减少重复代码
#####React Native甚至可以开发Android,IOS原生应用
#####可组合性
多个组件组合为一套组件库

###为什么使用React

#####构建随着时间数据不断变化的大规模应用程序
######简单
应用程序的模式比较固定
##### 声明式
数据变化会"刷新"视图，仅是数据发生变化部分

#####构建可组合的组件
复用、封装、便于测试和维护及查错，使开发更加轻松便捷

###学习React
####核心思想:
####1.封装组件
#####组件有各自的状态和UI,当状态变更，即可自动渲染整个组件
	
	var HelloMessage = React.createClass({
		  render: function() {
			    return
			    <div>
				    Hello{this.props.name}
			    </div>;
	  }
	});

	React.render(<HelloMessage name="John" />, mountNode);
	

		
####2.JSX语法
#####React开发使用JSX语法，是为了更优雅的把HTML模板插入JS代码中。但无法直接做到，需要通过编译输出JS代码

#####JSX语法
    React.render(
	  <h1>Hello, world!</h1>,
	  document.getElementById('example')
	);
#####编译后的JS文件
    React.render(
	 React.createElement('h1', null, 'Hello, world!'),
		  document.getElementById('example')
	);
#####使用React需要理解jsx语法,即在javascript中书写类XML的语法，使用该语法须进行编译，类似TypeScript/CoffeeScript

####3.虚拟DOM
#####组件更新state的时候，React会调用render方法重新渲染整个UI。


####4.Data Flow（应用架构的方式）
----构建大型应用的最佳实践
#####单向数据绑定
#####Redux


###React组件的state和props

####这两个是组件的核心概念
#####props是组件的属性，一般情况下不要更改
#####state是组件的当前状态，组件根据不同的state呈现不同的UI

###React组件的DOM操作
####通过设置ref和refs进行获取

###注意:
####1.组件名必须要大写
####2.必须要填写Render
####3.函数调用的上下文
####4.JSX语法标签必须闭合
####5.原生的属性名要改写为其他形式，如
####class要改为ClassName 
####6.行间样式要书写双大括号 如
#### style={{opacity:opacity}}
####7.不要尝试直接操纵DOM
####8.监听事件要书写为驼峰形式
####9.尽量创建无状态的子组件