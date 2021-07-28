# CSS

Link: https://meet.google.com/dur-zfij-xpv

## Warmup

If you haven't already, 

1. Create the following files in your project directory: 
    * `about.html` 
    * `blog.html`   
    * `contact.html`

1. Create a bulleted list of links at the top of each page that you just created
    * Home 
    * About 
    * Blog 
    * Contact 

1. Add the following text in a `<p>` tag to each page:

  > This website was made by {your name}. The source code can be found [here](https://github.com)


## CSS Basics 

You can add CSS to an HTML element in 3 ways: 

1. In-line 

  ```html
  <p style="color: red; text-align: center;"> Yo what is up look at my red text </p>
  ```

Here is a link for styling text: https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals

**DO NOW**: Edit a paragraph in your website with some inline style. 

2. In a `<style>` tag 

  ```html
  <html>
    <head>
      <style>
        h1 {color:red;}
        p {color:blue;}
      </style>
    </head>
    <body>

      <h1>A heading</h1>
      <p>A paragraph.</p>

    </body>
  </html> 
  ```

**DO NOW**: Edit a the `index.html` in your website to include a style block. 

3. In the `style.css` file 

  ```css
    html, body {
    margin: 0;
    padding: 0;
    }

    body {
      font-family: 'Roboto', sans-serif;
      font-weight: 100;
    }

    .container {
      margin: 0 auto;
      max-width: 940px; 
      padding: 0 10px;
    }

    .header {
      background: url(https://content.codecademy.com/projects/innovation-cloud/bg.jpg) no-repeat center center; 
      background-size: cover;
      height: 800px;
      text-align: center; 
    }

    .header .container {
      position: relative;
      top: 200px;
    }

    .header h1 {
      color: #fff;
      line-height: 100px; 
      font-size: 80px;
      margin-top: 0;
      margin-bottom: 80px;
      text-transform: uppercase; 
    }
  ```

The best practice is option #3. This makes it easier to read html files, and allows for maximum re-usability of our custom styles. 

## CSS Terminology 

![CSS](../images/CSS.png)

1. The **Selector** is the first part of a CSS ruleset. This targets the HTML element that will be styled. 
1. The **Declaration Block** is everything inside the two brackets {}. There can be multiple declarations inside a declaration block
1. A **Declaration** is a `property-value` pair that will apply to the _selected_ element. 
1. The **Property** is the first part of each declaration. It describes the visual characteristic of the element to be modified. 
1. The **Value** is the second part of each declaration. It describes what the property of the element should look like. 

## HTML Div tags 

The `<div>` tag is the most common way web designers _divide_ their HTML elements. We can give each div a different **class**, and style the classes accordingly. 


### Creating a Navbar 

** DO NOW **: On every page, edit the list of links so it looks like this 

```html 
<div class="nav">
  <div class="container">
    <ul>
        <li> <a href="index.html"> Home </a> </li>
        <li> <a href="about.html"> About </a> </li>
        <li> <a href="blog.html"> Blog </a>
        <li> <a href="contact.html"> Contact </a> </li>
      </ul>
  </div>
</div>
```

---

Now, add the following code to your css file, and hit run. 

```css

html, body {
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Roboto', sans-serif;
  font-weight: 100;
}

.container {
  padding: 10px 10px;
}

.nav { 
  background: #000;
  width: 100%;
}

.nav ul {
  list-style: none;
  padding: 0;
}

.nav ul li {
  color: red;
  display: inline-block; 
  list-style: none;
  padding: 10px 10px;
}

.nav ul li:hover {
  background: #117bff;
  cursor: pointer; 
  transition: background .5s;  
}

```

## What's going on? 

Lets take a deeper look at the CSS we added to the style sheet.  

#### Multiple selectors

```css
html, body {
  margin: 0;
  padding: 0;
}
```

In the above block, you see two selectors, separated by a comma. 

This means that the block applies to all content inside **BOTH** `html` **AND** `body` tags. 

---

#### Class vs Element selectors

```css

body {
  font-family: 'Roboto', sans-serif;
  font-weight: 100;
}

.container {
  padding: 10px 10px;
}
```

You might notice that `body` has no period in front of it while `.container` does. 

* No period in front of selector means it is an **element selector**. 

* The period in front of the selector means it is a **class selector**. 

So, 

```css

body {
  font-family: 'Roboto', sans-serif;
  font-weight: 100;
}
```

Applies to all the content inside the body element

```html 
<body>
  ...
</body>
```

While 

```css
.container {
  padding: 10px 10px;
}
```

Applies to all content in between this container div. 

```html 
<div class="container">
  ...
</div>
```

---

#### Margin and Padding 

You might be wondering, _what the heck is margin and padding?_

![Margin](../images/margin.png)

As you can see when you create an html element, the stuff inside the tags is called the **content**. 

* **Padding** is the area (typically measured in pixels) outside the content but _within_ the element. 

* **Margin** is the area (also measured in pixels) _outside_ the element

You can customize the margin and padding on the **top**, **bottom**, **left**, and **right** of an HTML element. You can do this 2 ways: 

```css
.container {
  padding-top: 10px;
  padding-right: 8px;
  padding-bottom: 6px;
  padding-left: 5px;
}
```

OR you can right it **shorthand** 

```css
.container {
  padding: 10px 8px 6px 5px;
}
```

_If you are writing your margin and padding shorthand..._


1. And you only provide 3 values, the `top` margin is given the first value, the `left` and `right` margins are given the second value, and the `bottom` margin is given the third value. 

1. And you only provide 2 values, the `top` and `bottom` margins are given the first value, and the `right` and `left` magins are given the second value. 

1. And you only provide 1 value, `top`, `bottom`, `right`, and `left` margins are all given the same value. 

**DO NOW**: Interpret the following declaration blocks: 

```css

.header {
  padding: 10px 10px;
  margin: 5px
}

.footer { 
  padding: 5px 10px 10px;
  margin: 0px 15px;
}

.main {
  padding: 20px;
  margin: 0px;
}
```

You can edit the margin in the same way that you edit the padding.  


**DO NOW**: Play with the margin and padding for the `container` declaration. 

---

#### Descendent selectors 

```css

.nav { 
  background: #000;
  width: 100%;
}

.nav ul {
  list-style: none;
  padding: 0;
}

.nav ul li {
  color: red;
  display: inline-block; 
  list-style: none;
  padding: 10px 10px;
}

```

If you add a space between two selectors in the same declaration block, you will create a descendant selector. 

This means that the style will be applied to elements that are _children_ of the element on the left. 

So, the first block applies to 

```html 
<div class="nav">
  ...
<div>
```

The second block only applies to 

```html 
<div class="nav">
  <ul>
    ...
  </ul>
<div>
```

And the third block applies to 

```html 
<div class="nav">
  <ul>
    <li>...</li>
    <li>...</li>
    <li>...</li>
    <li>...</li>
  </ul>
<div>
```

** DO NOW:** Play around with the declarations in your descendant selectors to see how your navbar is edited!

---

### Creating a Footer 

** DO NOW **: On every page, edit the bottom paragraph so it looks like this: 

```html 
    <div class="footer">
      <div class="container">
        <p>This website was made by {your name}. The source code can be found here</p>
      </div>
    </div>
```


Add the following CSS to your file, one declaration block at a time:

```css
.footer { 
  background: #000;
  height: 80px; 
  padding-bottom: 50px;
}

.footer p { 
  color: #fff;
  font-size: 14px;  
  height: 80px; 
  line-height: 80px;
  margin: 0;  
}
```

### Creating a Jumbotron
First add the following HTML 

```html 
    <div class="jumbotron">
        <div class="container">
          <h2>Stay Connected</h2>
        </div>
    </div>  
```

Then add the following CSS, one at a time

```css
.jumbotron {
  background: url(https://content.codecademy.com/projects/innovation-cloud/jumbotron_bg.jpg) center center;
  background-size: cover;
  height: 600px; 
}

.jumbotron .container {
  position: relative;
  top: 220px;
}
```