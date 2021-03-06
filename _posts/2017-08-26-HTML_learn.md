---
layout:     post                                    # 使用的布局（不需要改）
title:      HTML        # 标题
subtitle:   HTML learning from EJ            #副标题
date:       2017-08-27                              # 时间
author:     Chaoli Zhang                            # 作者
header-img: img/Tag-bg-hacker.jpg                  #这篇文章标题背景图片
catalog: true                                       # 是否归档
tags:                                               #标签
    - Learning
    - HTML
---


### HTML
A short introductory course on HTML by EJ, videos can be found here: [HTML Introductory Course](https://www.youtube.com/playlist?list=PLr6-GrHUlVf_ZNmuQSXdS197Oyr1L9sPB)

##### Tutorial 0

- `<>` is a tag
- `<body> something </body>` is a mark up element
- `<br>` is a line break, empty element

##### Tutorial 1

 ``` html
<!DOCTYPE html>
<html>
<head>
    <title> My webpage </title>
</head>

<body>
<h1> The fish website </h1>

<p> Welcome to the website </p>

<h2> This is subsection of Bass fish </h2>

<p> Bass fish is yummy </p>

</body>
</html>
 ```
##### Tutorial 2
- Add line breaks, spacing and comments
    1. line break `<br>`
    2. comment `<!-- This is the comments -->`
    3. spaces `&nbsp`

 ``` html
<!DOCTYPE html>
<html>
<head>
    <title> My webpage </title>
</head>

<body>

<h1> The fish website </h1>

<p> Welcome to the website </p>

Space in &nbsp between

<br>
<br>
<!-- This is the comments -->
<h2> This is subsection of Bass fish </h2>

<p> Bass fish is yummy </p>

</body>
</html>
 ```

##### Tutorial 3
- ordered and unordered lists
    1. unordered: `ul` i.e. items
    2. ordered: `ol` i.e. enumerate
    3. list item: `li`

```html
<!DOCTYPE html>
<html>
<head>
    <title></title>
</head>
<body>

<ul>
    <li>CD</li>
    <li>DVD</li>
</ul>

<ol>
    <li>CD</li>
    <li>DVD</li>
</ol>

</body>
</html>
```

##### Tutorial 4
- create a table
    1. table: `<table>`
    2. row: `<tr>`
    3. data: `<td>`
    4. column: `<th>`

```html
<!DOCTYPE html>
<html>
<head>
    <title></title>
</head>
<body>

<table>
    <tr>
        <th> Anna </th>
        <th> Jack </th>
        <th> David </th>
    </tr>
    <tr>
        <td> 25 </td>
        <td> 28 </td>
        <td> 24 </td>
    </tr>

</table>


</body>
</html>
```

##### Tutorial 5 - 6
- add a web link
    1. external: `<a href="chaolizhang.org"> My homepage</a>`
    2. internal (jump): `<a href="#Fish">Fish section</a>`


```html
<!DOCTYPE html>
<html>
<head>
    <title></title>
</head>
<body>

<ul>
    <li><a href="#Birds">Bird section</a></li>
    <li><a href="#Fish">Fish section</a></li>
</ul>

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

<a name="Birds"> THis is the article about birds. </a>
</body>
</html>
```

##### Tutorial 7 - 8
- add image
    1. include image: `<img src="Image.jpg">`
    2. change the size: `<img src="Image.jpg" width="200" height="200">`

```html
<!DOCTYPE html>
<html>
<head>
    <title></title>
</head>
<body>
<h1> Shanghai </h1>
<p> <img src="Image.jpg" width="200" height="200"></p>
</body>
</html>
```


##### Tutorial 10 - 18 Forms
- one line text box
    1. box: `<input type="text" name="">`
    1. add label to text box: `<label for='firstname'> first name</label>`
    1. change size: `<input type="text" id="firstname" name="" size="80">`
    1. multiple text box: `<textarea rows="10" cols="40"></textarea>`
    1. submit bottom: `<input type="submit" value="Submit">`
    1. radio bottom: `<input type="radio" name="yesorno" value="">`
    1. check box: `<input type="checkbox" name=""> A`
    1. number input: `<input type="number"> `
    1. drop down list `<option value='Shanghai'> Shanghai </option>`



```html
<!DOCTYPE html>
<html>
<head>
    <title></title>
</head>
<body>
<form>
    <label for='firstname'> First name: </label>
    <input type="text" id="firstname" name="" size="20">
    <label for='secondname'> Surname name: </label>
    <input type="text" id="secondname" name="" size="20">
</form>

<form>
    Comments <br>
    <textarea rows="10" cols="40"></textarea> <br>
    <input type="submit" value="Submit">
</form>

<form>
    radio bottom <br>
    Yes:
    <input type="radio" name="yesorno" value=""> <br>
    No:
    <input type="radio" name="yesorno" value=""> <br>
</form>


<form>
    check box <br>
    <input type="checkbox" name=""> A <br>
    <input type="checkbox" name=""> B <br>
    <input type="checkbox" name=""> C <br>
    <input type="checkbox" name=""> D <br>
</form>

<form>
    number input <br>
    <input type="number" min=0 max=30>
</form>


<form>
<select>
    dropdown list <br>
    <option value='Shanghai'> Shanghai </option>
    <option value='Beijing'> Beijing </option>
    <option value='Wenzhou'> Wenzhou </option>
</select>
</form>

<!-- Input date and days -->
<form>
  Enter day you want to travel to Cancun:
  <input type="date" name="day">
  Number of days: <input type="number" name="numdays" min="1" max="10">
</form>


</body>
</html>
```

##### Tutorial 19 - Attribute
Attribute

- `<p class="test"></p>`
- `<label for='name'></label>`


##### Tutorial 20 - Meta element
Meta element shows the information when you google searched it
**Number limits: 140 characters**

- name="discription"
- name="keywords": no longer used on Google
- http-equiv="author"
- http-equiv="content-language"

`<meta name="discription"content"fish, ocean, aqaurium" charset="utf-8">`

##### Tutorial 21 - Escape characters

- space:`&nbsp`
- . > :`&gt`
- < :`&lt`
- ? :`&#63`

##### Tutorial 22 - Bold, strong, italic and em

- Bold: <b> Bold element</b> `<b> Bold element</b>`
- Strong: <strong>Strong element</strong> `<strong>Strong element</strong>`
- Italic: <i>italic element</i> `<i>italic element</i>`
- em: <em>em element</em> `<em>em element</em>`

##### Tutorial 23 - iframe element

```html
<iframe frameborder='1' width="500" height="500" src="1st.html" name="1st" id="1st" ></iframe>

<a href="second.html" target="1st">Switch to new documents</a>

```

<iframe frameborder='1' width="500" height="500" src="1st.html" name="1st" id="1st" ></iframe>

<a href="second.html" target="1st">Switch to new documents</a>

##### Tutorial 24 - sup and sub elements

- sup: 23<sup>rd</sup> `23<sup>rd</sup>`
- sub: H<sub>2</sub>O `H<sub>2</sub>O`

##### Tutorial 25 - title and alt attributes

- title: text shown when you move your curse to the image
- alt: when your image can not be shown for some reason, then a text in alt is shown instead.

<img src="/img/Tag-bg-hacker.jpg?raw=true" title="title" alt="Hackerimage">

##### Tutorial 26 -29 - audio/videos element

- add audio: mp3
    + `<audio controls autoplay>`
    + `<audio controls autoplay loop>`
    + `<audio controls autoplay draggable="true">`
- add video: mp4

```html
<audio controls="audiocontrols">
    <source src="some.mp3" type="">
</audio>

<video width="500" height="360" controls>
    <source src="some.mp4" type="">
</video>
```

<audio controls="audiocontrols">
    <source src="some.mp3" type="">
</audio>

<video width="500" height="360" controls>
    <source src="some.mp4" type="">
</video>


This completes the whole series. Awesome work!





