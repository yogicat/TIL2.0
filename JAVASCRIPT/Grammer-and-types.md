## Grammer and Types

### Variables

Variable is a container for a value

**`var`**
- Declares a variable, optionally initializing it to a value
- `var` defines a variable globally, or locally to an entire function regardless of block scope

**`let`**
- Declares a block-scoped, local variable, optionally initializing it to a value
- `let` allows you to declare variables that are limited *in scope to the block, statement, or expression* on which it is used

**`const`**
- Declares a block-scoped, *read-only* named constant


```
function varTest() {
  var x = 1;
  if (true) {
    var x = 2;  // same variable!
    console.log(x);  // 2
  }
  console.log(x);  // 2
}

function letTest() {
  let x = 1;
  if (true) {
    let x = 2;  // different variable
    console.log(x);  // 2
  }
  console.log(x);  // 1
}
```

```
var x = 'global';
let y = 'global';
console.log(this.x); // "global"
console.log(this.y); // undefined
```


### Variable hoisting

```
/**
 * Example 1
 */
console.log(x === undefined); // true
var x = 3;

/**
 * Example 2
 */
// will return a value of undefined
var myvar = 'my value';

(function() {
  console.log(myvar); // undefined
  var myvar = 'local value';
})();
```

### Function hoisting

```
/* Function declaration */

foo(); // "bar"

function foo() {
  console.log('bar');
}


/* Function expression */

baz(); // TypeError: baz is not a function

var baz = function() {
  console.log('bar2');
};
```

---

## Data structures and types

**Data types**
- Primitives (values can contain only a single thing)
  1. Boolean - *true* and *false*
  2. null - `null` value / for unknown values
  3. undefined - top-level property whose value is not defined / unassigned values
  4. Number - an integer or floating point number
  5. String - text, characters
- Symbol (new in ECMA 2015) - its instances are unique and immutable
- Object (more complex data structures)




### Number

- integer and floating point numbers
- `Infinity`, `-Infinity` (1 / 0 -> Infinity)
- `NaN` represents a computational error


### String

- `"hi"` Double quotes
- `'hi'` Single quotes
- ``hi`` Template literals - can embed variables and expressions into a string by wrapping them in `${…}`

### null

- `null` does not beling to any of the types, seperate type of its own
- special value which represents 'nothing', 'empty' or 'value unknown'


### undefined

- 'value is not assigned'
- if a variable is declared, but not assigned, then its value is undefined.

### Object

- objects are used to store collections of data and more complex entities



