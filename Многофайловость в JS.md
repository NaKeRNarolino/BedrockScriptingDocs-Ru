Когда у тебя большой проект, не очень удобно хранить весь код в одной папке. Для этого мы можем разделить весь код по папкам. Допустим, у нас есть такая структура файлов.

scripts↓
	...main.js
	...other↓
		......other.js

И нам надо в main.js использовать функцию из other.js

Мы будем использовать такую структуру:

```js
//other.js
export function func() {
    return "func"
}

export let val = "var"

// export нужен чтобы экспортировать что-либо
```

```js
// main.js
import {val, func} from './other/other.js' //путь к файлу

console.log(val)
console.log(func())
//Вывод: "var"
//"func"
```