# Intro to Web Development 

In this course we will learn how to build a web page from scratch!


Before we dive in, let's learn how webpages work. 

![how the web works](../images/web.png)

Let's say you want to go to youtube.com.

1. You open your browser 
1. You type in www.youtube.com into your browser and hit enter  
1. Your browser sends a request to the DNS Server, which translates `www.youtube.com` into an IP address 
1. The requests is forwarded to the IP address (the web server hosting youtube)
1. The youtube server sends a response back to your computer with everything needed to render the webpage in the browser. 


The response that is returned to your browser contains 3 types of files, generally. The main objective of this class is to learn how to create these files!

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

---


## HTML Basics

All content in an HTML file is sandwhiched in between two tags. 

**Tags begin with <> and end with </>.**

Here are some examples: 

### Header tags 

```html
<h1> This is the largest header </h1>
<h2> This is the second largest header </h2>
...  
<h6> This is the smallest header </h6>
```

* ** DO NOW**: Add a header to our website!


### Paragraph 

```html 
<p> I will type my paragraphs inside the p tags </p>
```

* ** DO NOW**: Add a paragraph to our website!

### Style

```html 
<p> <b> This is bold </b> and <i> this is italicized </i> </p>
```

* ** DO NOW**: Style some text. Bold one word, italicize another, and bold AND italicize a third word. 

### HyperLink 

```html
<a href="google.com"> Let me google that for you, buddy </a>
```
* ** DO NOW**: Add a link to your favorite website!

### Images 

```html 
<img src="images/dog.jpg" alt="If the image can't be displayed this text is shown" width="400" height="400"> 
```

* ** DO NOW**: Add this code to your website under the button to see a cute picture of a dog!

### Breaks 

```html 
<p> Here is some text followed by a break </p>
<br> 
<p> Here is more text after the break </p>
```

* ** DO NOW**: Add a break after the button and before the image so they are not displayed on the same line!

### Lists 

```html 
<p> To Do List </p>

<ul>
  <li> Learn python </li>
  <li> Learn how to put pictures of dogs on a simple website </li>
  <li> Take over the world </li> 
</ul>
```

* ** DO NOW**: Create a to-do list on your website!