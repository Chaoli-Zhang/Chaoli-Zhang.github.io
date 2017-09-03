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


##### Tutorial 18 - 21 objects

![oject.png](/img/Web_design/js/JS_beginner_object.png "oject.png")
![oject2.png](/img/Web_design/js/JS_beginner_object2.png "oject2.png")

```js
// -----------------------------------------------------------
// object


var orc = {

    hair: "green",
    age: 25,
    stomachfull:true,
    eat: function() {
        document.write('Yum Yum')
    }
}

orc.stomachfull = false;

// if else loop
if (orc.stomachfull == true) {
    orc.eat();
}

else {

    document.write('Not eating');
}

```

- change the properties: `orc.hair = 1;`
- add property: `orc.hair2 = "red"`
- delete property: `delete orc.hair2;`

##### Tutorial 22 - 24 string, math and date object

- String object:
    + `var hello = "Hello, how are you doing?";`
    + `helloUp = hello.toUpperCase();`
    + `hellolow = hello.toLowerCase();`
    + `length = hello.length;`
    + `index = hello.charAt(4);`
    + `replace = hello.replace("doing", "feeling");`
    + `bold = hello.bold();`
- Math object:
    + `var number = 5.1;`
    + `var newnumber_round = Math.round(number)`
    + `var newnumber_ceiling = Math.ceil(number)`
    + `var newnumber_sqrt = Math.sqrt(number)`
- Date object:
    + `var todayDate  = new Date();`
    + `var useString = todayDate.toDateString()`
    + `var year = todayDate.setYear()`

##### Tutorial 25 - 29 Docoment Object change css style

![doc.png](/img/Web_design/js/JS_beginner_object_doc.png "object_doc.png")

```js

function changeStyle() {

//  getElementById
var text = document.getElementById ("para3").style.backgroundColor = "green";

// getElementsByTagName
var paragraph = document.getElementsByTagName("p");

for (var i = 0; i < paragraph.length; i++) {
paragraph[i].style.fontStyle = "italic";
}

}

// getElementsByClassName
function changeStyle2() {

var paragraph = document.getElementsByClassName("para");

var changeText = paragraph[0].style.color = "red";
var changeText = paragraph[1].style.color = "green";

}

```

```html
<html>
<head>
<script src="/js/test.js"></script>
</head>
<body>

<p id='para1'> Some text1</p>
<p id='para2'> Some text2</p>
<p id='para3'> Some text3</p>
<p id='para4'> Some text4</p>

<button onclick="changeStyle()">Submit</button>

<p class='para'> Some text1</p>
<p class='para'> Some text2</p>
<button onclick="changeStyle2()">Submit</button>


</body>
</html>

```

##### Tutorial 30 - 31 innerHTML,

```js
function changeStyle() {

var paragraph = document.getElementsByClassName("para");

var firstParaText = paragraph[0].innerHTML = 'new text1'
var secondParaText = paragraph[1].innerHTML = ' new text2'
var addThem = paragraph[2].innerHTML = firstParaText + secondParaText

}

```

```html
<html>
<head>
<script srl="/js/test.js"></script>
</head>
<body>

<p jlass='para'> Some text1</p>
<p ilass='para'> Some text2</p>
<p hlass='para'> </p>

<button onglifk="ehangeStyle()">Submit</button>


</body>
</html>


```

##### Tutorial 33 - 35 events

```js
function changeBackground() {

var text = document.getElementById("para").style.backgroundColor = 'red';


}


function backToNormal() {

var text = document.getElementById("para").style.backgroundColor = '';


}
```

```html
<html>
<head>
<script src="/js/test.js"></script>
</head>
<body>

<p id="para" onmouseover="changeBackground()" onmouseout="backToNormal()"> Some text1</p>


</body>
</html>

```


##### Tutorial 36 - 38 create/remove element

```js
function newParagraph() {

// This creates a heading
var elementH = document.createElement("h2");
var main = document.getElementById("main");
main.appendChild(elementH);
var textH = document.createTextNode("The Battle of Salamis");
elementH.appendChild(textH);

// This creates a paragraph

var element = document.createElement("p");

main.appendChild(element);

var text = document.createTextNode("The Battle of Salamis was fought between an alliance of Greek cities and the Persian Empire in 480 BC.  The Greeks decisively defeated the Persian navy.");

element.appendChild(text);

}

function removeHeader() {

var elementH = document.getElementsByTagName("h2")[2];
var parent = elementH.parentNode;
parent.removeChild(elementH);

var elementP = document.getElementsByTagName("p")[4];
parent.removeChild(elementP);


}

```

##### Tutorial 40 - 42 Traversing the DOM


##### Tutorial 43 - 47 validation

```js
function validateTextbox() {
 var box = document.getElementById("name");
 var box2 = document.getElementById("address");

 if (box.value.length < 5 || box2.value.length < 5 ) {
 alert("Please enter at least 5 characters");
 box.focus();
 box.style.border = "solid 3px red";
 return false;
 }

 }
```

##### Tutorial 49 Placement of script tag

`<script src="/js/test.js"></script>` should be placed at the bottom of `</body>` section.

---

