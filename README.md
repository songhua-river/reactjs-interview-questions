# 翻译 React 面试问题和答案
## [原文请点击这里](https://github.com/sudheerj/reactjs-interview-questions)

> 如果你喜欢这个项目 请给一个Star,表示非常的感谢.

### 内容表格

| 序号. | 问题 |
| --- | --------- |
|   | **React 核心** |
|1  | [什么是React？](#什么是React) |
|2  | [React主要特点是什么？](#React主要特点是什么) |
|3  | [什么是JSX？](#什么是JSX) |
|4  | [元素和组件有什么区别？](#元素和组件有什么区别) |
|5  | [如何在React中创建组件？](#如何在React中创建组件) |
|6  | [何时使用ClassComponent替函FunctionComponent？](#何时使用ClassComponent替函FunctionComponent) |
|7  | [什么是PureComponents？](#什么是PureComponents) |
|8  | [React中state是什么？](#React中state是什么) |
|9  | [React中porps是什么？](#React中porps是什么) |
|10 | [state和porps的区别？](#state和porps的区别) |
|11 | [为什么不应该直接更新state？](#为什么不应该直接更新state) |
|12 | [回调函数作为setState()参数的目的是什么？](#回调函数作为setState()参数的目的是什么)
|13 | [HTML和React事件绑定的区别是什么？](#HTML和React事件绑定的区别是什么) |
|14 | [如何在JSX回调中绑定方法或事件绑定？](#如何在JSX回调中绑定方法或事件绑定) |
|15 | [如何向事件绑定或回调中传递一个参数？](#如何向事件绑定或回调中传递一个参数) |
|16 | [React中合成事件是什么？](#React中合成事件是什么) |
|17 | [什么是内联条件表达式？](#什么是内联条件表达式) |
|18 | [什么是key属性，在数组中使用它们的好处是什么？](#什么是key属性在数组中使用它们的好处是什么) |
|19 | [refs有什么用？](#refs有什么用) |
|20 | [如何创建refs？](#如何创建refs) |  
|21 | [什么是 forward refs？](#什么是forward-refs) |
|22 | [在refs回调函数和findDOMNode()应该首选哪一个？](#在refs回调函数和findDOMNode()应该首选哪一个) |
|23 | [为什么曾经refs是String类型？](#为什么曾经refs是String类型) |
|24 | [什么是虚拟DOM？](#什么是虚拟DOM) |
|25 | [虚拟DOM是如何工作的？](#虚拟DOM是如何工作的) |
|26 | [Shadow DOM 和 Virtual DOM 的区别？](#Shadow-DOM和Virtual-DOM的区别) |
|27 | [React Fiber 是什么？](#React-Fiber是什么) |
|28 | [React Fiber 出现的主要目的是什么？](#ReactFiber出现的主要目的是什么) |
|29 | [什么是受控组件？](#什么是受控组件) |
|30 | [什么是非受控组件？](#什么是非受控组件) |
|31 | [createElement 和 cloneElement 的区别](#createElement和cloneElement的区别) |
|32 | [React 中 State 提升是什么？](#React中State提升是什么) |
|33 | [组件生命周期的不同阶段是什么？](#组件生命周期的不同阶段是什么) |
|34 | [React 生命周期方法是什么？](#React生命周期方法是什么) |
|35 | [什么是高阶组件？](#什么是高阶组件) |
|36 | [如何创建高阶组件的 props 代理？](#如何创建高阶组件的props代理) |
|37 | [什么是 context？](#什么是context) |
|38 | [什么是 children porp？](#什么是childrenporp) |
|39 | [在 react 中怎么写注释？](#在react中怎么写注释) |
|40 | [使用带 props 参数的 super 构造函数的目的是什么？](#使用带props参数的super构造函数的目的是什么) |
|41 | [什么是 reconciliation？](#什么是reconciliation) |
|42 | [如何使用动态 key 值设置state？](#如何使用动态key值设置state) |
|43 | [每次渲染时每次调用函数的常见错误是什么？](#每次渲染时每次调用函数的常见错误是什么) |
|44 | [为什么必须大写组件名称？](#为什么必须大写组件名称) |
|45 | [React 为什么使用 `className` 代替 `class` 属性？](#React为什么使用className代替class属性) |
|46 | [什么是 fragments？](#什么是fragments) |
|47 | [为什么 fragments 比 div 容器好？](#为什么fragments比div容器好) |
|48 | [React 中 portals 是什么？](#React中portals是什么) |
|49 | [什么是无状态组件？](#什么是无状态组件) |
|50 | [什么是有状态组件？](#什么是有状态组件) |
|51 | [React 中如何对 props 进行验证？](#React中如何对props进行验证) |
|52 | [React的优点是什么？](#React的优点是什么) |
|53 | [React 的局限是什么？](#React的局限是什么) |
|54 | [React V16 中错误边界是什么](#ReactV16中错误边界是什么) |
|55 | [React v15中如何处理错误边界？](#Reactv15中如何处理错误边界) |
|56 | [什么是 static 类型检查的推荐方法？](#什么是static类型检查的推荐方法) |
|57 | [react-dom 包的用途是什么？](#react-dom包的用途是什么) |
|58 | [react-dom render 方法的目的是什么？](#react-dom-render方法的目的是什么) |
|59 | [什么是 ReactDOMServer？](#什么是ReactDOMServer) |
|60 | [如何在 React 中使用 innerHTML？](#如何在React中使用innerHTML) |
|61 | [如何在 React 中使用 style？](#如何在React中使用style) |
|62 | [React 中事件有什么不同？](#React中事件有什么不同) |
|63 | [在 constructor 中使用 setState() 会发生什么？](#在constructor中使用setState()会发生什么) |
|64 | [数组索引作为keys的影响是什么？](#数组索引作为keys的影响是什么) |
|65 | [在 componentWillMount() 方法中使用 setState() 好么？](#在componentWillMount()方法中使用setState()好么) |
|66 | [如果在初始化 state 时使用 porps 会发生什么？](#如果在初始化state时使用porps会发生什么) |
|67 | [如何根据条件渲染组件？](#如何根据条件渲染组件)
|68 | [为什么在dom元素上展开props时要注意？](#为什么在dom元素上展开props时要注意) |
|69 | [React 怎么使用修饰器？](#React怎么使用修饰器) |
|70 | [你如何记忆一个组件？](#你如何记忆一个组件) |
|71 | [如何实现服务器端呈现或SSR？](#如何实现服务器端呈现或SSR) |
|72 | [React 怎么开启 production 模式？](#React怎么开启production模式) |
|73 | [什么是CRA及其好处？](#什么是CRA及其好处) |
|74 | [挂载阶段生命周期方法的顺序是什么？](#挂载阶段生命周期方法的顺序是什么) |
|75 | [React v16 什么生命周期方法不赞同使用？](#React-v16什么生命周期方法不赞同使用) |
|76 | [getDerivedStateFromProps() 生命周期的目的是什么？](#getDerivedStateFromProps()生命周期的目的是什么) |
|77 | [getSnapshotBeforeUpdate() 生命周期方法的目的是什么？](#getSnapshotBeforeUpdate()生命周期方法的目的是什么) |
|78 | [createElement() 和 cloneElement() 不同？](#createElement()和cloneElement()不同) |
|79 | [推荐的命名组件的方法是什么？](#推荐的命名组件的方法是什么) |
|80 | [组件类中方法的推荐顺序是什么？](#组件类中方法的推荐顺序是什么) |
|81 | [什么是 switching 组件？](#什么是switching组件) |
|82 | [为什么需要给 setState() 传递函数？](#为什么需要给setState()传递函数) |
|83 | [React 严格模式是是什么？](#React严格模式是是什么) |
|84 | [什么是 React Mixins？](#什么是React-Mixins) |
|85 | [为什么 ismounted() 是反模式，正确的解决方案是什么？](#为什么ismounted()是反模式，正确的解决方案是什么) |
|86 | [React中支持哪些指针事件？](#React中支持哪些指针事件) |
|87 | [为什么组件名字首字母需要大写？](#为什么组件名字首字母需要大写) |
|88 | [React v16 支持自定义 DOM 属性么？](#React-v16支持自定义DOM属性么) |
|89 | [constructor 和 getInitialState 区别？](#constructor和getInitialState区别) |
|90 | [是否可以在不调用setState的情况下强制组件重新呈现？](#是否可以在不调用setState的情况下强制组件重新呈现) |
|91 | [React 使用 ES6 类 super() 和 super(props) 区别是什么？](#React使用ES6类super()和super(props)区别是什么) |
|92 | [如何在JSX中循环？](#如何在JSX中循环) |
|93 | [如何访问属性引号中的属性？](#如何访问属性引号中的属性) |
|94 | [React proptype 数组形状？](#React-proptype数组形状) |
|95 | [如何按条件应用className属性？](#如何按条件应用className属性) |
|96 | [React 和 ReactDOM 的区别是什么？](#React和ReactDOM的区别是什么) |
|97 | [为什么 ReactDOM 从 React 中分离？](#为什么ReactDOM从React中分离) |
|98 | [如何使用 React label 元素？](#如何使用React-label元素) |
|99 | [怎么组合多个内联样式对象？](#怎么组合多个内联样式对象) |
|100| [如何在浏览器缩放时重渲染视图？](#如何在浏览器缩放时重渲染视图) |
|101| [setState 和 replaceState 方法的却别是什么？](#setState和replaceState方法的却别是什么) |
|102| [如何监听 state 改变？](#如何监听state改变) |
|103| [React state 下移除数组元素的建议方法是什么？](#React-state下移除数组元素的建议方法是什么) |
|104| [是否可以在不渲染HTML的情况下使用React？](#是否可以在不渲染HTML的情况下使用React) |
|105| [React 如何优雅的打印 JSON？](#React-如何优雅的打印-JSON) |
|106| [为什么 React 不能更新 prop？](#为什么React不能更新prop) |
|107| [页面加载时如何让 input 元素获取焦点？](#页面加载时如何让input元素获取焦点) |
|108| [是否可以更新 state 中的对象（Object）？](#是否可以更新state中的对象（Object）) |
|109| [为什么函数是 `setState()` 中覆盖object 建议的方法？](#为什么函数是setState()中覆盖object建议的方法) |
|110| [如何在浏览器中找到运行时的react版本？](#如何在浏览器中找到运行时的react版本) |
|111| [在你的 create react 应用中加入 polyfill 的方法是什么？](#在你的create-react应用中加入polyfill的方法是什么？) |
|112| [如何在create react app中使用https而不是http？](#如何在create-react-app中使用https而不是http) |
|113| [如何避免在create react app中使用相对路径导入？](#如何避免在create-react-app中使用相对路径导入) |
|114| [如何为React路由器添加谷歌分析？](#如何为React路由器添加谷歌分析) |
|115| [如何每秒更新组件？](#如何每秒更新组件) |
|116| [如何在内联样式中添加浏览器前缀？](#如何在内联样式中添加浏览器前缀) |
|117| [如何使用 React 和 ES6 导入导出组件？](#如何使用React-and-ES6导入导出组件) |
|118| [为什么React组件名称必须以大写字母开头？](#为什么React组件名称必须以大写字母开头) |
|119| [为什么组件的 constructor 只被调用一次？](#为什么组件的constructor只被调用一次) |
|120| [如何定义react中的常量？](#如何定义react中的常量) |
|121| [如何在React中以编程方式触发单击事件？](#如何在React中以编程方式触发单击事件) |
|122| [是否可以在普通的react中使用async/await？](#是否可以在普通的react中使用async/await) |
|123| [React的常见文件夹结构是什么？](#React的常见文件夹结构是什么) |
|124| [动画的流行库是什么？](#动画的流行库是什么) |
|125| [样式模块的好处是什么？](#样式模块的好处是什么) |
|126| [什么语法风格检测是 React 中受欢迎的？](#什么语法风格检测是React中受欢迎的) |
|127| [如何进行Ajax调用以及应该在哪些组件生命周期方法中进行Ajax调用？](#如何进行Ajax调用以及应该在哪些组件生命周期方法中进行Ajax调用？) |
|128| [什么是 render props？](#什么是render-props) |
|   | **React Router** |
|129| [什么是 React Router？](#什么是React-Router) |
|130| [React Router 与 history 库有什么不同？](#React-Router与history库有什么不同) |
|131| [React Router v4 中 /<Router> 组件是什么？](#React-Router-v4中<Router>组件是什么) |
|132| [push()和replace()方法用于history的目的是什么？](#push()和replace()方法用于history的目的是什么) |
|133| [如何使用React-Router-v4以编程方式导航？](#如何使用React-Router-v4以编程方式导航) |
|134| [如何在 React Router v4 获取查询参数？](#如何在React-Router-v4获取查询参数) |
|135| [为什么收到 Router 可能只有一个子元素警告？](#为什么收到Router可能只有一个子元素警告) |
|136| [React Router v4 中如何向 `history.push` 方法中传递参数？](#React-Router-v4中如何向history.push方法中传递参数) |
|137| [如何实现默认或未找到页？](#如何实现默认或未找到页) |
|138| [如何在 React Router v4 中获取 history？](#如何在React-Router-v4中获取history) |
|139| [如何在登录后执行自动重定向？](#如何在登录后执行自动重定向) |
|   | **React 国际化** |
|140| [什么是 React Intl?](#什么是React-Intl) |
|141| [React Intl 主要特性是什么?](#React-Intl主要特性是什么) |
|142| [React Intl 中两种格式化的方式是什么?](#React-Intl中两种格式化的方式是什么) |
|143| [React Intl 中如何使用 `<FormattedMessage>` 作为 placeholder?](#React-Intl中如何使用FormattedMessage作为placeholder) |
|144| [如何使用 React Intl 访问当前区域设置？](#如何使用React-Intl访问当前区域设置) |
|145| [如何使用 React Intl 格式化日期?](#如何使用React-Intl格式化日期) |
|   | **React Testing** |
|146| [React 测试中什么是 Shallow Renderer ?](#React测试中什么是Shallow-Renderer) |
|147| [React 中 TestRenderer 包是什么?](#React中TestRenderer包是什么) |
|148| [ReactTestUtils 包的目的是什么?](#ReactTestUtils包的目的是什么) |
|149| [什么是 Jest?](#什么是Jest) |
|150| [Jest 比 Jasmine有什么好处?](#Jest比Jasmine有什么好处) |
|151| [给出一个简单的Jest测试用例示例](#给出一个简单的Jest测试用例示例) |

## React 核心

1. ### 什么是React？

    React 是一个 **开源前端JavaScript库** 用于构建用户界面， 尤其是单页面应用程序。他被用于处理 web 和 移动 app 的视图层。 React 是由Facebook 的软件工程师 Jordan Walke 所创立的. React于2011年首次部署在Facebook的News Feed上，2012年首次部署在Instagram上。

2. ### React主要特点是什么？

    React 主要特点是:

    * 考虑到RealDOM操作很昂贵，它使用 **VirtualDOM** 而不是 RealDOM 。
    * 支持 **服务器端渲染**。
    * 遵循 **单向** 数据流或数据绑定。
    * 使用 **可重用/可组合的** UI 组件来开发视图。

3. ### 什么是JSX？

    *JSX* 是 ECMAScript 的类似XML的语法扩展 (是 *JavaScript XML* 首字母缩略词). 基本上它只是为 `React.createElement()` 函数提供语法糖, 给我们提供一种 JavaScript 和 HTML 在一起使用的类模板.

    In the example below text inside `<h1>` tag return as JavaScript function to the render function.
    在下面的示例中，`<h1>`标签和其中的文本，作为 JavaScript 函数 在render 函数中被返回。

    ```jsx harmony
    class App extends React.Component {
      render() {
        return(
          <div>
            <h1>{'Welcome to React world!'}</h1>
          </div>
        )
      }
    }
    ```

4. ### 元素和组件有什么区别？

    一个 *Element* 描述 DOM 节点和其他组件如何按你想要的出现在屏幕上的纯对象。 *Elements* 可以包含其他的 *Elements* 在它们的props 中. 创建一个React 元素很方便. 一旦创建了一个元素，它不再会发生改变。

    React Element的对象表示如下：:

    ```javascript
    const element = React.createElement(
      'div',
      {id: 'login-btn'},
      'Login'
    )
    ```

    上面 `React.createElement()` 函数返回一个对象:

    ```
    {
      type: 'div',
      props: {
        children: 'Login',
        id: 'login-btn'
      }
    }
    ```

    最后它使用 `ReactDOM.render()` 函数去渲染DOM:

    ```html
    <div id='login-btn'>Login</div>
    ```

    而 **组件** 可以用不同的方式声明，它可以使一个用 `render()` 方法的类。 或者简单的定义为一个函数. 无论怎样他都会接受传入的props, 并返回一个 JSX 树:

    ```javascript
    const Button = ({ onLogin }) =>
      <div id={'login-btn'} onClick={onLogin} />
    ```

    然后JSX转化为 `React.createElement()` 函数树:

    ```javascript
    const Button = ({ onLogin }) => React.createElement(
      'div',
      { id: 'login-btn', onClick: onLogin },
      'Login'
    )
    ```

5. ### 如何在React中创建组件？

    有两种可能的方法来创建组件.

    1. **Function Components:** 这是创建组件的最简单方法. 这些是纯JavaScript函数，它们接受props对象作为第一个参数并返回React元素：

        ```jsx harmony
        function Greeting({ message }) {
          return <h1>{`Hello, ${message}`}</h1>
        }
        ```

    2. **Class Components:** 您还可以使用ES6类来定义组件。上面的函数组件可以写成：

        ```jsx harmony
        class Greeting extends React.Component {
          render() {
            return <h1>{`Hello, ${this.props.message}`}</h1>
          }
        }
        ```

6. ### 何时使用ClassComponent替函FunctionComponent？

    如果组件需要 *内部状态（state）或生命周期方法 * 则使用类组件，否则使用函数组件。

7. ### 什么是PureComponents？

    *`React.PureComponent`* 与 *`React.Component`* 极为相似， 除了处理了 `shouldComponentUpdate()` 方法，当 props 或state 改变, *PureComponent* 将会浅层比较 state 和 props。另一方面， *Component*  在输出的时候不会比较porps 和 state, 因此，无论何时 `shouldComponentUpdate` 被调用组件总会重新渲染。

8. ### React中state是什么？

    组件的 *State（状态）* 是一个对象，在组件的整个生命周期中保存一些可能改变的信息。 组件状态应该尽可能的简单，尽可能使有状态组件数量最小。 让我们创建一个具有消息状态的用户组件，


    ```jsx harmony
    class User extends React.Component {
      constructor(props) {
        super(props)

        this.state = {
          message: 'Welcome to React world'
        }
      }

      render() {
        return (
          <div>
            <h1>{this.state.message}</h1>
          </div>
        )
      }
    }
    ```

    ![state](image/state.jpg)

9. ### React中porps是什么？

    *Props* 是组件传入的属性. 它们是单个值或包含一组值的对象，创建时使用类似于HTML标记属性的命名约定传入到组件中.它们是从父组件传递到子组件的数据。

    React中props的主要目的是提供以下组件功能：

    1. 将自定义数据传递给您的组件。
    2. 触发状态更改。
    3. 通过 `this.props.reactProp` 在组件 `render()` 方法中使用.

    例如，让我们创建一个具有reactProp属性的元素：

    ```jsx harmony
    <Element reactProp={'1'} />
    ```

    `reactProp` (无论起任何名字) 会被附加到 React 组件 props 属性中，所有由 React 库创建出来的组件都会有porps 属性。

    ```
    props.reactProp
    ```

10. ### state和porps的区别？

    *props* 和 *state* 都是 javascript 纯对象. 他们都保存影响渲染的数据, 但它们在组件方面的功能却不同。 Props 类似于函数参数传递给组件， 而 state 类似于函数中声明的变量在组件内部中管理。

11. ### 为什么不应该直接更新state？

    为什么不应该直接更新state，那么它不会重新渲染组件.

    ```javascript
    //错误
    this.state.message = 'Hello world'
    ```

    使用 `setState()` 方法代替. 他会为组件的state对象计划（安排）更新. 当state改变, 组件会重新渲染。

    ```javascript
    //正确
    this.setState({ message: 'Hello World' })
    ```

    **提示:**你可以使用 *constructor* 或javascript最新class声明语法中的任意一个，直接指定state对象。

12. ### 回调函数作为setState()参数的目的是什么？

    当setState执行完成，回调函数会被执行，而且组件会被重新渲染。 因 `setState()` 是 **异步的** 所以回调函数被用来发起一些请求。

    **提示:** 推荐使用生命周期函数而不是使用回调函数

    ```javascript
    setState({ name: 'John' }, () => console.log('The name has updated and component re-rendered'))
    ```

13. ### HTML和React事件绑定的区别是什么？

    1. HTML中时间名字必须是 *小写*:

    ```html
    <button onclick='activateLasers()'>
    ```

    然而React中遵循 *驼峰命名* 约定:

    ```jsx harmony
    <button onClick={activateLasers}>
    ```

    2. HTML中可以返回 `false` 阻止默认行为:

    ```html
    <a href='#' onclick='console.log("The link was clicked."); return false;' />
    ```

    然而React中必须明确调用 `preventDefault()`:

    ```javascript
    function handleClick(event) {
      event.preventDefault()
      console.log('The link was clicked.')
    }
    ```

14. ### 如何在JSX回调中绑定方法或事件绑定？

    有3中可行的方法达到目的:

    1.	**Constructor中绑定:** 在javascript的class中, 方法默认不会绑定执行上下文. 在React的事件绑定中也是同样的. 通常在constructor中绑定.

    ```javascript
    class Component extends React.Componenet {
      constructor(props) {
        super(props)
        this.handleClick = this.handleClick.bind(this)
      }

      handleClick() {
        // ...
      }
    }
    ```

    2. **Public class fields syntax（类的字段语法）:** 如果你不喜欢bind方法，那么 *public class fields syntax（类的字段语法）* 可以正确的绑定回调。

    ```jsx harmony
    handleClick = () => {
      console.log('this is:', this)
    }
    ```

    ```jsx harmony
    <button onClick={this.handleClick}>
      {'Click me'}
    </button>
    ```

    3. **回调中的箭头函数:** 你可以在回调函数中直接使用 *箭头函数*.

    ```jsx harmony
    <button onClick={(event) => this.handleClick(event)}>
      {'Click me'}
    </button>
    ```

    **提示:** 如果回调函数作为属性传递到组件, 这些组件可能会不必要的重新渲染. 鉴于此,考虑到性能问题， 使用`.bind()` 或 *public class fields syntax（类的字段语法）* 是首选的.

15. ### 如何向事件绑定或回调中传递一个参数？

    可以使用 *箭头函数* 包裹一个 *事件绑定函数* 并传入参数:

    ```jsx harmony
    <button onClick={() => this.handleClick(id)} />
    ```

    这相当于调用 `.bind`:

    ```jsx harmony
    <button onClick={this.handleClick.bind(this, id)} />
    ```

16. ### React中合成事件是什么？

    ```合成事件` 是浏览器原生事件跨浏览器进行了封装的事件. 它的API与浏览器原生事件相似, 包括 `stopPropagation()` 和 `preventDefault()`, except the events work identically across all browsers.

17. ### 什么是内联条件表达式？

    JS中提供了条件表达式，你可以使用 *if 声明* 或 *三元表达式* . 除了这些方法, 你也可以JS逻辑运算符`&&`在JSX中嵌入一些表达式。

    ```jsx harmony
    <h1>Hello!</h1>
    {
      messages.length > 0 &&
      <h2>
        You have {messages.length} unread messages.
      </h2>
    }
    ```

    <!-- TODO: fix this section -->

18. ### 什么是key属性，在数组中使用它们的好处是什么？

    `key` 是一个特殊的string属性，在创建数组元素的时候你 **应该** 包含它们 . *Keys* 帮助React确认哪一项发生改变,加入,或移除。

    多数时候使用数据中的id作为 *keys*:

    ```jsx harmony
    const todoItems = todos.map((todo) =>
      <li key={todo.id}>
        {todo.text}
      </li>
    )
    ```

    当没有稳定的ID用作每一项渲染时, 也可以使用数组的 *索引* 当作 *key*，作为最后的选择:

    ```jsx harmony
    const todoItems = todos.map((todo, index) =>
      <li key={index}>
        {todo.text}
      </li>
    )
    ```

    **提示:**

    1. 使用 *索引* 作为 *key* 是 **不推荐** 的。如果每一项的先后顺序改变. 会对性能有副作用并可能导致组件状态的问题。
    2. 如果将列表中的一项提取为单独的组件， 那么在组件上使用 *keys* 来代替 `li` 标签.
    3. 如果`key`属性在列表项中不存在，在控制台会报出错误.

19. ### refs有什么用？

    *ref* 用来返回一个元素的引用. 大多用情况 *应该避免使用*,当需要直接的操作DOM元素或组件实例时它们会非常有用。

20. ### 如何创建refs？

    有两种方法。
    1. 这是不久前才加入的方法. *Refs* 使用 `React.createRef()` 方法创建， 通过 `ref` 属性被附加到React元素上. 为了在组件中随处使用 *refs*, 只要把 *ref* 赋给组件构造函数的实例属性。

    ```jsx harmony
    class MyComponent extends React.Component {
      constructor(props) {
        super(props)
        this.myRef = React.createRef()
      }
      render() {
        return <div ref={this.myRef} />
      }
    }
    ```
    2. 也可以使用ref回调函数方法，无论在什么React版本中. 例如, SearchBar 组件获取Input元素，如下,
    ```jsx harmony
    class SearchBar extends Component {
       constructor(props) {
          super(props);
          this.txtSearch = null;
          this.state = { term: '' };
          this.setInputSearchRef = e => {
             this.txtSearch = e;
          }
       }
       onInputChange(event) {
          this.setState({ term: this.txtSearch.value });
       }
       render() {
          return (
             <input
                value={this.state.term}
                onChange={this.onInputChange.bind(this)}
                ref={this.setInputSearchRef} />
          );
       }
    }
    ```

    函数式组件中也可以通过闭包使用 *refs*
    **提示**: 你也可是使用内联的ref回调函数，虽然他不是推荐的方法。

21. ### 什么是 forward refs？

    *Ref forwarding* 是一个新特性， 让一些组件获得到接受的 *ref*, 并把它进一步传递到下层的子组件中.

    ```jsx harmony
    const ButtonElement = React.forwardRef((props, ref) => (
      <button ref={ref} className="CustomButton">
        {props.children}
      </button>
    ));

    // Create ref to the DOM button:
    const ref = React.createRef();
    <ButtonElement ref={ref}>{'Forward Ref'}</ButtonElement>
    ```

22. ### 在refs回调函数和findDOMNode()应该首选哪一个？

    应该优先使用 *callback refs* 而不是 `findDOMNode()`. 为了预防 `findDOMNode()` 在将来的 React 版本中发生改变

    `findDOMNode` 一般的使用方法:

    ```javascript
    class MyComponent extends Component {
      componentDidMount() {
        findDOMNode(this).scrollIntoView()
      }

      render() {
        return <div />
      }
    }
    ```

    推荐的使用方法:

    ```javascript
    class MyComponent extends Component {
      componentDidMount() {
        this.node.scrollIntoView()
      }

      render() {
        return <div ref={node => this.node = node} />
      }
    }
    ```

23. ### 为什么曾经refs是String类型？

    如果曾经在工作中使用过React, 你可能轻车熟路的一个过时的API就是 String 类型的 `ref` 属性， 像 `ref={'textInput'}`, 和 通过像 `this.refs.textInput` 的方式引用. 我们强烈反对它因为 *String 类型的 refs 有以下问题*, 他们在过去被反复确认过. String 类型的refs  **已经在 React V16 版本中被移除**.

    1. 它们 *迫使 React 与当前正在执行的组件保持联系*. 这是有问题的， 因为它使得 React 模块有状态, 因此 React 模块在打包过程中被复制时，会产生意想不到的问题.
    2. 它们是 *不可合并的* — 如果一个库把 ref 放在被传入的子元素上,使用者不能把另一个 ref 再放在上面. refs 回调函数是完美的可合并的。
    3. 它们像 Flow 一样 *在静态分析时并不工作* .Flow 无法推测框架想让字符串类型 ref 出现在 `this.refs` 上。 因此，他的类型可能不同. refs 回调函数对静态分析是友好的.
    4. 大多数人使用类似 "回调函数" 时，并不会像期待中的那样工作。 (例如 <DataGrid renderRow={this.renderRow} />)
       ```jsx harmony
       class MyComponent extends Component {
         renderRow = (index) => {
           // This won't work. Ref will get attached to DataTable rather than MyComponent:
           return <input ref={'input-' + index} />;

           // This would work though! Callback refs are awesome.
           return <input ref={input => this['input-' + index] = input} />;
         }

         render() {
           return <DataTable data={this.props.data} renderRow={this.renderRow} />
         }
       }
       ```
24. ### 什么是虚拟DOM？

    *虚拟DOM* (VDOM) 是内存中 *真实DOM* 的映射. UI的表现保存在内存中，并与“真实”DOM同步。他是发生在渲染函数被调用和在屏幕中展现元素之间的一步。 这一完整的过程称为 *reconciliation*.

25. ### 虚拟DOM是如何工作的？

    *虚拟DOM* 工作的三个简单步骤.

    1. 无论何时一些底层的数据改变, 全部UI都会在虚拟DOM表示中重新呈现。。
        ![vdom](image/vdom1.png)

    2. 然后计算前一个DOM表现和新DOM表现之间的差异。
        ![vdom2](image/vdom2.png)

    3. 一旦计算完成，真实 DOM 只会更新确实被改变的部分。
        ![vdom3](image/vdom3.png)

26. ### Shadow DOM 和 Virtual DOM 的区别？

    *Shadow DOM* 浏览器技术为在 *web components* 中变量和css作用域主要设计的。 *Virtual DOM* 是JavaScript库在浏览器API 上贯彻的理念。

27. ### 什么事React Fiber？

    Fiber 是React 16 中新的协调引擎或核心算法的重新实现。React Fiber的目标是提高其在诸如动画、布局、手势、暂停和中止的能力等领域的性能，重用工作并为不同类型的更新分配优先级; and new concurrency primitives.

28. ### ReactFiber出现的主要目的是什么？

    React Fiber 的目标是提高其在动画，布局，手势，等领域的性能. 首要的特点是 **增量渲染**: 可以把渲染工作切割成多k块，在多个画面中进行渲染.

29. ### 什么是受控组件？

    在用户输入后控制（劫持）了表单中的输入元素的组件叫做 **受控组件**, 即, 每一个 state 的改变都会有相关的处理函数

    例如, 把名字全部写为大写字母, 使用像下面的处理,

    ```javascript
    handleChange(event) {
      this.setState({value: event.target.value.toUpperCase()})
    }
    ```

30. ### 什么是非受控组件？

    **非受控组件** 是那些在自己内部存储状态的组件, 当你需要时，通过使用 ref 访问元素找到当前的值。这有点像传统的HTML。

    UserProfile 组件中, `name` 输入使用 ref 接入.

    ```jsx harmony
    class UserProfile extends React.Component {
      constructor(props) {
        super(props)
        this.handleSubmit = this.handleSubmit.bind(this)
        this.input = React.createRef()
      }

      handleSubmit(event) {
        alert('A name was submitted: ' + this.input.current.value)
        event.preventDefault()
      }

      render() {
        return (
          <form onSubmit={this.handleSubmit}>
            <label>
              {'Name:'}
              <input type="text" ref={this.input} />
            </label>
            <input type="submit" value="Submit" />
          </form>
        );
      }
    }
    ```

    一般情况下, 推荐使用受控组件实现表单.
31. ### createElement 和 cloneElement 的区别？

    JSX 元素将会被编译成 `React.createElement()` 函数用来创建 react 元素，他们将用于UI的对象表示. 然而， `cloneElement` 用来克隆一个元素并传入新的props.

32. ### React 中 State 提升是什么？

    当几个组件需要共享相同的可变数据时，建议 *提升共享状态* 到它们最近的公共祖先元素. 意味着如果两个子组件共享相同的数据时来自他们的父元素。 把状态移动到父元素代替在每个子元素中都有自己的状态。

33. ### 组件生命周期的不同阶段是什么？

    组件生命周期有四个不同阶段.

    1. **Initialization（初始化）:** 组件准备设置初始化 state 和 默认的 props.

    2. **Mounting（挂载）:** 组件随时可以在浏览器元素中挂载. 这个阶段包括 `componentWillMount()` 和 `componentDidMount()` 生命周期方法.

    3. **Updating（更新）:**  组件通过两种方式更新, 发送新的props 和 更新state. 这个阶段包括 `shouldComponentUpdate()`, `componentWillUpdate()` 和 `componentDidUpdate()` 生命周期方法.

    4. **Unmounting（卸载）:** 组件不再需要，从浏览器DOM中被卸载. 这个阶段包括 `componentWillUnmount()` 生命周期方法.
        ![phases](image/phases.png)

    <!-- TODO: new lifecycle methods in React v16 -->

34. ### React 生命周期方法是什么？

    - **componentWillMount:** 在渲染前执行，在根组件中用作App级别的配置。
    - **componentDidMount:** 在第一次渲染后执行，这里应该发生，所有的请求，元素、state 更新,事件监听。
    - **componentWillReceiveProps:** 当某些props更新触发了state的改变时执行。
    - **shouldComponentUpdate:** 决定组件是否更新. 默认返回true.在 state 或 props 更新后如果确定组件不需要冲渲染可以返回false.这是一个提升性能非常好的地方，因为它可以让你在组件接收到新的props避免重新渲染。
    - **componentWillUpdate:** 在重渲染前执行，如果有通过 `shouldComponentUpdate()` 确认的state 或 props 的改变，返回true.
    - **componentDidUpdate:** 大多数使用它在prop 或 state 改变时响应更新DOM。
    - **componentWillUnmount:** 它将用于取消任何传出的网络请求，或移除所有组件应该绑定的事件监听函数。

    <!-- TODO: new lifecycle methods in React v16 -->

35. ### 什么是高阶组件？

    *高阶组件* (*HOC*) 是一个接受组件并返回新组件的函数. 基本上,它是从React 组合特定中派生的一种模式。

    可以叫它们 **pure components** 因为它们可以接受任何动态提供的子组件，它们不会修改或复制来自输入组件的任何行为。

    ```javascript
    const EnhancedComponent = higherOrderComponent(WrappedComponent)
    ```

    HOC 可以在很多场景中使用:

    1. 代码重用、逻辑 和 bootstrap abstraction。
    2. 渲染劫持。
    3. 状态抽象和控制。
    4. Props 控制。

36. ### 如何创建高阶组件的 props 代理？

    你可以通过组件中使用 *props 代理* 的形式添加或编辑 props:

    ```jsx harmony
    function HOC(WrappedComponent) {
      return class Test extends Component {
        render() {
          const newProps = {
            title: 'New Header',
            footer: false,
            showFeatureX: false,
            showFeatureY: true
          }

          return <WrappedComponent {...this.props} {...newProps} />
        }
      }
    }
    ```

37. ### 什么是 context？

    *Context* 规定一种方法，穿过组件数传递数据，不需要在每个层级手动的把 props 传递下去。例如, 有效用户, locale preference, UI 主题在程序的很多组件中都需要接入。

    ```javascript
    const {Provider, Consumer} = React.createContext(defaultValue)
    ```

38. ### 什么是 children porp？

    *Children* 是一个 prop (`this.prop.children`)，允许把组件作为数据传递给其他组件, 就像使用其他的 props 一样. 组件树将把起始标签，闭合标签中间的内容作为 `children` prop 传递给其他组件。
    这有许多 React API 中的方法，对这个 prop 适用. 包括 `React.Children.map`, `React.Children.forEach`, `React.Children.count`, `React.Children.only`, `React.Children.toArray`.

    ```jsx harmony
    const MyDiv = React.createClass({
      render: function() {
        return <div>{this.props.children}</div>
      }
    })

    ReactDOM.render(
      <MyDiv>
        <span>{'Hello'}</span>
        <span>{'World'}</span>
      </MyDiv>,
      node
    )
    ```

39. ### 在 react 中怎么写注释？

    React/JSX 的注释于 JavaScript 多行注释很相似但要放在花括号中。

    **单行注释:**

    ```jsx harmony
    <div>
      {/* 单行注释(在通常的Javascript中, 单行注释使用两个反斜线(//)) */}
      {`Welcome ${user}, let's play React`}
    </div>
    ```

    **多行注释:**

    ```jsx harmony
    <div>
      {/* 多行
       注释 */}
      {`Welcome ${user}, let's play React`}
    </div>
    ```

40. ### 使用带 props 参数的 super 构造函数的目的是什么？

     子类构造函数在调用 `super()` 方法之前不能使用 `this` 引用。同样适用于ES6子类.传递参数到 `super()` 执行的主要原因是在子构造函数中获得 `this.props`.

    **传递Porps:**

    ```javascript
    class MyComponent extends React.Component {
      constructor(props) {
        super(props)

        console.log(this.props) // prints { name: 'John', age: 42 }
      }
    }
    ```

    **没有传递Porps**

    ```javascript
    class MyComponent extends React.Component {
      constructor(props) {
        super()

        console.log(this.props) // prints undefined

        // but props parameter is still available
        console.log(props) // prints { name: 'John', age: 42 }
      }

      render() {
        // no difference outside constructor
        console.log(this.props) // prints { name: 'John', age: 42 }
      }
    }
    ```

    上面代码显示 `this.props` 只在构造函数中是不同的.在构造函数之外是一样的。

41. ### 什么是 reconciliation？

    当一个组件的 props 或 state 改变,React通过比较新返回的元素和先前呈现的元素来确定是否需要实际的DOM更新。当他们不相同, react 将会更新DOM. 这一过程被叫做 *reconciliation*.

42. ### 如何使用动态 key 值设置state？

    如果你使用 ES6 或 Babel 转换器转换你的 JSX, 那么你可以使用 *computed property names* 完成.

    ```javascript
    handleInputChange(event) {
      this.setState({ [event.target.id]: event.target.value })
    }
    ```

43. ### 每次渲染时每次调用函数的常见错误是什么？

    你需要清楚的是，函数作为参数传递时没有被调用。

    ```jsx harmony
    render() {
      // 错误: handleClick 已经执行，替换了作为引用传递!
      return <button onClick={this.handleClick()}>{'Click Me'}</button>
    }
    ```

    相反，不带括号传递函数本身:

    ```jsx harmony
    render() {
      // 正确: handleClick 作为引用传递!
      return <button onClick={this.handleClick}>{'Click Me'}</button>
    }
    ```

44. ### 为什么必须大写组件名称？

    这是必须的，因为组件不是DOM元素，他们是构造函数. 同样, 在 JSX  中小写标签名代表 HTML 元素，不是组件.

45. ### React 为什么使用 `className` 代替 `class` 属性？

    `class` 在Javascript中是一个关键字, JSX 是 JavaScript 的扩展. 这是 React 为什么使用 `className` 代替`class` 的主要原因. 传递一个 String 类型 `className` 属性.

    ```jsx harmony
    render() {
      return <span className={'menu navigation-menu'}>{'Menu'}</span>
    }
    ```
46. ### 什么是 fragments？

    这是React中的通用模式，用于组件返回多个元素。*Fragments* 允许在不向DOM添加额外节点的情况下对子节点列表进行分组。

    ```jsx harmony
    render() {
      return (
        <React.Fragment>
          <ChildA />
          <ChildB />
          <ChildC />
        </React.Fragment>
      )
    }
    ```

    还有*更短的语法*，但是许多工具不支持它：

    ```jsx harmony
    render() {
      return (
        <>
          <ChildA />
          <ChildB />
          <ChildC />
        </>
      )
    }
    ```

47. ### 为什么 fragments 比 div 容器好？

    1. Fragments 会更快一点，不需要创建额外的DOM节点使用更少的内存. 这只对大树和深树有真正的好处。
    2. 一些CSS机制 *Flexbox* 和 *CSS Grid* 有特殊的父子关系, 在中间添加div使得很难保持所需的布局。
    3. DOM检查器会更清晰。

48. ### React 中 portals 是什么？

    *Portal* 是将子节点呈现到存在于父组件的DOM层次结构之外的DOM节点的推荐方法。

    ```javascript
    ReactDOM.createPortal(child, container)
    ```

    第一个参数是任何可呈现的Reict子元素，例如元素、字符串或片段。第二个参数是DOM元素。

49. ### 什么是无状态组件？

    如果行为独立于其状态，那么它可以是一个无状态组件。 可以使用函数或类来创建无状态组件。 不在组件中使用生命周期函数, 您应该选择函数组件.如果您决定在这里使用函数组件，那么有很多好处；它们易于编写、理解和测试，稍微快一点，并且您可以完全避免使用 `this` 关键字。

50. ### 什么是有状态组件？

    如果组件的行为取决于组件的 `state`，那么可以将其称为有状态组件, 这些 *有状态组件* 总是 *class 组件* 并在 `constructor` 中获取初始化 state. 

    ```javascript
    class App extends Component {
      constructor(props) {
        super(props)
        this.state = { count: 0 }
      }

      render() {
        // ...
      }
    }
    ```
51. ### React 中如何对 props 进行验证？

    当程序运行在 *开发模式*, React 将会自动检查所有设置在组件上的 props 确保它们有 *正确类型*. 如果类型错误, React将在控制台中生成警告消息。 由于性能影响，它在*生产模式*中禁用。. The mandatory props are defined with `isRequired`.

    一组预定义的prop类型:

    1. `PropTypes.number`
    2. `PropTypes.string`
    3. `PropTypes.array`
    4. `PropTypes.object`
    5. `PropTypes.func`
    6. `PropTypes.node`
    7. `PropTypes.element`
    8. `PropTypes.bool`
    9. `PropTypes.symbol`
    10. `PropTypes.any`

    我们可以为 `User` 组件定义 `propTypes`:

    ```jsx harmony
    import React from 'react'
    import PropTypes from 'prop-types'

    class User extends React.Component {
      static propTypes = {
        name: PropTypes.string.isRequired,
        age: PropTypes.number.isRequired
      }

      render() {
        return (
          <>
            <h1>{`Welcome, ${this.props.name}`}</h1>
            <h2>{`Age, ${this.props.age}`}</h2>
          </>
        )
      }
    }
    ```

    **Note:** 在 React v15.5 *PropTypes* 被从 `React.PropTypes` 移动到 `prop-types` 库.

52. ### React的优点是什么？

    1. 使用 *Virtual DOM* 提高应用程序的性能。
    2. JSX 使代码易读易写.
    3. 同时支持客户端服务端渲染 (*SSR*).
    4. 易于与框架（Angular, Backbone）集成，因为它只是一个视图库。
    5. 易于使用诸如Jest之类的工具编写单元和集成测试。

53. ### React 的局限是什么？

    1. React 只是一个视图库，并不是完整的框架.
    2. 对于刚接触网络开发的初学者来说，有一个学习曲线。
    3. 将React集成到传统的MVC框架中需要一些额外的配置。
    4. 代码复杂性随着内联模板和JSX的增加而增加。
    5. 太多的小组件导致过度工作量或模版。

54. ### React V16 中错误边界是什么？

    *错误边界*是在其子组件树中的任何位置捕获JavaScript错误的组件，打印这些错误, 并显示一个回退UI，防止组件树崩溃。

    一个类组件如果定义一个 `componentDidCatch(error, info)` 新的生命周期方法就回变成错误边界。

    ```jsx harmony
    class ErrorBoundary extends React.Component {
      constructor(props) {
        super(props)
        this.state = { hasError: false }
      }

      componentDidCatch(error, info) {
        // 显示回退 UI
        this.setState({ hasError: true })
        // 你也可以向错误收集服务器发送错误
        logErrorToMyService(error, info)
      }

      render() {
        if (this.state.hasError) {
          // 你可以渲染任何自定义的回退UI
          return <h1>{'Something went wrong.'}</h1>
        }
        return this.props.children
      }
    }
    ```

    之后像常规组件一样使用:

    ```jsx harmony
    <ErrorBoundary>
      <MyWidget />
    </ErrorBoundary>
    ```

55. ### React v15中如何处理错误边界？

    React v15 为错误边界提供了非常基本的支持使用 `unstable_handleError` 方法. 

56. ### 什么是 static 类型检查的推荐方法？

    在 React 程序中，通常我们使用 *PropTypes库* (`React.PropTypes` 在 React v15.5 移动到 `prop-types` 包中) 用作 *类型检查*。 以大量代码作为基础, 推荐使用 *static 类型检查* 就像 Flow 或 TypeScript, 在编译时执行类型检查并提供自动完成功能的。

57. ### react-dom 包的用途是什么？

    `react-dom` 包提供了*DOM特定的方法*可以在应用程序的顶层使用. 大多数组件不需要使用此模块。这个包的一些方法是:

    1. `render()`
    2. `hydrate()`
    3. `unmountComponentAtNode()`
    4. `findDOMNode()`
    5. `createPortal()`

58. ### `react-dom` render 方法的目的是什么？

    此方法用于在所提供的容器中将React元素呈现到DOM中，并返回对组件的引用。如果React元素先前被呈现到容器中, 它将对它执行更新，并且仅根据需要修改DOM以反映最新的更改。

    ```
    ReactDOM.render(element, container[, callback])
    ```

   如果提供了可选的回调，则在呈现或更新组件之后将执行该回调。

59. ### 什么是ReactDOMServer？

    `ReactDOMServer` 对象使您能够渲染组件为静态标记（通常在节点服务器上使用）. 这个对象主要用于*服务器端呈现*(SSR)。以下方法可以在服务器和浏览器环境中使用

    1. `renderToString()`
    2. `renderToStaticMarkup()`

    例如，通常运行基于节点的Web服务器，如Express、Hapi或Koa，然后调用 `renderToString` 将根组件呈现给字符串，然后作为响应发送该字符串。

    ```javascript
    // using Express
    import { renderToString } from 'react-dom/server'
    import MyPage from './MyPage'

    app.get('/', (req, res) => {
      res.write('<!DOCTYPE html><html><head><title>My Page</title></head><body>')
      res.write('<div id="content">')
      res.write(renderToString(<MyPage/>))
      res.write('</div></body></html>')
      res.end()
    })
    ```

60. ### 如何在 React 中使用 innerHTML？

    `dangerouslySetInnerHTML` 是浏览器中 React 代替 `innerHTML` 的属性. 就像 `innerHTML` 一样, 考虑到跨站点脚本（XSS）攻击，使用这个属性是危险的。 你只需要传递一个对象key为 `__html` 值为文本 .

    在这个例子中，MyComponent使用 `dangerouslySetInnerHTML` 属性来设置HTML标记:

    ```jsx harmony
    function createMarkup() {
      return { __html: 'First &middot; Second' }
    }

    function MyComponent() {
      return <div dangerouslySetInnerHTML={createMarkup()} />
    }
    ```
61. ### 如何在React中使用style？

    `style` 属性接受驼峰命名的javascript对象而不是 CSS 字符串。 这与DOM样式的JavaScript属性是一致的，更加有效，并且防止了XSS安全漏洞。.

    ```jsx harmony
    const divStyle = {
      color: 'blue',
      backgroundImage: 'url(' + imgUrl + ')'
    };

    function HelloWorldComponent() {
      return <div style={divStyle}>Hello World!</div>
    }
    ```

   Style 键是驼峰命名，以便与JavaScript中访问DOM节点上的属性一致 (例如. `node.style.backgroundImage`).

62. ### React 中事件有什么不同？

    绑定事件在 React 中有一些语法上的不同:

    1. React 事件处理是驼峰命名而不是小写命名。
    2. JSX 中传递一个函数作为事件处理函数,而不是一个字符串.

63. ### 在 constructor 中使用 `setState()` 会发生什么？

    当使用 `setState()`, 除了给对象状态赋值之外，React还重新呈渲染件及其所有子组件。 你会得到像这样的错误: *Can only update a mounted or mounting component.* 所以需要使用 `this.state` 在 constructor 初始化 state 变量.

64. ### 数组索引作为keys的影响是什么？

    键应该是稳定的、可预测的、唯一的，以便React可以跟踪元素。

    在下面的代码片段中，每个元素的键将基于排序, 而不是和正在使用的数据绑定.这限制了React可以做的优化。

    ```jsx harmony
    {todos.map((todo, index) =>
      <Todo
        {...todo}
        key={index}
      />
    )}
    ```

    如果将元素数据用于唯一键，假设todo.id对这个列表是惟一的并且是稳定的，React将能够重新排序元素，而无需对它们重新赋值。

    ```jsx harmony
    {todos.map((todo) =>
      <Todo {...todo}
        key={todo.id} />
    )}
    ```

65. ### 在 `componentWillMount()` 方法中使用 `setState()` 好么？

    建议避免 `componentWillMount()` 生命周期方法中的异步初始化。`componentWillMount()` 在渲染前发生. 在 `render()` 前被调用, 因此，在该方法中设置状态将不会触发重新渲染. 避免在此方法中引入任何side-effects or subscriptions。确保对组件的异步赋值发生在 `componentDidMount()` 而不是 `componentWillMount()`.

    ```jsx harmony
    componentDidMount() {
      axios.get(`api/todos`)
        .then((result) => {
          this.setState({
            messages: [...result.data]
          })
        })
    }
    ```
66. ### 如果在初始化state时使用porps会发生什么？

    如果在不刷新组件的情况下更改组件上的属性，新的prop值将永远不会显示，因为构造函数函数永远不会更新组件的当前状态。 只有当组件首次创建时，才会从props中执行状态初始化。

    下面的组件不会显示更新的输入值： 

    ```jsx harmony
    class MyComponent extends React.Component {
      constructor(props) {
        super(props)

        this.state = {
          records: [],
          inputValue: this.props.inputValue
        };
      }
      //译者：如果想使用props的值渲染组件，那么在render中直接从props中获取，而不是在constructor中保存在state中。
      render() {
        return <div>{this.state.inputValue}</div>
      }
    }
    ```

    在render方法中使用props将更新值：

    ```jsx harmony
    class MyComponent extends React.Component {
      constructor(props) {
        super(props)

        this.state = {
          record: []
        }
      }

      render() {
        return <div>{this.props.inputValue}</div>
      }
    }
    ```

67. ### 如何根据条件渲染组件？

    您希望根据某种状态渲染不同的组件. JSX 不会渲染 `false` 或 `undefined`, 所以你可以使用条件 *短路*，仅当某个条件为真时才渲染组件的给定部分。

    ```jsx harmony
    const MyComponent = ({ name, address }) => (
      <div>
        <h2>{name}</h2>
        {address &&
          <p>{address}</p>
        }
      </div>
    )
    ```

    如果你需要 `if-else` 条件，那么使用 *三元运算*.

    ```jsx harmony
    const MyComponent = ({ name, address }) => (
      <div>
        <h2>{name}</h2>
        {address
          ？ <p>{address}</p>
          : <p>{'Address is not available'}</p>
        }
      </div>
    )
    ```

68. ### 为什么在dom元素上展开props时要注意？

    当 *展开props* 我们遇到添加未知HTML属性的风险, 这是个坏习惯. 相反，我们可以使用 `...rest` 操作符，因此它只添加所需的 props。例如

    ```jsx harmony
    const ComponentA = () =>
      <ComponentB isDisplay={true} className={'componentStyle'} />

    const ComponentB = ({ isDisplay, ...domProps }) =>
      <div {...domProps}>{'ComponentB'}</div>
    ```

69. ### React 怎么使用修饰器？

    你可以 *修饰* 你的 *类* 组件, 就像给一个函数传递组件一样. **Decorators** 是灵活易读的修改组件功能的方法。

    ```jsx harmony
    @setTitle('Profile')
    class Profile extends React.Component {
        //....
    }

    /*
      title 是一个字符串将会被设置为 document title
      WrappedComponent 是上面个例子中，修饰器放在上面的类组件
    */
    const setTitle = (title) => (WrappedComponent) => {
      return class extends React.Component {
        componentDidMount() {
          document.title = title
        }

        render() {
          return <WrappedComponent {...this.props} />
        }
      }
    }
    ```

    **Note:** 装饰器是没有进入ES7的一个特性，但是目前是一个*阶段2建议*。

70. ### 你如何记忆一个组件？

    有可用的memoize库，可用于函数组件。例如，`moize` 库可以将另一个组件中的组件记忆起来。

    ```jsx harmony
    import moize from 'moize'
    import Component from './components/Component' // this module exports a non-memoized component

    const MemoizedFoo = moize.react(Component)

    const Consumer = () => {
      <div>
        {'I will memoize the following entry:'}
        <MemoizedFoo/>
      </div>
    }
    ```
71. ### 如何实现服务器端呈现或SSR？

    React 以及具备在服务器端的渲染。有一个特殊版本的DOM渲染器可用, 它遵循与客户端相同的模式。

    ```jsx harmony
    import ReactDOMServer from 'react-dom/server'
    import App from './App'

    ReactDOMServer.renderToString(<App />)
    ```

    此方法将以字符串形式输出常规HTML, 然后将其作为服务器响应的一部分放在页面正文中。在客户端, React 检测预渲染的内容， 然后 seamlessly（无缝的） picks up（获取） where it left off（停止）.

72. ### React 怎么开启 production 模式？

    你应该使用 Webpack 的 `DefinePlugin` 方法设置 `NODE_ENV` 成 `production`,它删除了PropType验证和额外警告等内容。 除此之外, 如果你压缩代码, 例如, Uglify 的 dead-code 删除仅用于开发的代码和注释, 它会大大减小你的包裹的尺寸。

73. ### 什么是CRA及其好处？

    `create-react-app` CLI 工具允许你快速穿件并运行React 程序而不需要配置的过程.

    让我们使用 *CRA* 创建 TODO app:

    ```console
    # Installation
    $ npm install -g create-react-app

    # Create new project
    $ create-react-app todo-app
    $ cd todo-app

    # Build, test and run
    $ npm run build
    $ npm run test
    $ npm start
    ```
    它包含了我们建立一个React app 需要的所有事情:

    1. React, JSX, ES6, 和异步流的支持.
    2. ES6之外的语言附加项，如对象扩展运算符.
    3. 自动添加 CSS 前缀,所以不需要 -webkit- 或其他的前缀.
    4. 一个快速交互的单元测试运行程序，内置了对覆盖率报告的支持.
    5. 对常见错误发出警告的实时开发服务器.
    6. 一个构建脚本，用于打包JS、CSS和用于生产的图像，以及hashes 和sourcemaps.

74. ###  挂载阶段生命周期方法的顺序是什么？

    当一个组件的实例被创建并插入到DOM中，生命周期方法按照下面的顺序被调用。
    1. `constructor()`
    2. `static getDerivedStateFromProps()`
    3. `render()`
    4. `componentDidMount()`

75. ### React v16 什么生命周期方法不赞同使用？

    下面的生命周期方法将是不安全的编码实践，并且在异步呈现方面会有更多的问题。

    1. `componentWillMount()`
    2. `componentWillReceiveProps()`
    3. `componentWillUpdate()`

    从react v16.3开始，这些方法的别名是“unsafe”前缀，未修复的版本将在react v17中删除。

76. ### `getDerivedStateFromProps()` 生命周期的目的是什么？

    新的静态生命周期方法 `getDerivedStateFromProps()`，在实例化组件之后以及重新渲染组件之前调用. 它可以返回一个对象来更新state, 或 `null` 表示新 props 不需要任何状态更新。

    ```javascript
    class MyComponent extends React.Component {
      static getDerivedStateFromProps(props, state) {
        // ...
      }
    }
    ```

    此生命周期方法与 `componentdidUpdate()` 一起涵盖 `componentwillReceiveProps()` 的所有使用场景。

77. ### `getSnapshotBeforeUpdate()` 生命周期方法的目的是什么 ？

    新的生命周期方法 `getSnapshotBeforeUpdate()` 在 DOM 更新之前调用. 从这个方法返回的值，将会被传递到 `componentDidUpdate()` 第三个参数中.

    ```javascript
    class MyComponent extends React.Component {
      getSnapshotBeforeUpdate(prevProps, prevState) {
        // ...
      }
    }
    ```

    此生命周期方法与 `componentDidUpdate()` 一起涵盖 `componentWillUpdate()`的所有使用场景。

78. ### createElement() 和 cloneElement() 不同？

    在JSX中，react元素被转换为 `react.createElement()`，表示一个UI元素。而`react.clonelement()`用于克隆元素并传递新的属性。

79. ### 推荐的命名组件的方法是什么？

    建议通过引用来命名组件，而不是使用 `displayname`。

    将 `displayname`用于命名组件：

    ```javascript
    export default React.createClass({
      displayName: 'TodoApp',
      // ...
    })
    ```

    **建议的** 方法:

    ```javascript
    export default class TodoApp extends React.Component {
      // ...
    }
    ```

80. ### 组件类中方法的推荐顺序是什么？

    *建议* 从 *挂载* 到 *渲染阶段* 的方法顺序:

    1. `static`方法
    2. `constructor()`
    3. `getChildContext()`
    4. `componentWillMount()`
    5. `componentDidMount()`
    6. `componentWillReceiveProps()`
    7. `shouldComponentUpdate()`
    8. `componentWillUpdate()`
    9. `componentDidUpdate()`
    10. `componentWillUnmount()`
    11. 事件处理方法 `onClickSubmit()` 或 `onChangeDescription()`
    12. 渲染的 getter 方法 `getSelectReason()` 或 `getFooterContent()`
    13. 可选渲染方法 `renderNavigation()` 或 `renderProfilePicture()`
    14. `render()`

81. ### 什么是 switching 组件？

    *switching 组件* 是渲染多个组件之一的组件. 需要使用对象将属性值赋值到组件.

    例如, 一个 switching 组件基于 `page` 属性显示不同的页面:

    ```jsx harmony
    import HomePage from './HomePage'
    import AboutPage from './AboutPage'
    import ServicesPage from './ServicesPage'
    import ContactPage from './ContactPage'

    const PAGES = {
      home: HomePage,
      about: AboutPage,
      services: ServicesPage,
      contact: ContactPage
    }

    const Page = (props) => {
      const Handler = PAGES[props.page] || ContactPage

      return <Handler {...props} />
    }

    // The keys of the PAGES object can be used in the prop types to catch dev-time errors.
    Page.propTypes = {
      page: PropTypes.oneOf(Object.keys(PAGES)).isRequired
    }
    ```

82. ### 为什么需要给 setState() 传递函数？

    在这一问题之前的问题就是 `setState()` 是一个异步操作. 为了性能问题 React 批量改变 state, 所以在 `setState()` 被调用之后 state 可能不会立即改变。那意味着你不应该在 `setState()` 调用后依赖于当前的 state,因为你不能确定那个状态是什么. 解决方法是传递一个函数到 `setState()`, 将前一状态作为参数。做了这个便可以解决由于 `setState()` 的异步性质，用户在访问时获取旧的状态值问题。
    让我们设置初始化的数值为0. 在三次连续的增加操作后,该值将只增加一个。

    ```javascript
    // assuming this.state.count === 0
    this.setState({ count: this.state.count + 1 })
    this.setState({ count: this.state.count + 1 })
    this.setState({ count: this.state.count + 1 })
    // this.state.count === 1, not 3
    ```

    如果传递一个函数到 `setState()`, 计数正确递增。

    ```javascript
    this.setState((prevState, props) => ({
      count: prevState.count + props.increment
    }))
    // this.state.count === 3 as expected
    ```

83. ### React 严格模式是是什么？

    `React.StrictMode` 是突出应用程序中潜在问题的有用组件. 就像 `<Fragment>`, `<StrictMode>` 不会渲染任何额外的 DOM 元素. 它为其后代元素触发额外的检查和警告. 这些检查仅适用于 *开发模式*。

    ```jsx harmony
    import React from 'react'

    function ExampleApplication() {
      return (
        <div>
          <Header />
          <React.StrictMode>
            <div>
              <ComponentOne />
              <ComponentTwo />
            </div>
          </React.StrictMode>
          <Footer />
        </div>
      )
    }
    ```

    在上面的示例中，*严格模式* 检查仅适用于 `<componentone>` 和 `<componenttwo>` 组件。

84. ### 什么是 React Mixins？

    *Mixins* 是一种完全分离组件以具有共同功能的方法. Mixins **不应该被使用** 它可以被 *高阶组件* 或 *修饰器* 替换.

    最常用的 *Mixins* 之一是 `purendermixin`。当props和state与之前的props和state略微相等时，您可能在某些组件中使用它来防止不必要的重新渲染：

    ```javascript
    const PureRenderMixin = require('react-addons-pure-render-mixin')

    const Button = React.createClass({
      mixins: [PureRenderMixin],
      // ...
    })
    ````
    <!-- TODO: mixins are deprecated -->

85. ### 为什么 `ismounted()` 是反模式，正确的解决方案是什么？

    `ismounted()`的主要用例是避免在卸载组件后调用 `setstate()`，因为它将发出警告。

    ```javascript
    if (this.isMounted()) {
      this.setState({...})
    }
    ```

    在 `setState()` 调用前检查 `isMounted()` 消除警告, 但它也破坏了警告的目的. 使用 `ismounted()`是一种code味道，因为您要检查的唯一原因是您认为在卸载组件后可能保存了一个引用。

    最佳解决方案是找到在组件卸载后调用 `setState()` 的位置并修复它们。这种情况最常见的原因是回调，即组件正在等待某些数据，并在数据到达之前卸载。理想情况下，任何回调都应在卸载之前在 `componentwillUnmount()`中取消。

86. ### React中支持哪些指针事件？

    *指针事件* 提供处理所有输入事件的统一方法。在过去，我们有一个鼠标和相应的事件监听器来处理它们，但现在我们有许多设备与鼠标无关。像带触摸屏或笔的手机. 我们需要记住，这些事件只能在支持*指针事件*规范的浏览器中工作。

    以下事件类型现在在*react dom*中可用 *React DOM*:

    1. `onPointerDown`
    2. `onPointerMove`
    3. `onPointerUp`
    4. `onPointerCancel`
    5. `onGotPointerCapture`
    6. `onLostPointerCaptur`
    7. `onPointerEnter`
    8. `onPointerLeave`
    9. `onPointerOver`
    10. `onPointerOut`

87. ### 为什么组件名字首字母需要大写？

    如果你是用JSX渲染你的组件, 那个组件的首字母要大写， 否则，react将作为无法识别的标记引发错误. 这种约定是因为只有HTML元素和SVG标记可以以小写字母开头。

    您可以定义组件类，名称以小写字母开头，但导入时应该使用大写字母。

    ```jsx harmony
    class myComponent extends Component {
      render() {
        return <div />
      }
    }

    export default myComponent
    ```

    While when imported in another file it should start with capital letter:

    ```jsx harmony
    import MyComponent from './MyComponent'
    ```

88. ### React v16 支持自定义 DOM 属性么？

    是的. 在过去, React 用于忽略未知的DOM属性. 如果编写的JSX具有一个React无法识别的属性, React 会跳过它. 例如:

    ```jsx harmony
    <div mycustomattribute={'something'} />
    ```

    React v15 将会渲染一个空的 div:

    ```html
    <div />
    ```

    React v16 一些未知的属性将会保留在 DOM:

    ```html
    <div mycustomattribute='something' />
    ```

    这对于提供特定于浏览器的非标准属性、尝试新的 DOM API 以及与固定的第三方库集成非常有用。

89. ### constructor 和 getInitialState 区别？

    使用 ES6 类你应该在constructor 中初始化 state, 在 `React.createClass()` 中使用 `getInitialState()` 方法。

    Using ES6 classes:

    ```javascript
    class MyComponent extends React.Component {
      constructor(props) {
        super(props)
        this.state = { /* initial state */ }
      }
    }
    ```

    Using `React.createClass()`:

    ```javascript
    const MyComponent = React.createClass({
      getInitialState() {
        return { /* initial state */ }
      }
    })
    ```

    **Note:** `React.createClass()` 在react v16中已弃用并删除。改用普通的javascript类。

90. ### 是否可以在不调用setState的情况下强制组件重新呈现？

    默认情况, 当组件的state 或 props 改变,组将将会重渲染. 如果您的 `render()` 方法依赖于其他数据，您可以通过调用`forceUpdate()` 来告诉react组件需要重新呈现。

    >默认情况下，当组件的state或props改变时，组件将重新渲染。如果你的render()方法依赖于一些其他的数据，你可以告诉React组件需要通过调用forceUpdate()重新渲染。 调用forceUpdate()会导致组件跳过shouldComponentUpdate(),直接调用render()。这将触发组件的正常生命周期方法,包括每个子组件的shouldComponentUpdate()方法。forceUpdate就是重新render。有些变量不在state上，当时你又想达到这个变量更新的时候，刷新render；或者state里的某个变量层次太深，更新的时候没有自动触发render。这些时候都可以手动调用forceUpdate自动触发render

    ```javascript
    component.forceUpdate(callback)
    ```

    建议避免使用 `forceupdate()` 所有地方，只读取 `render()` 中 `this.props` 和 `this.state`。

91. ### React 使用 ES6 类 super() 和 super(props) 区别是什么？

    当你需要 `this.props` 在 `constructor()` 中那应该传入 props 到 `super()` 方法中.

    使用 `super(props)`:

    ```javascript
    class MyComponent extends React.Component {
      constructor(props) {
        super(props)
        console.log(this.props) // { name: 'John', ... }
      }
    }
    ```

    使用 `super()`:

    ```javascript
    class MyComponent extends React.Component {
      constructor(props) {
        super()
        console.log(this.props) // undefined
      }
    }
    ```

    在 `constructor()` 外面 这两种写法都会显示相同的 `this.props` 的值.

92. ### 如何在JSX中循环？

    可以简单使用 `Array.prototype.map`  ES6 *箭头函数* 语法. 例如,  `items` 数组对象转换成数组组件

    ```jsx harmony
    <tbody>
      {items.map(item => <SomeComponent key={item.id} name={item.name} />)}
    </tbody>
    ```

    不能使用 `for` 循环:

    ```jsx harmony
    <tbody>
      for (let i = 0; i < items.length; i++) {
        <SomeComponent key={items[i].id} name={items[i].name} />
      }
    </tbody>
    ```

    这是因为JSX标签被转换成*函数调用*，并且不能在表达式中使用语句。这可能会由于 `do` 表达式而改变，这些表达式是*第一阶段建议*。

93. ### 如何访问属性引号中的属性？

    React (或 JSX) 不支持属性值内的变量插值，下面的表达不起作用:

    ```jsx harmony
    <img className='image' src='images/{this.props.image}' />
    ```

    但可以将任何JS表达式作为整个属性值放在大括号内。所以下面的表达式是有效的:

    ```jsx harmony
    <img className='image' src={'images/' + this.props.image} />
    ```

    使用 *模版字符串* 也同样可以:

    ```jsx harmony
    <img className='image' src={`images/${this.props.image}`} />
    ```

94. ### React proptype 数组形状？

    如果要将对象数组传递给具有特定形状的组件，请使用 `react.proptypes.shape()` 作为 `react.proptypes.arrayOf()`的参数。

    ```javascript
    ReactComponent.propTypes = {
      arrayWithShape: React.PropTypes.arrayOf(React.PropTypes.shape({
        color: React.PropTypes.string.isRequired,
        fontSize: React.PropTypes.number.isRequired
      })).isRequired
    }
    ```

95. ### 如何按条件应用className属性？

    您不应该在引号内使用大括号，因为它将作为字符串进行计算。

    ```jsx harmony
    <div className="btn-panel {this.props.visible ？ 'show' : 'hidden'}">
    ```

    相反，您需要将大括号移到外部（不要忘记在类名之间包含空格）

    ```jsx harmony
    <div className={'btn-panel ' + (this.props.visible ？ 'show' : 'hidden')}>
    ```

    *模版字符串* 也将会工作:

    ```jsx harmony
    <div className={`btn-panel ${this.props.visible ？ 'show' : 'hidden'}`}>
    ```

96. ### React 和 ReactDOM 的区别是什么？

    `react` 包括 `React.createElement()`, `React.Component`, `React.Children`,和其他帮助描述元素和类组件. 您可以将这些视为构建组件所需的同构或通用帮助器。 `react-dom` 包括 `ReactDOM.render()`， `react-dom/server` 有`ReactDOMServer.renderToString()` 和 `ReactDOMServer.renderToStaticMarkup()` 支持 *服务端渲染* 。

97. ### 为什么 ReactDOM 从 React 中分离？

    react团队致力于将所有与dom相关的特性提取到一个名为 *react dom* 的单独库中。 React v0.14是第一个分离库的版本。 通过查看一些包“react native”、“react art”、“react canvas”和“react three”，我们可以清楚地看到react的美和本质与浏览器或DOM无关。为了构建更多React可渲染环境，React团队计划将主React包分为两部分：`react` and `react-dom`. 这为编写可在React和React Native的Web版本之间共享的组件铺平了道路。

98. ### 如何使用 React label 元素？

    如果尝试使用标准的`for`属性渲染绑定到文本输入的`<label>`元素,则会生成缺少该属性的HTML，并向控制台打印警告。

    ```jsx harmony
    <label for={'user'}>{'User'}</label>
    <input type={'text'} id={'user'} />
    ```

    由于`for`是javascript中的保留关键字，因此请改用`htmlFor`。

    ```jsx harmony
    <label htmlFor={'user'}>{'User'}</label>
    <input type={'text'} id={'user'} />
    ```

99. ### 怎么组合多个内联样式对象？

    你可以在 React 中使用 *展开运算符*:

    ```jsx harmony
     <button style={{...styles.panel.button, ...styles.panel.submitButton}}>{'Submit'}</button>
    ```

    如果您使用的是react native，那么可以使用数组表示：

    ```jsx harmony
    <button style={[styles.panel.button, styles.panel.submitButton]}>{'Submit'}</button>
    ```

100. ### 如何在浏览器缩放时重渲染视图？

    你可以在 `componentDidMount()` 监听 `resize` 事件，并更新他们的尺寸 (`宽度` 和 `高度`). 你应该在 `componentWillUnmount()` 移除方法.

     ```javascript
     class WindowDimensions extends React.Component {
       componentWillMount() {
         this.updateDimensions()
       }

       componentDidMount() {
         window.addEventListener('resize', this.updateDimensions)
       }

       componentWillUnmount() {
         window.removeEventListener('resize', this.updateDimensions)
       }

       updateDimensions() {
         this.setState({width: $(window).width(), height: $(window).height()})
       }

       render() {
         return <span>{this.state.width} x {this.state.height}</span>
       }
     }
     ```
101. ### setState 和 replaceState 方法的却别是什么？

     当你使用 `setState()` 合并当前和之前的 states。 `replaceState()` 抛出当前的states, 只替换你提供的. 通常使用`setstate()`，除非您出于某种原因确实需要删除所有以前的键. 你也可以在 `setState()` 中设置state 为 `false`/`null` 以代替 `replaceState()`.

102. ### 如何监听 state 改变？

     下面的生命周期函数会在 state 改变时被调用。 您可以将提供的state和props值与当前state和props进行比较，以确定某些有意义的内容是否发生了更改。

     ```javascript
     componentWillUpdate(object nextProps, object nextState)
     componentDidUpdate(object prevProps, object prevState)
     ```

103. ### React state 下移除数组元素的建议方法是什么？

     一个途径是使用 `Array.prototype.filter()` 方法.

     例如, 让我们创建一个 `removeItem()` 方法用来更新state.

     ```javascript
     removeItem(index) {
       this.setState({
         data: this.state.data.filter((item, i) => i !== index)
       })
     }
     ```

104. ### 是否可以在不渲染HTML的情况下使用React？

     最新版本（大于等于16.2）是可能的。以下是可能的选项：

     ```jsx harmony
     render() {
       return false
     }
     ```

     ```jsx harmony
     render() {
       return null
     }
     ```

     ```jsx harmony
     render() {
       return []
     }
     ```

     ```jsx harmony
     render() {
       return <React.Fragment></React.Fragment>
     }
     ```

     ```jsx harmony
     render() {
       return <></>
     }
     ```

     返回 `undefined` 是无效的。

105. ### React 如何优雅的打印 JSON？

     我们可以使用 `<pre>` 标签，以便保留 `json.stringify()`的格式：

     ```jsx harmony
     const data = { name: 'John', age: 42 }

     class User extends React.Component {
       render() {
         return (
           <pre>
             {JSON.stringify(data, null, 2)}
           </pre>
         )
       }
     }

     React.render(<User />, document.getElementById('container'))
     ```

106. ### 为什么 React 不能更新 prop？

     反应哲学中，props 应该是`不可变的`和`自上而下的`。 这意味着父级可以向子级发送任何属性值，但子级不能修改接收到的属性。

107. ### 页面加载时如何让 input 元素获取焦点？

     你可以通过为 `input` 元素创建 *ref* 达到目的，并在 `componentDidMount()` 使用它:

     ```jsx harmony
     class App extends React.Component{
       componentDidMount() {
         this.nameInput.focus()
       }

       render() {
         return (
           <div>
             <input
               defaultValue={'Won\'t focus'}
             />
             <input
               ref={(input) => this.nameInput = input}
               defaultValue={'Will focus'}
             />
           </div>
         )
       }
     }

     ReactDOM.render(<App />, document.getElementById('app'))
     ```

108. ### 是否可以更新 state 中的对象（Object）？

     1. **调用 `setState()` 通过 state和对象合并:**

         * 使用 `Object.assign()` 创建一个Object的副本:

             ```javascript
             const user = Object.assign({}, this.state.user, { age: 42 })
             this.setState({ user })
             ```

         * 使用 *展开运算符*:

             ```javascript
             const user = { ...this.state.user, age: 42 }
             this.setState({ user })
             ```

     2. **调用 `setState()` 通过一个函数:**

         ```javascript
         this.setState(prevState => ({
           user: {
             ...prevState.user,
             age: 42
           }
         }))
         ```

109. ### 为什么函数是 `setState()` 中覆盖object 建议的方法？

     为了性能，React 可能会再一次更新中批量调用 `setState()`. 因为 `this.props` 和 `this.state` 可能是异步更新, 不应该依赖它们的值来计算下一个状态。

     此计数器示例将无法按预期更新：

     ```javascript
     // 错误
     this.setState({
       counter: this.state.counter + this.props.increment,
     })
     ```

     推荐的方法是通过一个函数调用 `setState()` 而不是一个对象. 该函数将接收前一个状态作为第一个参数，以及应用更新时的props作为第二个参数。

     ```javascript
     // Correct
     this.setState((prevState, props) => ({
       counter: prevState.counter + props.increment
     }))
     ```

110. ### 如何在浏览器中找到运行时的react版本？

     可以使用 `React.version` 来获取版本.

     ```jsx harmony
     const REACT_VERSION = React.version

     ReactDOM.render(
       <div>{`React version: ${REACT_VERSION}`}</div>,
       document.getElementById('app')
     )
     ```
111. ### 在你的 create react 应用中加入 polyfill 的方法是什么？

     1. **手动从 `core-js` 中引入:**

         创建一个文件叫 (类似的) `polyfills.js` 并在根文件 `index.js` 中引入它. 运行 `npm install core-js` 或 `yarn add core-js` 并导入您所需的特定功能.

         ```javascript
         import 'core-js/fn/array/find'
         import 'core-js/fn/array/includes'
         import 'core-js/fn/number/is-nan'
         ```

     2. **使用 Polyfill 服务:**

         使用 polyfill.io CDN 来检索, 浏览器 polyfills 通过 `index.html` 中这一行被添加:

         ```html
         <script src='https://cdn.polyfill.io/v2/polyfill.min.js？features=default,Array.prototype.includes'></script>
         ```

         在上面的脚本中，我们必须显式地请求 `array.prototype.includes` 功能，因为它不包含在默认功能集中。

         >原型方法没有被自动添加，需要使用 `array.prototype.includes`

112. ### 如何在create react app中使用https而不是http？

     只需要使用 `HTTPS=true` 配置. 你可以编辑 `package.json` 文件:

     ```json
     "scripts": {
       "start": "set HTTPS=true && react-scripts start"
     }
     ```

     或运行 `set HTTPS=true && npm start`

113. ### 如何避免在create react app中使用相对路径导入？

     创建一个文件叫 `.env` 在项目根目录并写入导入路径:

     ```
     NODE_PATH=src/app
     ```

     之后重启开发服务器. 现在，您应该能够在不使用相对路径的情况下导入 `src/app` 中的任何内容。

114. ### 如何为React路由器添加谷歌分析？

     在 `history` 对象上添加侦听器以记录每个页面视图：

     ```javascript
     history.listen(function (location) {
       window.ga('set', 'page', location.pathname + location.search)
       window.ga('send', 'pageview', location.pathname + location.search)
     })
     ```

115. ### 如何每秒更新组件？

     你需要使用 `setInterval()` 触发改变, 但同样需要在组件卸载时清除定时器防止错误和内存泄漏。
     ```javascript
     componentDidMount() {
       this.interval = setInterval(() => this.setState({ time: Date.now() }), 1000)
     }

     componentWillUnmount() {
       clearInterval(this.interval)
     }
     ```
116. ### 如何在内联样式中添加浏览器前缀？

     React *不支持* 自动添加 *浏览器前缀*. 需要手动添加.

     ```jsx harmony
     <div style={{
       transform: 'rotate(90deg)',
       WebkitTransform: 'rotate(90deg)', // note the capital 'W' here
       msTransform: 'rotate(90deg)' // 'ms' is the only lowercase vendor prefix
     }} />
     ```

117. ### 如何使用 React 和 ES6 导入导出组件？

     应该使用默认值导出组件

     ```jsx harmony
     import React from 'react'
     import User from 'user'

     export default class MyProfile extends React.Component {
       render(){
         return (
           <User type="customer">
             //...
           </User>
         )
       }
     }
     ```

     使用导出标识, MyProfile将成为组件并从此模块导出，在其他组件中导入时不用提及它的名字。

118. ### 为什么React组件名称必须以大写字母开头？

     在JSX中，小写标记名被认为是HTML标记。 但是, 大写的和使用 `.` 的小写标签名不是。

     1. `<component />` compiles to `React.createElement('component')` (i.e, HTML tag)
     2. `<obj.component />` compiles to `React.createElement(obj.component)`
     3. `<Component />` compiles to `React.createElement(Component)`

119. ### 为什么组件的 constructor 只被调用一次？

     React 的 *调停* 算法， 假定没有任何信息在对立面,如果自定义组件在随后的渲染中出现在同一位置，它与以前的组件相同，因此重用以前的实例，而不是创建新的实例。

120. ### 如何定义react中的常量？

     你可以使用 ES7 `static` 定义常量.

     ```javascript
     class MyComponent extends React.Component {
       static DEFAULT_PAGINATION = 10
     }
     ```

     *静态字段*是*类字段*阶段3建议的一部分。

121. ### 如何在React中以编程方式触发单击事件？

     可以使用ref属性通过回调获取对基础 `HTMLInputElement` 对象的引用, 将引用存储为类属性, 然后使用该引用稍后使用 `HTMLElement.click` 方法从事件处理程序中触发单击. 这可以通过两个步骤完成:

     1. render 方法中创建 ref:

         ```jsx harmony
         <input ref={input => this.inputElement = input} />
         ```

     2. 在事件处理程序中应用Click事件:

         ```javascript
         this.inputElement.click()
         ```

122. ### 是否可以在普通的react中使用async/await？

     如果你想在 React 中使用 `async`/`await`, 你需要使用 *Babel* 和 [transform-async-to-generator](https://babeljs.io/docs/en/babel-plugin-transform-async-to-generator) 插件. React Native ships with Babel and a set of transforms.

123. ### React的常见文件夹结构是什么？

     React项目文件结构有两种常见做法。

     1. **按领域模型或路由分组：**

         构造项目的一种常见方法是将CSS、JS和测试放在一起，按领域模型或路由分组。

         ```
         common/
         ├─ Avatar.js
         ├─ Avatar.css
         ├─ APIUtils.js
         └─ APIUtils.test.js
         feed/
         ├─ index.js
         ├─ Feed.js
         ├─ Feed.css
         ├─ FeedStory.js
         ├─ FeedStory.test.js
         └─ FeedAPI.js
         profile/
         ├─ index.js
         ├─ Profile.js
         ├─ ProfileHeader.js
         ├─ ProfileHeader.css
         └─ ProfileAPI.js
         ```

     2. **按文件类型分组**

         另一种流行的项目结构方法是将类似的文件组合在一起。

         ```
         api/
         ├─ APIUtils.js
         ├─ APIUtils.test.js
         ├─ ProfileAPI.js
         └─ UserAPI.js
         components/
         ├─ Avatar.js
         ├─ Avatar.css
         ├─ Feed.js
         ├─ Feed.css
         ├─ FeedStory.js
         ├─ FeedStory.test.js
         ├─ Profile.js
         ├─ ProfileHeader.js
         └─ ProfileHeader.css
         ```

124. ### 动画的流行库是什么？

     *React Transition Group* 和 *React Motion* React生态系统中流行的动画库.

125. ### 样式模块的好处是什么？

     建议避免在组件中对样式值进行硬编码。任何可能在不同的UI组件之间使用的值都应该提取到它们自己的模块中。

     例如，可以将这些样式提取到单独的组件中：

     ```javascript
     export const colors = {
       white,
       black,
       blue
     }

     export const space = [
       0,
       8,
       16,
       32,
       64
     ]
     ```

     然后在其他组件中单独导入：

     ```javascript
     import { space, colors } from './styles'
     ```

126. ### 什么语法风格检测是 React 中受欢迎的？
     ESLint is a popular JavaScript linter. There are plugins available that analyse specific code styles. One of the most common for React is an npm package called `eslint-plugin-react`. By default, it will check a number of best practices, with rules checking things from keys in iterators to a complete set of prop types. Another popular plugin is `eslint-plugin-jsx-a11y`, which will help fix common issues with accessibility. As JSX offers slightly different syntax to regular HTML, issues with `alt` text and `tabindex`, for example, will not be picked up by regular plugins.
     >ESLint 是一个受欢迎的React语法风格检测. 代码风格特异性分析中有用的插件. React最常见的一个是名为`eslint-plugin-react`的NPM包。默认情况下，它将检查一些最佳实践， 使用规则检查从迭代器中的键到一组完整的属性类型。 另一个流行的插件是`eslint-plugin-jsx-a11y`, 这将有助于解决可访问性的常见问题。由于JSX为常规HTML提供了稍有不同的语法，例如，`alt` 文本和`tabindex` 的问题不会被常规插件发现。 例如，常规插件将不会接收。

127. ### 如何进行Ajax调用以及应该在哪些组件生命周期方法中进行Ajax调用？

     您可以使用Ajax库，如AXIOS、JQueryAjax和浏览器内置的 `fetch`。您应该在`componentdidmount()`生命周期方法中获取数据。这样，您就可以在检索数据时使用`setState()`更新组件。

     例如，从API中获取员工列表并设置本地状态：

     ```jsx harmony
     class MyComponent extends React.Component {
       constructor(props) {
         super(props)
         this.state = {
           employees: [],
           error: null
         }
       }

       componentDidMount() {
         fetch('https://api.example.com/items')
           .then(res => res.json())
           .then(
             (result) => {
               this.setState({
                 employees: result.employees
               })
             },
             (error) => {
               this.setState({ error })
             }
           )
       }

       render() {
         const { error, employees } = this.state
         if (error) {
           return <div>Error: {error.message}</div>;
         } else {
           return (
             <ul>
               {employees.map(item => (
                 <li key={employee.name}>
                   {employee.name}-{employees.experience}
                 </li>
               ))}
             </ul>
           )
         }
       }
     }
     ```

128. ### 什么是 render props？

     **Render Props** 是指一种在 React 组件之间使用一个值为函数的 prop 在 React 组件间共享代码的简单技术。下面的组件使用的render 属性返回react元素。

     ```jsx harmony
     <DataProvider render={data => (
       <h1>{`Hello ${data.target}`}</h1>
     )}/>
     ```

     React Router 和 DownShift这样的库使用这种模式。

## React Router

129. ### 什么是 React Router？

     React Router是一个功能强大的路由库，它构建在React之上，帮助您以难以置信的速度添加新屏幕和流到应用程序, 同时保持URL与页面上显示的内容同步。

130. ### React Router 与 history 库有什么不同？

     React Router 是 `history` 库的包装，它负责与浏览器`window.history` 交互， 通过浏览器和 hash histories. 它也提供 memory history 这对于没有全局历史的环境很有用, 例如手机app 开发环境 (React Native) and 节点单元测试.

131. ### React Router v4 中 `<Router>` 组件是什么？

     React Router v4 提供以下3个组件：

     1. `<BrowserRouter>`
     2. `<HashRouter>`
     3. `<MemoryRouter>`

     以上组件将创建*浏览器*,*哈希*和*内存*历史实例。react router v4使与路由器关联的 `history` 实例的属性和方法通过 `router` 对象中的上下文可用。 

132. ### `push()`和`replace()`方法用于`history`的目的是什么？

    历史实例有两种用于导航的方法

     1. `push()`
     2. `replace()`

     如果你把历史history看作访问位置的数组, `push()` 将会在数组中添加新的位置 `replace()` 将会在数组中用一个新的覆盖当前的位置。

133. ### 如何使用React Router v4以编程方式导航？

     有三种不同的方法来实现组件内的编程路由/导航。.

     1. **使用 `withRouter()` 高阶函数:**

         `withRouter()` 高阶函数将历史对象作为组件的一个属性注入. 这个对象提供 `push()` 和 `replace()` 方法来避免使用 context.

         ```jsx harmony
         import { withRouter } from 'react-router-dom' // this also works with 'react-router-native'

         const Button = withRouter(({ history }) => (
           <button
             type='button'
             onClick={() => { history.push('/new-location') }}
           >
             {'Click Me!'}
           </button>
         ))
         ```

     2. **使用 `<Route>` 组件和渲染porps模式:**

         `<Route>` 组件传递与 `withRouter()` 相同的属性, 因此，您可以通过History属性访问History方法。

         ```jsx harmony
         import { Route } from 'react-router-dom'

         const Button = () => (
           <Route render={({ history }) => (
             <button
               type='button'
               onClick={() => { history.push('/new-location') }}
             >
               {'Click Me!'}
             </button>
           )} />
         )
         ```

     3. **使用 context:**

         不建议使用此选项，并将其视为不稳定的API。 

         ```jsx harmony
         const Button = (props, context) => (
           <button
             type='button'
             onClick={() => {
               context.history.push('/new-location')
             }}
           >
             {'Click Me!'}
           </button>
         )

         Button.contextTypes = {
           history: React.PropTypes.shape({
             push: React.PropTypes.func.isRequired
           })
         }
         ```

134. ### 如何在 React Router v4 获取查询参数？

     解析查询字符串的能力已从React Router v4中去掉，因为多年来一直有用户请求支持不同的实现。因此，用户可以选择他们喜欢的实现。建议使用查询字符串库。

     ```javascript
     const queryString = require('query-string');
     const parsed = queryString.parse(props.location.search);
     ```

     如果想要原生可以使用 `URLSearchParams`:

     ```javascript
     const params = new URLSearchParams(props.location.search)
     const foo = params.get('name')
     ```

     你应该为 IE11 使用 *polyfill*.

135. ### 为什么收到 Router 可能只有一个子元素警告？

     您必须将路由包装在一个 `<switch>` 块中，因为 `<switch>` 是唯一的，它只呈现路由。

     首先需要引入 `Switch` :

     ```javascript
     import { Switch, Router, Route } from 'react-router'
     ```

     在 `<Switch>` 块中定义路由:

     ```jsx harmony
     <Router>
       <Switch>
         <Route {/* ... */} />
         <Route {/* ... */} />
       </Switch>
     </Router>
     ```

136. ### React Router v4 中如何向 `history.push` 方法中传递参数？

     导航时，可以将属性传递给 `history` 对象：

     ```javascript
     this.props.history.push({
       pathname: '/template',
       search: '？name=sudheer',
       state: { detail: response.data }
     })
     ```

     `search` 属性用于在`push()`方法中传递查询参数。

137. ### 如何实现*默认*或*未找到*页？

     `<switch>` 会渲染第一个匹配的子 `<route>` 。没有路径的 `<route>` 总是匹配的。所以只需要简单地删除路径属性，如下所示

     ```jsx harmony
     <Switch>
       <Route exact path="/" component={Home}/>
       <Route path="/user" component={User}/>
       <Route component={NotFound} />
     </Switch>
     ```

138. ### 如何在 React Router v4 中获取 history ？

     1. 创建一个导出 `history` 对象的模块，并在整个项目中导入此模块。

         例如, 创建 `history.js` 文件:

         ```javascript
         import { createBrowserHistory } from 'history'

         export default createBrowserHistory({
           /* pass a configuration object here if needed */
         })
         ```

     2. 您应该使用 `<router>` 组件，而不是内置路由器。 在 `index.js` 文件中导入上面的 `history.js`:

         ```jsx harmony
         import { Router } from 'react-router-dom'
         import history from './history'
         import App from './App'

         ReactDOM.render((
           <Router history={history}>
             <App />
           </Router>
         ), holder)
         ```

     3. 您还可以使用类似于内置 `history` 对象的 `history` 的push方法：

         ```javascript
         // some-other-file.js
         import history from './history'

         history.push('/go-here')
         ```

139. ### 如何在登录后执行自动重定向？

     `react router` 包在react router中提供了`<redirect>`组件。导航到一个新位置时渲染`<redirect>`。与服务器端重定向一样，新位置将覆盖历史堆栈中的当前位置。

     ```javascript
     import React, { Component } from 'react'
     import { Redirect } from 'react-router'

     export default class LoginComponent extends Component {
       render() {
         if (this.state.isLoggedIn === true) {
           return <Redirect to="/your/redirect/page" />
         } else {
           return <div>{'Login Please'}</div>
         }
       }
     }
     ```
## React 国际化

140. ### 什么是 React Intl?

     *react intl*库使react的内部化变得简单，它有现成的组件和一个可以处理从格式化字符串、日期和数字到复数的一切内容的API。react intl是*formatjs*的一部分，它提供绑定以通过其组件和API进行响应。

141. ### React Intl 主要特性是什么?

     1. 使用分隔符显示数字.
     2. 正确显示日期和时间.
     3. 显示相对于“现在”的日期.
     4. 在多元化的字符串标签.
     5. 支持150多种语言.
     6. 在浏览器和节点中运行.
     7. 以标准为基础.

142. ### React Intl 中两种格式化的方式是什么?

     库提供了两种格式化字符串、数字和日期的方法：React组件或API。

     ```jsx harmony
     <FormattedMessage
       id={'account'}
       defaultMessage={'The amount is less than minimum balance.'}
     />
     ```

     ```javascript
     const messages = defineMessages({
       accountMessage: {
         id: 'account',
         defaultMessage: 'The amount is less than minimum balance.',
       }
     })

     formatMessage(messages.accountMessage)
     ```

143. ### React Intl 中如何使用 `<FormattedMessage>` 作为 placeholder?

     来自 `react-intl` 的组件 `<Formatted... />` 返回元素, 不是纯文本, placeholder, alt 文本等。 在那种情况下, 你应该使用低等级 API `formatMessage()`. 你可以使用高阶组件 `injectIntl()` 在你的组件中注入 `intl`，在那个对象中使用获得的 `formatMessage()`方法格式化 。

     ```jsx harmony
     import React from 'react'
     import { injectIntl, intlShape } from 'react-intl'

     const MyComponent = ({ intl }) => {
       const placeholder = intl.formatMessage({id: 'messageId'})
       return <input placeholder={placeholder} />
     }

     MyComponent.propTypes = {
       intl: intlShape.isRequired
     }

     export default injectIntl(MyComponent)
     ```

144. ### 如何使用 React Intl 访问当前区域设置?

     可以使用 `injectIntl()` 在应用程序的任何组件中获取当前区域设置：

     ```jsx harmony
     import { injectIntl, intlShape } from 'react-intl'

     const MyComponent = ({ intl }) => (
       <div>{`The current locale is ${intl.locale}`}</div>
     )

     MyComponent.propTypes = {
       intl: intlShape.isRequired
     }

     export default injectIntl(MyComponent)
     ```

145. ### 如何使用 React Intl 格式化日期?

     `injectIntl()` 高阶组件将会通过组件的属性给你访问 `formatDate()` 方法的能力。 `formatted date` 的实例在内部使用该方法，它返回格式化日期的字符串表示形式。

     ```jsx harmony
     import { injectIntl, intlShape } from 'react-intl'

     const stringDate = this.props.intl.formatDate(date, {
       year: 'numeric',
       month: 'numeric',
       day: 'numeric'
     })

     const MyComponent = ({intl}) => (
       <div>{`The formatted date is ${stringDate}`}</div>
     )

     MyComponent.propTypes = {
       intl: intlShape.isRequired
     }

     export default injectIntl(MyComponent)
     ```
## React Testing

146. ### React 测试中什么是 Shallow Renderer?

     *Shallow rendering* 对于在 React 中编写单元测试用例很有用. 它允许您渲染一个组件*一级深度*并断言他 render 方法的返回值, 无需担心子组件未实例化或渲染的行为。

     例如，如果你有如下的组件:

     ```javascript
     function MyComponent() {
       return (
         <div>
           <span className={'heading'}>{'Title'}</span>
           <span className={'description'}>{'Description'}</span>
         </div>
       )
     }
     ```

     那么你可以像如下断言:

     ```jsx harmony
     import ShallowRenderer from 'react-test-renderer/shallow'

     // in your test
     const renderer = new ShallowRenderer()
     renderer.render(<MyComponent />)

     const result = renderer.getRenderOutput()

     expect(result.type).toBe('div')
     expect(result.props.children).toEqual([
       <span className={'heading'}>{'Title'}</span>,
       <span className={'description'}>{'Description'}</span>
     ])
     ```

147. ### React 中 `TestRenderer` 包是什么?

     这个包提供了一个可以用来渲染组件为纯 JavaScript 对象的渲染器。无序依赖 DOM 或原生移动环境。这个包可以很容易地抓取由 ReactDOM 或 React Native 渲染的平台视图层次结构（类似于dom树）的快照，而无需使用浏览器或 `jsdom`。

     ```jsx harmony
     import TestRenderer from 'react-test-renderer'

     const Link = ({page, children}) => <a href={page}>{children}</a>

     const testRenderer = TestRenderer.create(
       <Link page={'https://www.facebook.com/'}>{'Facebook'}</Link>
     )

     console.log(testRenderer.toJSON())
     // {
     //   type: 'a',
     //   props: { href: 'https://www.facebook.com/' },
     //   children: [ 'Facebook' ]
     // }
     ```

148. ### ReactTestUtils 包的目的是什么?

     *ReactTestUtils* 在 `with addons` 包中提供，允许您针对模拟的DOM执行操作，以进行单元测试。

149. ### 什么是 Jest?

     *jest* 是facebook基于jasmine创建的一个javascript单元测试框架，提供自动模拟创建和 `jsdom` 环境。它通常用于测试组件。

150. ### Jest 比 Jasmine有什么好处?

      与Jasmine 相比有几种有点:

     - 自动查找要在源代码中执行的测试.
     - 运行测试时自动模拟依赖项.
     - 允许您同步测试异步代码.
     - 使用假DOM实现（通过`jsdom`）运行测试，以便可以在命令行上运行测试。.
     - 在并行进程中运行测试，以便它们更快完成.

151. ### 给出一个简单的Jest测试用例示例

     让我们为在`sum.js`文件中添加两个数字的函数编写一个测试：

     ```javascript
     const sum = (a, b) => a + b

     export default sum
     ```

     创建一个名为`sum.test.js`的文件，其中包含实际测试：

     ```javascript
     import sum from './sum'

     test('adds 1 + 2 to equal 3', () => {
       expect(sum(1, 2)).toBe(3)
     })
     ```

     然后将以下部分添加到`package.json`中：

     ```json
     {
       "scripts": {
         "test": "jest"
       }
     }
     ```
     
     最后，运行`yarn test`或 `npm test`，Jest将打印结果：

     ```console
     $ yarn test
     PASS ./sum.test.js
     ✓ adds 1 + 2 to equal 3 (2ms)
     ```
