#  Hooks

### 노트

- can't use hooks inside a `conditional`
- `useState` - works like `setState` but in the function component
- `useEffect` - use side effect, works like life-cycle methods
- `useContext` - use context api in the function component
- custom hooks' names must start with `use`

---

### 사용하기

리액트와 함께 `useState`를 임포트한다.
`import React, { useState } from 'react'`

함수형 컴포넌트의 가장 윗부분에 상태를 선언한다. (상태의 명, 업데이트 함수의 이름) 초기 상태 값을 useState함수의 인자로 넘겨준다.
`const [<state>, <setState>] = useState(<initialState>)>`


클래스 컴포넌트에서 처럼 life cycle method를 사용하고 싶을땐 `useEffect`를 사용한다. 첫번째 인자로 함수를 넘겨주고(함수 안에 componentDidMount처럼 사용될 로직을 적어준다.) 두번째 인자로는 `componentDidUpdate`처럼 업데이트 트레킹하고 싶은 상태를 넘겨준다. `useEffect(() => {}, [<업데이트하고 싶은 state>])`

---

### 참고자료

- https://reactjs.org/docs/hooks-intro.html
