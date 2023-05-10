
## 1. If we execute this Javascript, what will the browser's console show?

```js
    var text = 'outside';
    function logIt(){
        console.log(text);
        var text = 'inside';

    };

    logIt();
```


### Answer:

The console will show undefined. This is because the variable text is hoisted to the top of the function and is declared but not initialized. So when the console.log() is called, the variable text is undefined.

<br/>

## 2. Write a regular expression to reverse the first and last name

### Answer:

```js
    let name = "Madiha Mallick"
    let reverse_name = name.replace(/(\w+)\s(\w+)/, '$2 $1')
    console.log(reverse_name)
```

output: Mallick Madiha

<br/>

## 3. Write a Regular expression to validate email address

```js
    let email = "madiha.mallick@kreeti.com"
    let email_regex = /^([a-zA-Z0-9\.-]+)@([a-zA-Z0-9-]+).([a-z]{2,8})(.[a-z]{2,8})?$/
    console.log(email_regex.test(email))
```

output: true

<br/>

## 4. what will be the output?

```js
var x = 100;
console.log(x);

function test(){
  var x = 250;
  console.log(x);

  if (x > 100) {
    let x = 350;
    console.log(x);
  }

  console.log(x);
}

test();
console.log(x);
```

### Answer:

output: 100, 250, 350, 250, 100

<br/>

## 5. What is the difference of output between these two expressions? Give your reasons for it:

```js
a. 12 == “12”

b. 12 === “12”

c. Number(12) === 12
```

### Answer:

a. true

b. false

c. true


In the first case, the == operator does type coercion and converts the string to a number and then compares the values. In the second case, the === operator does not do type coercion and hence the comparison fails.


<br/>

## 6. What is NaN?

### Answer:

NaN stands for Not a Number. It is a property of the global object. In other words, it is a variable in global scope. The initial value of NaN is Not-A-Number — the same as the value of Number.NaN. In modern browsers, NaN is a non-configurable, non-writable property. Even when this is not the case, we avoid overriding it.

<br/>