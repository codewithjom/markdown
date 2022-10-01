# :point_right: Learn JavaScript

> (c) 2022 w3schools/sql. Use of this is to help the user whenever not online.

## Table of Contents

- [Introduction](#introduction)
  - [JavaScript Can Change HTML Content](#javascript-can-change-html-content)
  - [JavaScript Can Change HTML Styles (CSS)](#javascript-can-change-html-styles-(css))


<a id='introduction'></a>
## Introduction

<a id='javascript-can-change-html-content'></a>
### JavaScript Can Change HTML Content

One of many JavaScript HTML methods is `getElementById()`.

The example below "finds" HTML element (with id='demo'), and changes the element content (innerHTML) to 'Hello JavaScript':

**Example**

``` js
document.getElementById('demo').innerHTML = 'Hello JavaScript';
```

> JavaScript accepts both double and single quotes:

**Example**

``` js
document.getElementById("demo").innerHTML = "Hello JavaScript";
```

<a id='javascript-can-change-html-styles-(css)'></a>
### JavaScript Can Change HTML Styles (CSS)

Changing the style of an HTML element, is a variant of changing an HTML attribute:

**Example**

``` js
document.getElementById('demo').style.fontsize = '35px';
```

### JavaScript Can Hide HTML Elements

Hiding HTML elements can be done by changing the `display` style:
