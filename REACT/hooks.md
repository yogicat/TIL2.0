#  Hooks

리액트 16.8부터 새롭게 적용된 hooks를 사용하면 함수형 컴포넌트에서도 상태관리와 라이프사이클메서드를 클래스컴포넌트에서 보다 더 간결하게 사용할 수 있다. 커스텀 hook를 작성해 불필요한 중복을 방지할 수 있어 매우 유용하다. React Conf 2018에서 발표한 영상을 미리 볼것을 권한다. 특히 Dan의 발표는 전반적인 사용법을 이해하는데 **큰** 도움이 되었다. State hook외에도 다양한 hook를 제공한다.

**Basic Hooks**
- useState
- useEffect
- useContext

**Additional Hooks**
- useReducer
- useCallback
- useMemo
- useRef
- useImperativeHandle
- useLayoutEffect
- useDebugValue

---

### 노트

- Don’t call Hooks inside `loops`, `conditions`, or nested functions.
- `useState` - works like `setState` but in the function component
- `useEffect` - use side effect, works like lifecycle methods
- `useContext` - use context api in the function component
- custom hooks' names must start with `use`
- use `liner-plugin` for eslint support. [eslint-plugin-react-hooks](https://www.npmjs.com/package/eslint-plugin-react-hooks)

---

### 사용하기

리액트와 함께 `useState`를 임포트한다.
`import React, { useState } from 'react'`

함수형 컴포넌트의 가장 윗부분에 state를 선언한다. 초기 상태 값을 useState함수의 인자로 넘겨준다.
`const [<state>, <setState>] = useState(<initialState>)>`

```js
  const [name, setName] = useState('Ohda');
  // name은 상태의 이름, setName은 상태를 업데이트할 함수의 이름, 'ohda'는 초기상태값

  const [age, setAge] = useState(42);
  const [fruit, setFruit] = useState('banana');
```

`useState`는 현재의 상태값과 상태를 업데이트할 수 있는 함수를 반환한다.`useState`는 위에 코드에서 처럼 여러번 다른 상태값을 위해 사용 가능하다.


클래스 컴포넌트에서 처럼 life cycle method를 사용하고 싶을땐 `useEffect`를 사용한다. 첫번째 인자로 함수를 넘겨주고(함수 안에 `componentDidMount`처럼 사용될 로직을 적어준다.) 두번째 인자로는 `componentDidUpdate`처럼 업데이트 트레킹하고 싶은 상태를 넘겨준다. `useEffect(() => {}, [<업데이트하고 싶은 state>])`

---

### 참고자료

- https://reactjs.org/docs/hooks-intro.html
