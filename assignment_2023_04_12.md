### 1. Write a program that declares a variable using var, let, and const and prints the value to the console.

<br/>

```js
var x = 5
let y = 10
const z = 20

console.log(x)
console.log(y)
console.log(z)
```

### 2. Write a program that reassigns a value to a variable declared with let and prints the new value to the console.

<br/>

```js
let x = "madiha"
x = "mallick"

console.log(x)
```

### 3. Write a program that tries to reassign a value to a variable declared with const and prints the message to the console

<br/>

```js
const x = 10

try{
    x = 20
}
catch(err){
    console.log(err.message)
}

```

### 4. Write a program to declare a const, let, var variable within an if statement and try to access the variable outside the if block, what is the result?

<br/>

```js
if (true){
    let i = 10
    var j = 20
    const k = 30
}
console.log(i)
console.log(j)
console.log(k)
```

Here i and k cannot be accessed outside the if block as let and const have block access where as we can access j outside the block since it is var and var has global access.

### 5. Write a program that concatenates two or more strings and prints the result to the console.

<br/>

```js
let f_name = "madiha"
let l_name = "mallick"

console.log(`My full name is ${f_name} ${l_name}`)

```

### 6. Write a program that takes a string as input and prints the length of the string to the console.

<br/>

```js

let user_input = prompt("Please enter a string")

console.log(user_input)

```

### 7. Write a program that converts a string to uppercase and prints the result to the console.

<br/>

```js

let string = "Hello World"

console.log(string.toUpperCase())

```
