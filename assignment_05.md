
## 1. What is an IIFE (Immediately Invoked Function Expression) and why would you use it in JavaScript? Give an example of IIFE.

### Answer:

An IIFE is a JavaScript function that runs as soon as it is defined.

```js
(function () {
    console.log("Hello World!")
})();
```

## 2. What is the purpose of using the bind() method in JavaScript and how is it different from call() and apply()?

### Answer:

The bind() method creates a new function that, when called, has its this keyword set to the provided value, with a given sequence of arguments preceding any provided when the new function is called.

```js
const person = {
    name: "Madiha",
    age: 20
}

function printPerson() {
    console.log(this.name + " is " + this.age + " years old.")
}

const printPersonBind = printPerson.bind(person)

printPersonBind()
```
 
 Output: Madiha is 20 years old.

 ## 3. What is a Higher-Order Function (HOF) in JavaScript and how is it different from regular functions? Explain with an example.

### Answer:

A higher-order function is a function that can take another function as an argument, or that returns a function as a result.

```js
function add(x, y) {
    return x + y
}

function subtract(x, y) {
    return x - y
}

function multiply(x, y) {
    return x * y
}

function divide(x, y) {
    return x / y
}

function calculator(x, y, operator) {
    return operator(x, y)
}

console.log(calculator(10, 5, add))
console.log(calculator(10, 5, subtract))
console.log(calculator(10, 5, multiply))
console.log(calculator(10, 5, divide))
```

Output: 15, 5, 50, 2


## 4. Write a function called multiplyBy that takes a number as input and returns a new function that multiplies any number passed into it by the original number.

### Answer:

```js
function multiplyBy(x) {
    return function(y) {
        return x * y
    }
}

const multiplyByTwo = multiplyBy(2)

console.log(multiplyByTwo(5))

const multiplyByThree = multiplyBy(3)

console.log(multiplyByThree(5))
```

Output: 10, 15

## 5.Write a function named sortArray that takes in two parameters:

    An array of numbers

    A boolean value ascending that indicates whether the array should be sorted in ascending or descending order.

    The sortArray function should return the sorted array. Use an anonymous function to do the actual sorting, rather than using the built-in sort method.

### Answer:

```js
function sortArray(arr, ascending) {
    return arr.sort(function(a, b) {
        if (ascending) {
            return a - b
        }
        else {
            return b - a
        }
    })
}

console.log(sortArray([1, 2, 3, 4, 5], true))

console.log(sortArray([1, 2, 3, 4, 5], false))
```

Output: [1, 2, 3, 4, 5], [5, 4, 3, 2, 1]

