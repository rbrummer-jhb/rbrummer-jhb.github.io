---
css: js
layout: js
permalink: /js/
---

## Section 1 | Overview & Setup

These notes are based of off this course:
<br/>[https://www.udemy.com/course/the-complete-javascript-course/](https://www.udemy.com/course/the-complete-javascript-course/)

>

- Fundamentals
- Developer Skills
- DOM Manipulation
- How JavaScript Works
- Modern Operators (ES6+)
- Functions
- Arrays
- Numbers, Dates & Timers
- Advanced DOM
- Object-Oriented JS
- Mapty Project
- Asynchronous JS
- Modern JA Applications
- Forkify Project
- Deployment & Git

Download Visual Studio Code [here](https://code.visualstudio.com/download).

## Section 2 | Fundamentals

You can hit `CTRL + SHIFT + J` (Windows), or `right-click > Inspect` to open the Developer Tools in Chrome to gain access to the console.

You can write **JavaScript** in the console and it will be interpreted after hitting **Enter**.

```javascript
alert("Hello World!");

1 + 2 + 3 + 4; // 10
```

You can navigate through your previous console entries with the **up arrow**.

> JavaScript is a **high-level**, **object-oriented**, **multi-paradigm** programming language.

- The **language** is used to give the computer instructions.
- **High-level** : you don't have to worry too much about complexities like memory management.
- **Object-oriented** : based on objects for storing data.
- **Multi-paradigm** : accommodates a variety of programming styles (imperative & declarative programming; the way of structuring code).

In **Web Development** JavaScript is used alongside **HTML** & **CSS** to build web applications.

>

- **HTML** : Content. _(Nouns)_
- **CSS** : Presentation. _(Adjectives)_
- **JS** : Dynamic effects & Loading data. _(Verbs)_

Some popular **Web Development** JavaScript frameworks & libraries are **React**, **Angular** & **View** _(frontend)_, and **NodeJS** _(backend; web servers)_.

You can also build **Native Mobile Applications** with JavaScript using **React Native**, and <br/>
**Native Desktop Applications** using **Electron**.

Use the `<script> [scripts] </script>` tags to include inline JavaScript into your **HTML** document,<br/>
and they are usually placed at the end of the `<body></body>` tags.

`alert( [string] )` to display a pop up message in the browser.

```html
<script>
  let js = "bruce wayne";
  if (js === "bruce wayne") alert("I'm Batman.");

  console.log(1 + 2 + 3 + 4); // console will return 10
</script>
```

Alternatively, you can specify a source to link to JavaScript files containing scripts <br/>`<script src=" [script filename] "></script>`.<br/>
_(Beware of where your script file is located)_

```html
<script src="script.js"></script>
```

A **value** is a piece of data.<br/>
A **variable** is like a box in your computer's memory, and the **assigned value** is stored inside of that box.

`let [variable name]` to declare a variable.<br/>
`console.log( [expression] )` to log to the browser console.<br/>
`;` semicolons are used to end statements and are a good programming practice.<br/>

```javascript
// "Eminem" is the literal value
console.log("Eminem");

// 42 is the literal value
console.log(42);

let firstName = "Brimstone";
console.log(firstName);
```

| console output |
| :------------- |
| Eminem         |
| 42             |
| Brimstone      |

When naming variables it is a good practice to use camel Case : `thisIsCamelCase`<br/>
and to give them descriptive names.<br/>
**Variable names** may contain `_` **underscores**, `123` **numbers**, and `$` **dollar signs**.<br/>
Variable names can however not start with a **number**, or be named with a JavaScript **keyword**.<br/>
Variable names containing all **UPPERCASE** letters are reserved for declaring **constants**.<br/>
**CONSTANTS** are variables whose values will not change.

```javascript
// these variable names are descriptive
let myFirstJob = 'Programmer';
let myCurrentJob = 'Teacher';
// these variable names are not descriptive
let j1 = 'programmer';
let j2 = 'teacher';

// this is a CONSTANT
let PI = 3.141;

// these will throw errors

// starts with a number
let 3years = 3;
// uses a keyword as a variable name
let function = 'arigato';
```

A **VALUE** can either be an **OBJECT** or a **PRIMITIVE**.<br/>
There are **7 Primitive Data Types**:

>

1. Number _(always floating points; decimals & integers)_<br/>
   `let age = 23;`
2. String _(used for text; double or single quotes)_<br/>
   `let firstName = 'Hanzo';`
3. Boolean _(logical type; true of false)_<br/>
   `let isOfAge = true;`
4. Undefined _(does not have an assigned value)_ <br/>
   `let shenanigans;`
5. Null _(also means 'empty value' in some circumstances)_
6. Symbol (ES2015) _(defines a value that is unique & immutable)_
7. Bigint (ES2020) _(for integers that are too large for the number type)_

**Comments** are good for documenting code and are ignored by JavaScript.

```javascript
// single line comment

/*
multi-line comment
*/

// wubba lubba dub dub
let aCoolShow = "Rick & Morty";
```

JavaScript has **Dynamic Typing**; you don't have to specify the data type of the variable's value.<br/>
The **value** has a type NOT the **variable**.

`typeof` to get the value's data type.

```javascript
let isStrong = true; // boolean value
/*
'let' keyword is omitted,
because we are reassigning
a value to the same variable,
or mutating the variable
*/
isStrong = "YES!"; // string value; dynamically type casted

console.log(typeof 47);
console.log(typeof isStrong);
isStrong = false;
console.log(typeof isStrong);
```

| Console Output |
| :------------- |
| number         |
| string         |
| boolean        |

**Undefined** is different from other data types; the **variable & value** can be **undefined**.

```javascript
let year; // empty variable
console.log(year);
console.log(typeof year);
```

| Console Output |
| :------------- |
| undefined      |
| undefined      |

Using `const` is a good practice for declaring variables.<br/>
Use `let` if you are sure the variable's value will change.<br/>
`var` is the old way of declaring variables; avoid this.<br/>
Omitting these declaration keywords causes JavaScript to create a property on the global object.

```javascript
let age = 30;
age = 31; // age mutated

const birthYear = 1990;
birthYear = 1991; // throws TypeError; immutable

var job = "programmer"; // old declaration style; avoid
job = "teacher"; // job mutated

lastName = "Schwarzeneggar"; // declaration keyword omitted
console.log(lastName); // still legal
```

| Console Output |
| :------------- |
| Schwarzeneggar |

Basic operators for **Arithmetic**, **Concatenation** & **Assignment** and their **Precedence**.<br/>
`x > y` x greater than y.<br/>
`x >= y` x greater than or equal to y.<br/>
`x < y` x less than y.<br/>
`x <= y` x less than or equal to y.<br/>
`x ** y` x to the power of y.<br/>

```javascript
// arithmetic operators
const now = 2077;
const ageGandalf = now - 1011;
const ageGaladriel = now - 420;
console.log(ageGandalf, ageGaladriel);

// 2 ** 3 means 2 to the power of 3 = 2 * 2 * 2
console.log(ageGandalf * 2, ageGandalf / 10, 2 ** 3);

const firstName = "greatest";
const lastName = "ever";
console.log(firstName + " " + lastName);

// assignment operators
// arithmetic takes precedence over assignment
let x = 10 + 5;
x += 10; // x = x + 10 = 25
x *= 4; // x = x * 4 = 100
x++; // x = x + 1
x--; // x = x - 1
console.log(x);

// comparison operators
console.log(ageGandalf > ageGaladriel);
console.log(ageGaladriel >= 18);

const isFullAge = ageGaladriel >= 18;

// arithmetic takes precedence over comparison
console.log(now - 1991 > now - 2018);
```

| Console Output |
| :------------- |
| 1066 1657      |
| 2132 106.6 8   |
| greatest ever  |
| 100            |
| false          |
| true           |
| true           |

### Strings & Template Literals

JavaScript has **Type Coercion** which will convert value types. _(See below)_:

```javascript
const firstName = "Bane";
const job = "villain";
const birthYear = 1977;
const year = 2077;
const bane =
  "I'm " + firstName + ", a " + (year - birthYear) + " year old " + job + "!";
```

**Template Literals (ES2015)** can assemble multiple pieces into a string with **`` backticks**
and this notation for variables `${ variableName }`.

```javascript
const bane2 = `I'm ${firstName}, a ${year - birthYear} year old ${job}!`;

// inserting newlines with single quotes
console.log(
  "String with \n\
multiple \n\
lines"
);

// inserting mewlines with backticks
console.log(`String with
multiple
lines`);
```

### Conditionals

`if()` to declare a **Control Structure** or condition.

```javascript
const age = 15;

if (age >= 18) {
  console.log("Sherlock can start his driving license");
} else {
  const yearsLeft = 18 - age;
  console.log(`Sherlock is too young. Wait another ${yearsLeft} years`);
}
```

### Type Conversion & Coercion

Type **Conversion** is explicit **conversion/casting** of types _(manual)_.<br/>
Type **Coercion** is implicit **conversion/casting** of types _(automatic)_.
JavaScript will try to convert different value types beside an operator to the same type.<br/>
`Number( [expression] )` to cast to a number type.<br/>
`String( [expression] )` to cast to a string type.<br/>
You cannot convert to **undefined** or **null**.

```javascript
const inputYear = "1991";

console.log(Number(inputYear), inputYear); // 1991 "1991"
console.log(Number(inputYear) + 18); // 2009

// this will return NaN (Not a Number)
// which means an invalid number
console.log(Number("string"));

// oddly the type of NaN is number
console.log(typeof NaN);

console.log(String(23), 23); // "23" 23

// this invokes type coercion
console.log("I am " + 23 + " years old");

// this will convert to numbers and return the result
console.log("23" - "10" - 3); // 10

// this will simply concatenate the numbers because
// the + operator has another function with strings
console.log("23" + "10" + 3); // 23103

console.log("23" / "2"); // 11.5
console.log("23" > "10"); // true

let n = "1" + 1;
n = n - 1;
console.log(n); // 10
```

### Truthy & Falsy Values

There are **5 Falsy Values** in JavaScript. These are values that will become **false** when converted to a **boolean**.

1. 0
2. '' (empty string)
3. Null
4. NaN (Not a Number)
5. undefined

```javascript
console.log(Boolean(0)); // false
console.log(Boolean(undefined)); // false
console.log(Boolean("String")); // true
console.log(Boolean({})); // true
console.log(Boolean("")); // false

const money = 0;
if (money) {
  console.log("Don't spend it all.");
} else {
  console.log("You should get a job!");
}

let height; // undefined
if (height) {
  console.log("height is defined");
} else {
  console.log("height is undefined");
}
```

### Boolean Logic

Truth Table for **AND**:<br/>
A **AND** B:

| | | **A** | |
| | **AND** | TRUE | TRUE |
| **B** | TRUE | **TRUE** | FALSE |
| | FALSE | FALSE | FALSE |

Truth table for **OR**:<br/>
A **OR** B:

| | | **A** | |
| | **OR** | TRUE | FALSE |
| **B** | TRUE | TRUE | TRUE |
| | FALSE | TRUE | FALSE |

**NOT** inverts **true/false** values.

### The Switch Statement

```javascript
const day = "monday";

switch (day) {
  case "monday":
    console.log("Plan course structure.");
    console.log("Go to coding meetup.");
    break;
  case "tuesday":
    console.log("Prepare theory videos.");
    break;
  case "wednesday":
  case "thursday":
    console.log("Write code examples.");
    break;
  case "friday":
    console.log("Record videos");
    break;
  case "saturday":
  case "sunday":
    console.log("Enjoy the weekend.");
    break;
  default:
    console.log("Invalid day");
}

// this is the same as the above switch statement
if (day === "monday") {
  console.log("Plan course structure.");
  console.log("Go to coding meetup.");
} else if (day === "tuesday") {
  console.log("Prepare theory videos.");
} else if (day === "wednesday" || day === "thursday") {
  console.log("Write code examples.");
} else if (day === "friday") {
  console.log("Record videos");
} else if (day === "saturday" || day === "sunday") {
  console.log("Enjoy the weekend.");
} else {
  console.log("Invalid day");
}
```

**SIDE NOTE**:

- An **expression** is anything that produces a value.<br/>

  > 4 + 7 // this is an expression

- A **statement** is comprised of expressions and end with semicolons `;`.

  > const myNum = 4 + 7; // this is a statement

- **Template Literals** can only take expressions.
  > console.log(`${50 - 47} is my favourite number.`);

### The Conditional / Ternary Operator

`[condition] ? [expression] : [alternative expression] ;` to use the **Ternary Operator**.

```javascript
const age = 23;
age >= 18
  ? console.log("I like to drink wine.")
  : console.log("I like to drink water");

const drink = age >= 18 ? "wine" : "water";
console.log(drink);

// This is the above statement uncondensed
let drink2;
if (age >= 18) {
  drink2 = "wine";
} else {
  drink2 = "water";
}
console.log(drink2);

// template literal
console.log(`I like to drink ${age >= 18 ? "wine" : "water"}.`);
```

|    Console Output     |
| :-------------------: |
| I like to drink wine. |
|         wine          |
|         wine          |
| I like to drink wine. |

### Strict Mode

`'use strict';` to activate **Strict Mode** in JavaScript.<br/>
This **String statement** forbids us from doing certain things and it creates visible errors in the console instead of failing silently if there is something wrong in the code.<br/>

```javascript
"use strict";

let hasDriversLicense = false;
const passTest = true;

// this ReferenceError will not be thrown without strict mode
if (passTest) hasDriveLicense = true;

// these will throw SyntaxError, because strict mode reserves
// some words that might become keywords in the future
const interface = "Audio";
const private = 47;
```

### Functions

`function [function name]() {}` to **declare** a function.<br/>
_(Don't use reserved keywords for function names.)_

```javascript
function logger() {
  console.log("My name is Watson");
}
// this is calling / running / invoking the function
logger();
```

Functions can **return or receive** data.<br/>
You can **pass parameters/arguments** to a function<br/>
`function [function name]( [param1], [param2] ) {}`

Not all functions need to **return data** or **accept parameters**.<br/>
Functions allow us to create more maintainable code and helps enforce the **D.R.Y** principle _(**D**on't **R**epeat **Y**ourself)_.

```javascript
function fruitProcessor(apples, oranges) {
  const juice = `Juice with ${apples} apples and ${oranges} oranges.`;
  return juice;
}
// this captures the result of the function
const appleJuice = fruitProcessor(5, 0);
// this logs the captured result
console.log(appleJuice);
// this simply logs the result of the function
console.log(fruitProcessor(4, 7));
```

|           Console Output           |
| :--------------------------------: |
| Juice with 5 apples and 0 oranges. |
| Juice with 4 apples and 7 oranges. |

Function **declarations** can be called before they are defined.<br/>
Function **expressions** can **NOT** be called before they are defined.<br/>
Both function **Declarations** & function **Expressions** have their place.<br/>
It's generally a good practice to have function declarations at the top of the script file.

```javascript
// calling before declaration
console.log(calAge1(1997));
// this is a function declaration
function calAge1(birthYear) {
  return 2077 - birthYear;
}

// this is a function expression
const calAge2 = function (birthYear) {
  return 2077 - birthYear;
};
// calling after declaration
console.log(calAge2(1997));
```

### Arrow Functions

**Arrow Functions** were introduced in ES6 _(ECMAScript6)_, and they can be one liner functions.

```javascript
const calcAge1 = (birthYear) => 2097 - birthYear;
console.log(calcAge1(1997));

const yearsUntilRetirement = (birthYear, firstName) => {
  const age = 2077 - birthYear;
  const retirement = 65 - age;
  return `${firstName} retires in ${retirement} years.`;
};
console.log(yearsUntilRetirement(1997, "Sherlock"));
console.log(yearsUntilRetirement(1998, "Watson"));
```

|         Console Output         |
| :----------------------------: |
| Sherlock retires in -15 years. |
|  Watson retires in -14 years.  |

**Functions calling other functions** _(docstrings/'contracts' included)_.

**Docstrings** are a good practice in any programming language.<br/>
They are used to document your code, especially **functions**.<br/>
You can create a docstring by typing `/**` and then hitting **Enter**.<br/>
Most editors will autocomplete the docstring for you by filling it with the necessary placeholder words.

```javascript
/**
 * Multiplies the parameter (fruit) with 4
 * @param {int} fruit
 * @returns fruit * 4
 */
function cutPieces(fruit) {
  return fruit * 4;
}

/**
 * Calls cutPieces() and then creates a
 * template literal with the parameters
 * @param {int} apples
 * @param {int} oranges
 * @returns juice (Template Literal String)
 */
function fruitProcessor(apples, oranges) {
  const applePieces = cutPieces(apples);
  const orangePieces = cutPieces(oranges);

  const juice = `Juice with ${applePieces} pieces of apple and
    ${orangePieces} pieces of orange.`;
  return juice;
}
console.log(fruitProcessor(2, 3));
```

Anything **after the return statement** in a function is **ignored**.<br/>
So there are **3 different ways** of writing functions:

- Function Declarations
  ```javascript
  function calcAge(birthYear) {
    return 2037 - birthYear;
  }
  ```
- Function Expressions
  ```javascript
  const calcAge = function (birthYear) {
    return 2037 - birthYear;
  };
  ```
- Arrow Functions
  ```javascript
  const calcAge = (birthYear) => 2037 - birthYear;
  ```

**Arrays & Objects** are the most important data structures in JavaScript.  
Arrays are zero-based.

```javascript
const friends = ["qui gon jin", "obi wan kenobi", "yoda"];
console.log(friends);
console.log(friends[0]);
console.log(friends.length);
console.log(friends[friends.length - 1]);
```

|              Console Output               |
| :---------------------------------------: |
| ['qui gon jin', 'obi wan kenobi', 'yoda'] |
|                qui gon jin                |
|                     3                     |
|                   yoda                    |

Any positon of an array simply need to be an expression.

```javascript
const someName = "Sam Jackson";
const someArray = [1, 2, 3];

const randomThings = [47, "windu", someName, 4 + 20, someArray];
```

`.push( [expression] )` to add elements to the end of the array.  
`.push()` also returns the length of the array.  
`.unshift( [expression] )` to add elements to the start of the array;  
also returns the length of the array.

```javascript
const friends = ["qui gon jin", "obi wan kenobi", "yoda"];
const newLength = friends.push("anakin");
console.log(friends);
console.log(newLength);
```

|                   Console Output                    |
| :-------------------------------------------------: |
| ['qui gon jin', 'obi wan kenobi', 'yoda', 'anakin'] |
|                          4                          |

`.pop( [expression] )` to remove elements from the end of the array.  
`.pop()` does **not** return the length of the array; it returns the removed element.  
`.shift( [expression] )` to remove the first element of the array;  
also returns the removed element.

```javascript
const friends = ["qui gon jin", "obi wan kenobi", "yoda"];
console.log(friends.pop());
console.log(friends);
```

|          Console Output           |
| :-------------------------------: |
|              'yoda'               |
| ['qui gon jin', 'obi wan kenobi'] |

`.indexOf( [expression ] )` to get the index / position of the element in the array.

```javascript
const friends = ["qui gon jin", "obi wan kenobi"];
console.log(friends.indexOf("obi wan kenobi"));
```

| Console Output |
| :------------: |
|       1        |

`.includes( [expression ] )` also gets the index / position of the element in the array,  
but it also performs type checking.

```javascript
const arr = ["qui gon jin", "obi wan kenobi", "47", 42];
console.log(arr.indexOf("47"));
console.log(arr.includes(47));
```

| Console Output |
| :------------: |
|       2        |
|     false      |

**Objects** are good for unstructured data.  
You can access the properties of an object using **dot .** or **bracket []** notation.  
You can build expressions with **bracket [] notation**.  
Any function that is attached to an object is called a **method**.

```javascript
const obj = {
    firstName: 'Michael',
    lastName: 'Scott',
    age: 55 - 10,
    job: 'Regional Manager'
    // this property holds a method
    calcAge: function (birthYear) {
        return 2037 - birthYear;
    }
};
console.log(obj.firstName);
console.log(['lastName']);
// dot notation
console.log(obj.calcAge(1990));
// bracket notation
console.log(obj['calcAge'](1990));

const nameKey = 'Name';
console.log(obj['first' + nameKey]);
console.log(obj['last' + nameKey]);
```

| Console Output |
| :------------: |
|    Michael     |
|     Scott      |
|       47       |
|       47       |
|    Michael     |
|     Scott      |

`for( [counter]; [condition]; [increment] ) { [instruction] }` to declare a **for loop** control statement.

```javascript
for (let counter = 1; counter <= 10; counter++) {
  console.log(`Dip dip potato chip ${counter}`);
}
```

|     Console Output     |
| :--------------------: |
| Dip dip potato chip 1  |
| Dip dip potato chip 2  |
| Dip dip potato chip 3  |
| Dip dip potato chip 4  |
| Dip dip potato chip 5  |
| Dip dip potato chip 6  |
| Dip dip potato chip 7  |
| Dip dip potato chip 8  |
| Dip dip potato chip 9  |
| Dip dip potato chip 10 |

Looping through an array.  
`continue` exits the current iteration of the loop and **continues** to the next one.  
`break` terminates the loop.

```javascript
const arr = [
  "Michael",
  "Scott",
  45,
  "Regional Manager",
  ["Dwight", "Kevin", "Oscar"],
];
// continue
for (let i = 0; i < arr.length; i++) {
  if (typeof arr[i] === "number") continue;
  console.log(arr[i], typeof arr[i]);
}
// break
for (let i = 0; i < arr.length; i++) {
  if (typeof arr[i] === "number") break;
  console.log(arr[i], typeof arr[i]);
}
// backwards looping
for (let i = arr.length - 1; i >= 0; i--) {
  console.log(arr[i]);
}
```

| Console Output _(continue)_  | Console Output _(break)_ | Console Output _(backwards looping)_ |
| :--------------------------: | :----------------------: | :----------------------------------: |
|        Michael string        |      Michael string      |     ["Dwight", "Kevin", "Oscar"]     |
|         Scott string         |       Scott string       |           Regional Manager           |
|   Regional Manager string    |                          |                  45                  |
| ["Dwight", "Kevin", "Oscar"] |                          |                Scott                 |
|                              |                          |               Michael                |

A loop within a loop:

```javascript
// runs through first iteration
for (let exercise = 1; exercise < 4; exercise++) {
  console.log(`--- Starting exercise ${exercise} ---`);
  // runs through all iterations
  for (let rep = 1; rep < 4; rep++) {
    console.log(`Exercise ${exercise} : Lifting weights rep ${rep}`);
  }
}
```

|           Console Output           |
| :--------------------------------: |
|  --- **Starting exercise 1** ---   |
| Exercise 1 : Lifting weights rep 1 |
| Exercise 1 : Lifting weights rep 2 |
| Exercise 1 : Lifting weights rep 3 |
|  --- **Starting exercise 2** ---   |
| Exercise 2 : Lifting weights rep 1 |
| Exercise 2 : Lifting weights rep 2 |
| Exercise 2 : Lifting weights rep 3 |
|  --- **Starting exercise 3** ---   |
| Exercise 3 : Lifting weights rep 1 |
| Exercise 3 : Lifting weights rep 2 |
| Exercise 3 : Lifting weights rep 3 |

Looping through an **array of arrays**:

```javascript
const blue = [
  ["I'm", "blue"],
  ["da", "ba", "dee"],
  ["da", "ba", "daa"],
];

for (let i = 0; i < blue.length; i++) {
  // console.log(blue[i]);
  for (let j = 0; j < blue[i].length; j++) {
    console.log(blue[i][j]);
  }
}
```

| Console Output |
| :------------: |
|      I'm       |
|      blue      |
|       da       |
|       ba       |
|      dee       |
|       da       |
|       ba       |
|      daa       |

`[counter]; while ( [condition] ) { [instruction]; [increment] }`  
to declare a **while loop**.  
A **while loop** doesn't necessarily need a counter.  
It can have a terminating condition.

```javascript
let rep = 1;
while (rep <= 5) {
  console.log(`Lifting weights rep ${rep}`);
  rep++;
}
```

|    Console Output     |
| :-------------------: |
| Lifting weights rep 1 |
| Lifting weights rep 2 |
| Lifting weights rep 3 |
| Lifting weights rep 4 |
| Lifting weights rep 5 |

How to think like a developer:

1. Understand the problem & ask the right questions.
2. Divide & conquer; identify sub-problems.
3. Do as much research as you have to.
4. Write some pseudo code.

`console.table` can give you a nice format similar to a markdown table in the console window.

You can set **breakpoints** with the Chrome developer console **debugger**.  
`ctrl+shift+j > Sources > script.js > insert into line number pane`

JavaScript also has a `debugger;` statement.

### Section 6 | HTML & CSS Crash Course (Optioanl)
# Section 7 | DOM & Events Fundamentals

To select an element that has a **class** or **id** and its content,  
you can also use the `.getElementById()` method without the `#` symbol in its argument to select an element that has an **id**:
```html
<!-- index.html -->

<p class="class-name">This is the text content!</p>
```
*(`.getElementById()` is supposedly faster than `.querySelector()`)*
```js
// script.js

// for a class
document.querySelector('.class-name');

// for an id
document.querySelector('#id-name');
// OR
document.getElementById('id-name');
```
| Console Output |
|:-|
| This is the text content! |

## The DOM
The **D**ocument **O**bject **M**odel is a structured representation of HTML documents.  
It allows JavaScript to access HTML elements & styles to manipulate them.

The DOM is automatically created by the browser as soon as the HTML pages loads,  
and it has a trees structure.  
In the tree each HTML element is one object.

The DOM always start with the **document** object.  
The `<html>` element is the first child element of the document object.  
The `<head>` & `<body>` elements are the first child elements of the `<html>` element.

The DOM is **NOT** a part of the JavaScript language.  
The DOM and its methods are part of the Web APIs.
The Web APIs are libraries that browsers implement that JavaScript can access.
The Web APIs are written in JavaScript.

You can get the text content of an element using the `.textContent()` method,  
and the value of an element using the `.value()` method:
```js
console.log(document.querySelector('.class-name').textContent);
console.log(document.querySelector('.class-name').value);
```

Use **camelCase** to change the style of a selected element if the style's name contains hyphens `-`.
```js
// 'document.querySelector('body').style.background-color' becomes:
document.querySelector('body').style.backgroundColor = '#60b347';
```

To add an event listener to an element  
*(the first parameter is the 'event', the second is the function)*:
```html
<!-- index.html -->

<button class="btn">Again!</button>
```
```js
// script.js

// this adds an event listener to an element's 'click' event
document.querySelector('.btn').addEventListener('click', function() {
  // do some logic
});
```

It's a good practice to store element selections in their own variables:
```js
const modal = document.querySelector('.modal');
const overlay = document.querySelector('.overlay');
...
```
You can select multiple elements that have the same **'selector'** names with `.querySelectorAll()`:
```js
const btnsOpenModal = document.querySelectorAll('.show-modal');
```

You can also add events to **keys**. Keyboard events are global events.  
When an event occurs JavaScript creates an object.  
Key presses are stored in the **event** object.  
`.addEventListener()`'s second function argument can accept the event object.

# Section 8 | JavaScript Background Operations

> JavaScript is a high-level, prototype-based object-oriented, multi-paradigm, interpreted or just-in-time complied, dynamic, single-threaded, garbage-collected programming language with first-class functions and a non-blocking event loop concurrency model. ????

* **High Level**
  * The developer does not have to manage resources like memory allocation.
* **Garbage Collection**
  * JavaScript cleans memory automatically, it removes unused objects.
* **Interpreted / Just-in-time compiled**
  * JavaScript code is compiled to machine code inside its engine.
* **Multi-paradigm**
  * It supports multiple approaches of structuring code *(Procedural, OOP, FP)*.
* **Prototype-based Object-oriented**
  * Everything is an object except for primitives. *(Prototypal inheritance)*.
* **First-class functions**
  * Functions are treated as variables.
* **Dynamic**
  * Data types are dynamically typed.
* **Single-threaded**
  * JavaScript runs in one thread, it can only do one thing at a time.
  * A thread is a set of instructions that gets executed in the CPU.
* **Non-blocking event loop**
  * The non-blocking event loop executes long running tasks in the background,  
  and then puts it back into the thread.

### The JavaScript Engine
The program that executes JavaScript code.  
The most popular JavaScript is **Chrome's V8**.  
Any JavaScript has a **call stack** *(execution context)* and a **heap** *(unstructured memory pool that stores the objects)*.

### Compilation vs Interpretation
* In compilation, the entire source code is converted into machine code at once,  
and written to a portable, binary file that can be execute later.
* In interpretation, the source code is read, converted into machine code,  
and executed all at the same time.
* Interpretation is much slower than Compilation, but modern JavaScript makes use of both.  
This is known as **just-in-time** compilation.


1. Parsing *(realising)*.
    * The code is parsed into a data structure called the Abstract Syntax Tree *(AST)*.
    * The lines of code are split into pieces that are meaningful to the language *(**const** of **function**)*.
    * **The AST has nothing to do with the DOM tree**.
2. Compilation
    * AST is compiled into machine code.
3. Execution
    * The machine code is then executed right away *(call stack)*.
4. Optimization
    * The executed code is optimized by recompiling it during execution *(multiple times)*.

All these steps happen in special, inaccessible threads in the engine.

The JavaScript Runtime contains the Engine, the Web APIs and the Callback Queue.
The Node.js Runtime is the same except it has C++ Bindings & a Thread Pool instead of Web APIs.

### Execution Context

The first thing created in the execution context is the **Variable Environment** ( `let`, `const`, `functions()` ), then the **Scope Chain** and then the `this` keyword.  
Top-level code, code that is not inside any functions, gets executed first *(global execution context)*.  
Functions should only be executed when they are called, and they are executed after top-level code.  
Separate execution contexts are created for function calls. The same goes for methods.

The **global execution context** is added to the **call stack** first.  
Then if there are any functions their execution contexts are created and added to the call stack,  
and that becomes the **active execution context** and any variables inside this execution context get their own variable environments.  
Once execution finishes it is popped off the stack, and the previous execution context becomse the active execution context.

### Scope & Scoping (The Scope Chain)

Scoping is how the program's variables are **organized & accessed**.  
Lexical Scoping is controlled by **placement** of functions and& blocks in the code.  
Scope is the space / environment in which a certain variable is **declared**, there is:
* **Global** scope
  * this is for top-level code, variables here are accessible everywhere.
* **Function**/local scope
  * this is for variables inside a function, they are only accessible inside the function. 
* **Block** scope
  * this is similar to the function scope except `var` variables are accessible from outside unlike `let` & `const`.
  * 'block' refers to the `{}` curly brackets of a function.

Nested scopes have access to the variables inside their parent scopes.
```js
const hero = 'Bat';

function first() {
  // has access to hero
  if (hero === 'Bat') {
    hero += 'man';

    function second() {
      // has access to hero
      console.log(`I am ${hero}`);
    }
  }
}
```
**The scope chain has nothing to do with the execution context.**

### Hoisting

Hoisting is when a variable is declared with the `var` keyword, but it has not been initialized with a value yet.  
A **property** is created for it in the **Variable Environment object** with a **value** of `undefined`.  
This allows you to access that variable, that is declared, but before it is initialized, however, this is considered a bad practice. Avoid using the `var` keyword.

### 'this' Keyword

`this` is a special variable that gets created for every execution context.  
`this` points to the object that is calling its method/function.  
Arrow functions do not get their own `this` keyword. It will simply point to the global `window` object, or to the `this` keyword of its parent object.

Functions also have access to the `arguments` keyword.  
It is only available in regular functions.  
It can be useful for when your function is accepting more arguments than you initially specified.
```js
const addExpr = function(a, b) {
    console.log(arguments);
    return a + b;
};
addExpr(2, 5, 8, 12);
```
| Console Output |
|:-|
| Arguments(4) [2, 5, 8, 12, ... |


JavaScript has 8 **Primitive** data types:
* Number
* String
* Boolean
* Undefined
* Null
* Symbol
* BigInt

The rest:
* Object Literal
* Arrays
* Functions, etc

are **objects**.

Objects are reference types. They are stored right in the heap.  
Primitives are stored in the execution context in which they are created in the call stack.

You cannot change the value of `const` when working with primitives,  
but you can when working with reference types.  
Objects' value in the stack are **memory addresses** that point to objects in the heap.  
This value cannot change, because memory addresses cannot change their value:
```js
const agent = {
  name: 'J',
  age: 30
};
// this throws TypeError
agent = {};
```
You can create a **Shallow Copy** of an object using `Object.assign()`.  
This means that only top-level code is copied; it is not a **Deep Clone**.  
If there is another object inside this object,  
it is not copied, it is referenced.
```js
const agent = {
  name: 'J',
  age: 30,
  // this is an array, another object
  // it will change for both objects
  partners: ['K', 'worms', 'Z']
};

const agentCopy = Object.assign({}, agent);
agentCopy.name = 'James';
agentCopy.age = 40;
agentCopy.partners.push('Frank');

console.log(agent);
console.log(agentCopy);
```
| Console Output |
|:-|
| name: 'J', age: 30, partners(4): ['K', 'worms', 'Z', 'Frank'] |
| name: 'James', age: 40, partners(4): ['K', 'worms', 'Z', 'Frank'] |

# Data Structures, Modern Operators & Strings

### Destructuring

This involves breaking down complex data structures into variables.  
Below is array destructuring:
```js
const restaurant = {
  categories: ['American', 'Italian', 'Japanese'],
  starters: ['slide', 'ciabatta', 'maki'],
  mains: ['smash', 'pasta', 'yakatori'],
  order: function(starterIndex, mainIndex) {
    return [this.starters[starterIndex], this.mains[mainIndex]];
  }
};

const [category1, category2] = restaurant.categories;
console.log(category1, category2);

// this is a nice way to get multiple return values from a function/method
const [starterMeal, mainMeal] = restaurant.order(2, 1);
console.log(starterMeal, mainMeal);

// the values are easily swapped with destructuring
[mainMeal, starterMeal] = [starterMeal, mainMeal];
```
| Console Output |
|:-|
| 'American', 'Italian' |
| 'maki', 'pasta' |

Nested destructuring:
```js
const nested = [1, 2, [3, 4]];

// notice the skip
const [a, ,b] = nested;
console.log(a, b);

const [x, y, [z1, z2]] = nested;
console.log(x, y, z1, z2);

// setting default values
// this is useful for when
// data is coming from an API
const [p=1, q=1, r=1] = [8, 9];
console.log(p, q, r);
```
| Console Output |
|:-|
| 1, [3, 4] |
| 1, 2, 3, 4 |
| 8, 9, 1 |

Use `{}` curly brackets to destructure objects.  
The variable names have to be the same as the object's property names  
unless you reassign them to different names *(see second block)*:
```js
const agent = {
  name: 'J',
  age: 30,
  partners: ['K', 'worms', 'Z']
};

const { name, age, partners } = agent;
console.log(name, age, partners);
```
| Console Output |
|:-|
| 'J' 30 partners(3) ['K', 'worms', 'Z'] |

```js
const { name: agentName, age: agentAge, partners: agentPartners } = agent;
console.log(agentName, agentAge, agentPartners)
```
You can assign a default value to a variable if the property dose not exist:
```js
const { weapon = 'the noisy cricket', name, age, partners } = agent;
console.log(weapon, name, age, partners);
```
| Console Output |
|:-|
| 'the noisy cricket' 'J' 30 partners(3) ['K', 'worms', 'Z'] |

Objects can also be destructured as function parameters,  
and they can also be assigned default values:
```js
const restaurant = {
  categories: ['American', 'Italian', 'Japanese'],
  starters: ['slide', 'ciabatta', 'maki'],
  mains: ['smash', 'pasta', 'yakatori'],
  
  order: function({
    starterIndex,
    mainIndex,
    time = '20:00',
    address = 'Sesame'
  }) {
    console.log(`Order received! ${this.starterMenu[starterIndex]} and ${this.mainMenu[mainIndex]} will be delivered to ${address} at ${time}`);
  }
};

restaurant.order({
  starterIndex: 1,
  mainIndex: 2
});
```
| Console Output |
|:-|
| Order received! ciabatta and yakatori will be delivered to Sesame at 20:00 |

The `...` **spread operator** unpacks array elements, and it works on all iterables *(not objects)*.  
It's also good for merging & creating shallow copies of arrays.
```js
const arr = [7, 8, 9];
const newArr = [5, 6, ...arr];
console.log(newArr);

const food = {
  mains: ['smash', 'pasta', 'yakatori']
}
console.log(...food.mains);

const arrShallowCopy = [...arr];
const joinedArr = [...arr, ...newArr];
```
| Console Output |
|:-|
| (5) [5, 6, 7, 8, 9] |
| (3) ['smash', 'pasta', 'yakatori'] |

### The Rest Pattern

The `...` **spread operator** unpacks elements if it is on the **right** side of the `=` **assignment operator**,  
but if it is on the **left** side of the assignment operator it becomes the **rest operator** which packs the *rest* of the elements into a new array. It does include any skipped elements.
```js
// spread on the right
const arr = [1, 2, ...[3, 4]];
console.log(arr);

// spread on the left
const [a, b, ...others] = [1, 2, 3, 4, 5];
console.log(a, b, others);
```
| Console Output |
|:-|
| (4) [1, 2, 3, 4] |
| 1 2 (3) [3, 4, 5] |

**Short-circuiting** is when the boolean OR `||` operator gives precedence to its first **'truthy'** operand,  
or when the boolean AND `&&` operator gives precedence to its first **'falsy'** operand.  
The **Nullish Coalescing Operator** `??` returns the first **non-nullish** *(null & undefined)* value.
```js
// this will log 'Hello'
console.log(undefined || 0 || '' || 'Hello' || 23 || null);

// this will log null
console.log('Hello' && 23 && null && 'j');

// this will return 0
console.log(null ?? undefined ?? 0 ?? '');
```
The `for of` loop:
```js
const nums = [1, 2, 3, 4, 5];
for (const num of nums) console.log(num);
```
| Console Output |
|:-|
| 1 |
| 2 |
| 3 |
| 4 |
| 5 |

To get the index and the element value with a `for of` loop use destructuring & the `.entries()` method:
```js
const str = ['a', 'b', 'c'];
for (const [i, e] of str.entries()) console.log(`${i} ${e}`);
```
| Console Output |
|:-|
| 0 a |
| 1 b |
| 2 c |

The **Optional Chaining Operator** `?` checks if a property exists.  
It saves the effort of making `if` blocks.
```js
const restaurant = {
  openingHours: {
    thu: {
      open: 12,
      close: 22,
    },
    fri: {
      open: 11,
      close: 23,
    },
    sat: {
      open: 0, // Open 24 hours
      close: 24,
    },
  }
};
// this checks if the 'mon' property exists
console.log(restaurant.openingHours.mon?.open);
// this checks if the 'openingHours' property exists
console.log(restaurant.openingHours?.mon?.open);
```
Console Output |
|:-|
| undefined |
| undefined |

The **optional chaining** `?` *(does the value/property exist)* &  
the **nullish coalescing operator** `??` *(returns first non-null)*  
were implemented at the same time, so they work well together.
```js
...
const days = ['mon', 'tue', 'wed', 'thu', 'fri', 'sat', 'sun'];

// For Loop
for(const day of days) {
  const open = restaurant.openingHours[day]?.open ?? 'closed';
  console.log(`On ${day}, we open at ${open}`);
}

// Methods
console.log(restaurant.order?.(0, 1) ?? 'Method does not exist');

// Arrays
const users = [
  {name: 'J', email: 'agent@j.com'}
];
console.log(users[0]?.name ?? 'User array empty');
```
| Console Output |
|:-|
| On mon, we open at closed |
| On tue, we open at closed |
| On wed, we open at closed |
| On thu, we open at 12 |
| On fri, we open at 11 |
| On sat, we open at 0 |
| On sun, we open at closed |
| Method does not exist |
| J |

A **set** is a collection of unique values, meaning do duplicates.  
`.add()`, `.has()`, `.delete()`, `.size()` and `.clear()` are some common Set methods.
```js
const ordersSet = new Set(['Pasta', 'Pizza', 'Pizza', 'Risotto', 'Pasta', 'Pizza']);

console.log(ordersSet)
console.log('John');
```
| Console Output |
|:-|
| Set(3) {"Pasta", "Pizza", "Risotto"} |
| Set(4) {"J", "o", "h", "n"} |

A **map** can be used to map values to keys, but in this case the keys can be of any type.
```js
const rest = new Map();
rest.set('name', 'Bond');
console.log(rest);
```
| Console Output |
|:-|
| Map(1) {"name" => "Bond"} |

### Sources of Data

1. From the program itself:
    * Data written directly into source code *(e.g. status messages)*.
2. Form the UI:
    * Data input from the user or data written in DOM *(e.g. tasks in todo app)*.
3. From external sources:
    * Data fetched for example from web API *(e.g. recipe objects)*.

Collections of data are stored in **Data Structures**.

**Arrays** vs **Sets**:
| Arrays | Sets |
|:-|:-|
| **Ordered** list of values are needed | **Unique** values are needed |
| Data **manipulation** is needed | If **high-performance** is needed |
|  | **Removal of duplicates** is needed |

**Objects** vs **Maps**:
| Objects | Maps |
|:-|:-|
| More 'traditional' key/value store ('abused' objects) | Better performance |
| Easier to write and access values with `.` & `[]` | Keys can have any data type |
|  | Easier to iterate |
|  | Easy to compute size |

# Section 10 | A Closer Look at Functions

JavaScript does not have passing by reference, only passing by value.

# Section 14 | Object-Oriented Programming (OOP) With JavaScript

There are 2 major **paradigms** in JavaScript:
1. **Functional Programming**
2. **Object-Oriented Programming**

Object-Oriented Programming:
* **OOP** is a programming paradigm that is based on the concepts of objects.
* Objects can be used to model real-world or abstract features.
* Objects may contain data *(properties)* and code *(methods)*.
  * All the data and corresponding behavior is packed into one block.
* Objects are self-contained pieces/blocks of code.
* Objects are building blocks of apps, and interact with one another.
  * These interactions happen through a **public interface (API)**: methods that the code outside of the object can access and use to communicate with the object.
* OOP's goal is code organization, flexibility and maintainability.

A **Class** is a blueprint for objects.  
JavaScript does **NOT** support real classes.  
A class can be used to create multiple instances of objects.

4 Fundamental OOP Principles:
1. Abstraction
    * Ignoring or hiding details that don't matter.
2. Encapsulation
    * To keep some properties and methods private.
    * Some methods can be exposed which is called an **API**.
    * Prevents external code from manipulating internal state. 
    * The term **'state'** refers to an object's data.
3. Inheritance
    * Makes all properties and methods available to a child class.
4. Polymorphism
    * A child class can override a method that it inherited from a parent class.

Objects (instances) are **instantiated** from a class.  
All objects are linked to a prototype object. This is called prototypal inheritance.

**Constructor** Functions
* Can create objects from a function.  
* This is how built-in objects like Arrays, Maps or Sets are actually implemented.

**ES6 Classes**
* Modern alternative to constructor function syntax.
* Work exactly like constructor functions.
* Do **NOT** behave like classes in classical OOP.

**`Object.create()`**
* The easiest and most straightforward way of linking an object to a prototype object.

Never create a method inside a constructor function,  
because each object created will carry around that function,  
and that degrades the performance of the code.