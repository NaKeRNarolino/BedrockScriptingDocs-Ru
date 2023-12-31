Если вы знаете джаваскрипт хотя бы немного, можете пропустить этот урок.

## JS и TypeScript - языки которые используются скриптами. Мы будем изучать JavaScript (он легче)

Перед тем как начнем, надо уточнить, что символ ; в конце строки не обязателен в языке JS. Ставьте его на свое усмотрение.

#### Переменные
Чтобы создать переменную в JavaScript, мы используем ```let```
Для вывода информации в консоль мы будем использовать функцию ```console.log()```

```js
let myVar = 0
console.log(myVar)
// Вывод: 0
```

Переменные могут содержать все что угодно. Начиная от чисел и строк, заканчивая JSON Объектами и Entity майнкрафта.

#### Арифметика в JavaScript

Арифметические функции нужны чтобы взаимодействовать с переменными и значениями. Арифметических функций много — +, -, /, \*, % (Выдает остаток от деления). Есть и более комплексные функции, но они используются не очень часто. Есть так же сокращения этих действий
```js
var++ // добавляет единицу к переменной
var-- // минусует единицу из переменной
var*= 2 // умножает переменную на два, так же и со всеми другими — +=, -=, /=, %=
```

Использовать арифметику легко:

```js
let a = 1+2 //3
let b = 8%2 //0
let c = 3/2 //1,5
let d = a + b + c // 4,5
console.log(d*2)
// Вывод: 9
```

#### Массивы(Array) в JS.

Массивы - тип данных, как строки(String) и числа(Int). Он позволяет хранить много значений в одной переменной!

Чтобы создать массив, мы будем использовать такой синтаксис: 
```js
let myArray = [1,2,3,4,5]
console.log(myArray)
//Вывод: [1,2,3,4,5]
```

Мы можем добавлять значения и после создания массива, используя функцию ```.append()``` , а так же убирать значения с помощью ```.pop()```:

```js
myArray.append(6)
console.log(myArray)
//Вывод: [1,2,3,4,5,6]
myArray.pop()//Убираем 6
myArray.pop()//Убираем 5
console.log(myArray)
//Вывод: [1,2,3,4]
```

Стоит уточнить, что значения в массивах могут повторяться.

Если мы хотим обратится к какому либо конкретному элементу массива, мы сделаем это используя такой синтаксис. Запомните, что в JS счет в массивах начинается с нуля.
```js
console.log(myArray[0])//Первый элемент массива
//Вывод: 1
```

#### Циклы в JS
Циклы позволяют повторять какое то действием пару раз. Основных циклов 2, это For и While. 

```js
// Пример цикла for
for (let i=0; i < 5; i++) {
    console.log(i)
}
// Здесь i - переменная итератор
// i<5 - условие, при нарушении которого цикл остановиться
// i++ - выражение, которое выполняется каждый раз когда цикл работает
/*
Вывод:
0
1
2
3
4
*/

// пример цикла while
let a = 0
while(a < 5)
{
    console.log(a)
    a++
}
// Здесь a - переменная, которая используется для "контроля" цикла
// a < 5 - условие, при нарушении которого цикл остановиться
// a++ - нужен для того, чтобы не получить бесконечный цикл (бесконечный цикл=баги,лаги,краши)
// Вывод: такой же, как и у цикла for выше
```

Из этого примера видно, что циклы for и while в большинстве случаев **взаимозаменяемы**.

#### Цикл for на массивах

Для написания цикла на массив можно использовать такую структуру.
```js
for (let element of myArray)
{
    console.log(element)
}
/*
Вывод:
1
2
3
4
5
*/
```

#### Логические выражения, конструкции ЕСЛИ, ЕСЛИ НЕ.

В программировании всегда надо что-то проверять. Для проверки мы будем использовать данную конструкцию: 
```js
if (условие) {
    Ваш код
} else {
    Ваш код
}
```

В данной конструкции код в if будет выполняться только если **условие** равно **истине**. В JS есть логические операторы, которые нужны для проверки, ниже все они: 
```js
1 == 1 // True(истина), так как 1 = 1. Обратите внимание, что при присвоении значения переменной мы используем 1 знак =, а в логическом операторе — 2
1 < 2 // True, так как 1 < 2
3 > 5 // False(ложь), так как 3 не больше 5
1 <= 1 // Таким образом записывается ≤. True, так как 1≤1
5 >= 5 // Таким образом записывается ≥. True, так как 5≥5
2 != 3 // Таким образом записывается ≠. True, так как 2 не равна 3
```

Все примеры были с числами, для более простого понимания. Вы можете использовать операторы с большинство количеством типов данных.

Конструкция else (ЕСЛИ НЕ) не обязательна, но вы можете ее использовать.

```js
let a = 6
if (a < 5)
{
    console.log("Значение меньше 5!")
}
else {
    console.log("Значение больше или равно 5!")
}
```

#### Функции в JS

Предоставьте, что у вас есть код, который надо выполнять много раз, при том — в разных местах кода. Для этого мы можем использовать функции. Для создания функции используется такая конструкция: 
```js
function названиеФункции(аргументыФункции) {
    ...
    return тоЧтоВозвращаетФункция
}
```
А для вызова: 
```js
названиеФункции(аргументыФункции)
```
Приведу простой пример: 
```js
function plus(a, b) {
    let c = a + b
    return c
}

console.log(plus(1,4))
// Вывод: 5
```

Надо уточнить, что функции могут не иметь аргументов и/или возвращаемого значения.

#### Комментарии

Комментарии нужны чтобы оставить заметки в вашем коде. Для того чтобы создать однострочный комментарий мы будем использовать два слеша : //, а для многострочного: \/\*\*\/
Примеры: 
```js
// Это однострочный комментарий
/*
А
Это
Много
Строчный 
*/
```

***Комментарии не учитываются при запуске кода.***

На этом все, больше узнать можно на https://www.learnjavascript.online

А если вам нужна многофайловость → [[Многофайловость в JS]]