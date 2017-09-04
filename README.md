# 前端面试大全
 
## React & Flux & Vuex

 React解决了什么问题
- **如何设计一个好的组件？**
- **组件的Render函数在何时被调用？**
    - 调用时DOM就一定会被更新吗？
- 组件的生命周期有哪些？
    - 当某些第三方类库想对DOM初始化，或者进行远程数据加载时，应该在哪个周期中完成？
    - 在哪些声明周期中可以修改组件的state？
- **不同父节点的组件需要对彼此的状态进行改变时应该实现？**
    - 如何设计出一个好的Flux架构
    - 如何设计出一个好的React组件
- 如何进行优化？
    - 组件中的key属性有什么用？
- Component 与 Element 与 Instance 的区别
- **如果你使用过Redux与Vuex的话，聊聊他们的区别与你的心得**
    - Vue.js 的双向绑定是如何实现的？
- 解释一下Redux的架构
    - Redux中的store和flux中的有什么不同？
    - 解释一下Redux的中间件
    - redux-thunk 和 connet 解决了什么问题
- Webpack如何打包输出多个文件？
    - webpack打包时如何工作的？
        - 如何解决循环引用的问题
    - 在什么情况下需要打包输出多个文件？
    - loader和plugin的差别
    - 你觉得使用过什么高级技巧吗？
- （开放问题）React的生态你使用过哪些类库

## Personal && Specific && 

- 为什么要写一本书？
- 如何设计一个好的组件？

### 为什么要写一本书

这本书的主题是响应式开发，但并不是因为那个时候我精通响应式开发才去写，恰恰相反我也是才刚开始学习这门技术。而为什么作为一个新手要写是因为有两个原因
1. 我个人有喜欢写技术博客做总结和做研究的习惯，想当然这是一个很长的系列，也很适合入门。与其只放在博客上不如出版为图书
2. 更重要的原因是，胡适说过，**发表是吸收的利器**。我的个人经验也是这样，如果你想检验你对学习的知识的吸纳情况，最好的办法是把它们叙述给另外一个人听，这样你就有可能发现一些**模糊的**或者不足的地方。从而反过来督促进一步学习

### 如何设计一个好的组件

从两个维度看这件事
1. 感性（组件的目标）
    感性上来说，假设你开发了一个组件，当另一个人想要使用你的组件的时候他应该是根据文档无障碍的，你的功能是完全满足他期待的，他不需要在使用组件的时候做二次开发
2. 理性（从概括到具体）
    - SOLID 原则
        - **S: 单一职责**，一个组件只做一件事，支持以**组合**的方式组成另一个组件
        - **O: 对拓展开放**，对修改关闭（对组件的封装）。后端语言是通过继承特性来实现的，而在组件中则可以通过添加 hook 函数，开放自定义样式等实现
        - 接口隔离（对开发组件有启示）
        - 反转依赖（对开发组件有启示）
    - React 官方提倡 Hight Order Component，或者使用 Container Component，将 Container Component 与 Presentional Component 分离
    - 在实现内部使用设计模式
    - 保持好的代码习惯
