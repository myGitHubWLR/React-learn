# JSX

# 什么是JSX
- Facebook起草的JS扩展语法
- 本质是一个JS对象，会被babel编译，最终会被转换为React.createElement
- 每个JSX表达式，有且只有一个根节点
  - React.Fragment  <></>
- 每个JSX元素必须结束

## 在JSX中嵌入表达式
  - 将表达式作为内容的一部分
  - null,undefined,false不会显示
  - 普通对象不能作为子元素 ｛a:1｝
  - 可以放置react元素对象
  - 将表达式作为元素属性
  - 放置数组，会遍历数组元素，作为子元素嵌入
  - 属性使用小驼峰命名法
  - 防止注入攻击
  - 自动编码
  - dangerouslySetInnerHTML={
    {
      _html:
    }
  }

 {/*注释/}

## 元素的不可变性
- 虽然JSX元素是一个对象，但是该对象中的所有属性不可更改  冻结元素 Object.freeze(demo)
- 如果确实需要更改元素的属性，需要重新创建JSX元素