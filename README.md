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
|8  | [React中state 是什么？](#React中state是什么) |
|9  | [React中porps 是什么？](#React中porps是什么) |
|10 | [state和porps 的区别？](#state和porps的区别) |
|11 | [为什么不应该直接更新state？](#为什么不应该直接更新state) |
|12 | [回调函数作为setState()参数的目的是什么？](#回调函数作为setState()参数的目的是什么)
|13 | [HTML和React事件绑定的区别是什么？](#HTML和React事件绑定的区别是什么) |
|14 | [如何在JSX回调中绑定方法或事件绑定？](#如何在JSX回调中绑定方法或事件绑定) |
|15 | [如何向事件绑定或回调中传递一个参数？](#如何向事件绑定或回调中传递一个参数) |
|16 | [React中合成事件是什么？](#React中合成事件是什么) |
|17 | [什么是内联条件表达式？](#什么是内联条件表达式) |
|18 | [什么是key属性，在数组中使用它们的好处是什么？](#什么是key属性，在数组中使用它们的好处是什么) |
|19 | [refs有什么用？](#refs有什么用) |
|20 | [如何创建refs？](#如何创建refs) |  
|21 | [什么是 forward refs？](#什么是forward-refs) |
|22 | [在refs回调函数和findDOMNode()应该首选哪一个？](#在refs回调函数和findDOMNode()应该首选哪一个) |
|23 | [为什么曾经refs是String类型？](#为什么曾经refs是String类型) |
|24 | [什么是虚拟DOM？](#什么是虚拟DOM) |
|25 | [虚拟DOM是如何工作的？](#虚拟DOM是如何工作的) |

## React 核心

1. ### 什么是React？

    React 是一个 **开源前端JavaScript库** 用于构建用户界面， 尤其是单页面应用程序。他被用于处理 web 和 移动 app 的视图层。 React 是由Facebook 的软件工程师 Jordan Walke 所创立的. React于2011年首次部署在Facebook的News Feed上，2012年首次部署在Instagram上。

2. ### React主要特点是什么？

    React 主要特点是:

    * 考虑到RealDOM操作很昂贵，它使用 **VirtualDOM** 而不是 RealDOM 。
    * 支持 **服务器端渲染**。
    * 遵循 *单向** 数据流或数据绑定。
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