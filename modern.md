# Modernizing our website

Link: https://meet.google.com/dur-zfij-xpv

## Warmup 

* What is the difference between margin and padding? 

* What is a `<div>` and how can we style them?

* What is the difference between a class and an element selector? 

  ```css

  body {
    font-family: 'Roboto', sans-serif;
    font-weight: 100;
  }

  .container {
    padding: 10px 10px;
  }
  ```

* How do multiple selectors work? What does the following code mean? 

  ```css
  html, body {
    margin: 0;
    padding: 0;
  }
  ```

* How do descendent selectors work? 

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

## Changing the font 

We can pick from a much wider range of fonts by importing fonts into our html pages. 

1. Check out [this link](https://artisanthemes.io/best-google-fonts-combinations-modern-agency-website/) to view modern fonts 
1. Under the **embed** code section, copy and past the `<link>` on the top of each html page 
1. Copy and paste the corresponding css code into your `style.css` file 

## Making a full page jumbotron 

Lets make the entire landing page background a picture of our choice. 

** DO NOW**: 
* If you haven't already, get 4 high quality images for each of the pages on your website
* High quality free images: https://unsplash.com
* Rename each image file, and drag it into your images folder 

Now, lets edit the css. 

```css 
.jumbotron {
  background-size: cover;
  height: 100vh;
}

.jumbotron.goldengate {
  background-image: url('images/goldengate.jpg');
}
.jumbotron.italy {
  background-image: url('images/italy.jpg');
}
.jumbotron.space {
  background-image: url('images/space.jpg');
}
.jumbotron.pfieffer {
  background-image: url('images/pfieffer.jpg');
}
```

Here, we introduce the concept of **multiple classes**. 

```html 
<div class="jumbtron">
  ...
</div>
```

All divs following the above pattern will make the entire background the picture. 

Next, 

```css 
.jumbotron.goldengate {
  background-image: url('images/goldengate.jpg');
}
```

will be applied to the following divs. 

```html 
<div class="jumbtron goldengate">
  ...
</div>
```

This is an example of **inheritance**. Inheritance is a really big idea in computer science, and it has many applications. It is a good idea to use inheritance when you have multiple objects that share many similar characteristics. For example, all jumbtrons should span the entire page, but not all jumbotrons should be the same picture. 

## Making a fixed navbar 

Lets make a fixed navbar, i.e., one that stays on the top of the screen even when you scroll down. 

** DO NOW **: Take your best guess: if we want the navbar to be overlayed on the jumbotron, should we put our navbar element above, below, or inside our jumbotron element? 

---

Edit your `style.css` with the following code: 

```css 
.nav { 
  background: transparent;
  width: 100%;
  position: fixed;
}

.nav ul {
  text-align: right;
  list-style: none;
  padding: 0;
}

.nav ul li {  
  display: inline-flex; 
  padding: 0px 2% 0px;
}

.nav ul li a {  
  color: white;
  font-size: x-large;
  text-decoration: none
}

.nav ul li:hover {
  cursor: pointer; 
  font-weight: bold;  
}
```

On each page, edit your HTML to look like this: 

```html 
<div class="jumbotron pfieffer">
  <div class="nav">
    <ul>
      <li> <a href="index.html"> Home </a> </li>
      <li> <a href="about.html"> About </a> </li>
      <li> <a href="blog.html"> Blog </a>
      <li> <a href="contact.html"> Contact </a> </li>
    </ul>
  </div>
</div>
```

** DO NOW: ** Add a Title and subtitle to each page! Try and mimic the website shown to you: 

Things to consider: 
* How do we want to represent a title and a subtitle in html and css? 
* should we put our title and sub element above, below, or inside our jumbotron element? 
* how can we use padding to correctly place our element?

