### Fund of ReactJS

#### Requirements:
- npm
- node.js
- yarn

#### Intro to React
- Composition
- Unidirectional Dataflow
  + if the state changes, the UI updates.
  + Data -> UI
- not Framework, it's UI library

#### Webpack
- transfiler
- ES6
- transform to normal .js .png. .css
- decided to use create react app by facebook 

#### Start creating app
- get into desired dir
- `create-react-app [foldername]`
- `cd [foldername]`
- `yarn start`

#### jsx?
- language that use for making react components 

#### components
- all components should include render function
- `ReactDOM.render(<App />, document.getElementById('root'));`:app component를 root에 render함
- ReactDOM: 리액트를 웹사이트에 rendering하는 것을 도와주는 모델
- 리액트를 사용해서 웹사이트에 올려놓고 싶을때: reactDOM
- 리액트를 사용해서 모바일앱에 올려놓고 싶을때: reactNative

#### Overall Steps
1. Components
2. render
3. return
4. jsx

#### Dataflow with Props
- Props are the way a father component gives information to a child component

#### React LifeCycle - Render
1. componentWillMount() --> request API
2. render()
3. componentDidMount()
 
#### React LifeCycle - Update
1. componentWillReceiveProps()
2. shouldComponentUpdate()
3. componentWillUpdate()
4. render()
5. componentHasUpdate

#### state
- object

#### stateless function
- function that does not have state; dumb components
  + just to return something. 
  + no need update, mounting...
  + no lifecycle
  + functional component
- class component; smart components

#### Ajax
- Asynchronous JavaScript and XM
- JSON: JavaScript Object Notation; 오브젝트를 자바스크립트로 작성하는 기법 
- FETCH

#### refe
- https://reactjs.org/docs/react-component.html#constructor
- https://reactjs.org/docs/react-component.html#setstate
- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions

