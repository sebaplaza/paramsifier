# paramsifier

This library parses function and class constructor parameters.

## How to use it ?

```js
import { parseParameterList } from "paramsifier";

// With Classes
class MyClass {
	constructor({ firstParam, secondParam }, thirdParam) {}
}

parseParameterList(MyClass.toString());
// [
//   { name: 'firstParam', optional: false },
//   { name: 'secondParam', optional: false },
//   { name: 'thirdParam', optional: false }
// ]

// With Functions
function myFunction(param1, param2, param3) {}

parseParameterList(myFunction.toString());
// [
//   { name: 'param1', optional: false },
//   { name: 'param2', optional: false },
//   { name: 'param3', optional: false }
// ]
```

## Credits

Original parser code has [been extracted](https://github.com/jeffijoe/awilix/issues/307) from [awilix](https://github.com/jeffijoe/awilix) param-parser. 
Thanks @jeffijoe
