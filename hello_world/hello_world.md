# Lesson 1: Intro to Web Development 

In this course we will learn how to build a web page from scratch!

## 3 Languages 
* HTML (HyperText Markup Language)
* CSS (Cascading Style Sheets)
* Javascript 

## HTML 

HyperText Markup Language (HTML) is the standard formatting language for web pages. 

** DO NOW: **

* Copy and paste the following code into `index.html`, indented in between the `<body>` and `</body>` tags.
* Refresh the web page on the top right of your screen.

```html 
<p> 
  Hello this is what a paragraph looks like in HTML 
</p>
```

## CSS 

Cascading Style Sheets (CSS) allow us to style our HTML. 

HTML and CSS work together in our browser to display stylized web pages. 

** DO NOW: **

* Copy and paste the following code into `style.css`
* Refresh the web page on the top right of your screen.

```css
body {
  background-color: lightblue;
}

p {
  font-family: verdana;
  font-size: 20px;
}
```

## Javascript 

Javascript is the programming language of the web! We can add Javascript scripts to an HTML file to make our webpages *interactive*! 

** DO NOW: ** 
* Copy and paste the HTML into `index.html`, underneath the previous `<p>` tag.
* Copy and paste the javascript into `script.js`
* Refresh the web page on the top right of your screen.
* Click the button and see what happens!

HTML: 
```html 
<p id='demo'> This is a javascript demo </p>
<button onclick="changeDemoText()"> Click Me to run a javascript function! </button>
```

Javascript:

```javascript
// change the html element with id "demo" 
function changeDemoText() {
  document.getElementById("demo").innerHTML = "Wow look how cool javascript is";
}
```

## Basics 

### HTML Tags 

All content in an HTML file is sandwhiched in between two tags. 

