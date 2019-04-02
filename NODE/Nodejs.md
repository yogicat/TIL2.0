## Intro to Nodejs



- Environment to run JavaScript outside a browser
- Built on Chrome's V8 JavaScript engine
- Created by Ryan Dahl in 2009



---



### What can I create with Nodejs?

- Tooling (build, automation - webpack, gulp, etc)
- API's (REST, Realtime, GraphQL, etc)
- CDNs
- Shareable Libraries
- Desktop Applications (Electron, etc)
- IoT (Johnny Five, etc)



---



### Installing Node

- Using NVM(node version manager)!!

  - recommended
  - allows you to run many versions of Node whenever

  

- From Nodejs Source

  - easiest way to install
  - limits your options for have many versions of Nodejs
  - can cause permission errors



---



### Running Nodejs code

- Interactive REPL (Read, Evaluate, Print, Loop) 
  - testing, playing
  - start by just typing `$ node`  
- CLI Executable
  - `$ node somefile.js`

**REPL for playing around, CLI for everything else!**



---



node가 여러개 설치 된 경우 (nvm, brew등으로 인해) 어떤 노드를 쓰고 있는지 확인 하고 싶을때 `$ which node`

`bash_profile`

`bashrc`

---

### Browser and Nodejs



Browser

- Build interactive apps for the web
- DOM
- Window
- Fragmentation - (browser handles version not you.)
- optional modules (es6)
- Async



Nodejs

- Build server side apps and scripts
- no GUI, no DOM (but can virtualize DOM)
- no window but dose have a global
- versioned, so no fragmentation.
- Required modules (commomjs +)
- Async
- No browser based APIs



---



### Globals

- `process` - has information about the environment the program is running in
- `require` - function to find and use modules in current module
- `__dirname` - the current directory path
- `module` - information about current module, methods for making module consumable
- `global` - like window, its the 'global' object. Almost NEVER use this.



---



### modules in Nodejs

- encapsulated code
- uses CommonJS for its module system
- ESM (ecmascript modules) **new standard**



#### Creating modules

- All your Nodejs code are already modules.
- just Export it. `$ module.exports = something ` 

Importing modules

```node
// lib.js
module.export = () => {
  console.log('hello i am library')
}
```

```node
// app.js
const someModule = require('./lib')
```

- 앱내에서 내가 작성한 코드를 불러올때는 항상 `.` 입력!
- lib.js에서 모듈은 이름없이 바로 export되었으므로 app.js에서 원하는 변수명으로 불러 올 수 있다.