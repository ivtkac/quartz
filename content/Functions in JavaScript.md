---
created: 2025-11-29
title: Functions in JavaScript
tags:
  - javascript
aliases:
---
- functions are defined with `function myname(variable) {}`

## Arrow functions

**Arrow functions** have a shorter syntax compared to regular functions. You can skip keyword `function`

 ```javascript
  let greet = name => "Hello, " + name;
  console.log(greet("gearxxed")) // Outputs: "Hello, gearxxed"
  ```

> [!error] Limitations
> - no binding of `this`
> - not suitable as methods
> - can't be used as Contstructors
> - arrow functions and argument object is a missing link

> [!question] When and why use?
> - suited in callbacks (solve `this` issue)
> - with array methods (concise and clear)
> - variadic functions (easy multiple arguments)
