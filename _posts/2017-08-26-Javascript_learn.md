---
layout:     post                                    # 使用的布局（不需要改）
title:      Website develop (Javascript)        # 标题
subtitle:   Javascript learning from EJ            #副标题
date:       2017-08-27                              # 时间
author:     Chaoli Zhang                            # 作者
header-img: img/Tag-bg-hacker.jpg                  #这篇文章标题背景图片
catalog: true                                       # 是否归档
tags:                                               #标签
    - Learning
    - Javascript
---


### Javascript
    A short introductory course on Javascript by EJ, videos can be found here: [Javascript Introductory Course](https://www.youtube.com/playlist?list=PLr6-GrHUlVf96NLj3PQq-tmEB6woZjwEl)

##### Tutorial 0 - 2 Introduction

```html
<html>
<head>
<script>
document.write ("Hello")


</script>
</head>
<body>

</body>
</html>
```

##### Tutorial 3 - 4 variable

- `var years = 35`

##### Tutorial 5 external file

- `<script src="/js/test.js"></script>`

##### Tutorial 6-7 functions

```js
function addSomething (num, str) {
    // statement

var add = num + str

alert (add)

}

addSomething(48, " cool")

```

##### Tutorial 8 operator

- num1 += num2 is the same as num1 = num1+num2
- num1++: num1 plus one

```js
// -----------------------------------------------------------
// Arithemetic and assignment operator Tutorial 8 operator

var num1 = 7
var num2 = 4

var number1 = num1 + num2

document.write (number1);

```


##### Tutorial 9 - 12 conditionals and loops

- if loop
- if ... else loop
- if ... else if ... else loop

```js
// -----------------------------------------------------------
// Conditionals loop
var food = "Apple";

// if
if (food == "Apple") {

    // alert ("Conditionals true")
}

// if else loop
if (food == "Apple") {
    // alert ("Apple is true")
}
else  {
    // alert ("Apple is false")
}

// while loop

var i = 1;
while (i<5) {
    document.write("whole"+" loop"+i)
    i += 1
}

// for loop
for (var i = 1; i < 6; i++) {
    document.write("For"+" loop")
}

```


##### Tutorial 13 - 14 function and if, and return statement


```js
// -----------------------------------------------------------
// Function and if statement

function batting(player, distance) {

    if (distance <= 300) {
        document.write(player + " is cool")
    }
    else {
        document.write(player + " is NOT cool")
    }
}

batting('Jack', 240)
batting('Jack', 444)

// return statement

function add(x,y) {

    result = x + y
    return result

}

var theResult = add(9,12)

document.write(theResult)
```


##### Tutorial 16 - 17 pass by value, array

- func(1,b): where 1 and b are pass by values
- `var roads = ["1","2","3","4"]`
- The index is the same as Python i.e. roads[1] will print out 2
- Change array element: `roads[1] = "Dirt"`


##### Tutorial 18 objects













---

<html>
<head>
<script src="/js/test.js"></script>
</head>
<body>

</body>
</html>
