# Node.getRootNode()

## W3C 标准
[WHATWG: getRootNode](https://dom.spec.whatwg.org/#dom-node-getrootnode)

**以下用法和代码和标准不一致，只表示Chrome 54的实现**

## 定义和用法
节点（node）的getRootNode(optional)方法用于获得指定节点所在的根节点。包括两种情况：

1. 如果指定节点不是Shadow DOM中的节点，则返回值为document节点对象
2. 如果指定节点是Shadow DOM中的节点，分为两种情况：

    - optioal为{composed:false}，则返回值为该节点的ShadowRoot节点对象
    - optioal为{composed:true}，则返回值为document节点对象

> 语法：node.getRootNode(optional)
>
> 参数：optional为一个对象，只包含composed属性。composed为一个布尔值，true表示不返回ShadowRoot对象，false表示返回ShadowRoot对象，默认为false
>
> 返回值：document节点对象 或 相应的ShadowRoot节点对象

[示例代码](./getRootNode().html)

## 兼容性
> 只有Chrome 54 支持

## 参考资料
1. https://developer.mozilla.org/en-US/docs/Web/API/Node/getRootNode
2. https://developer.mozilla.org/en-US/docs/Web/Web_Components/Shadow_DOM