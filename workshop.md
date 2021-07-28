# Filling out our website 

Link: https://meet.google.com/dur-zfij-xpv

In today's lesson, you will be implementing most of the code yourself. Try to use what you have learned about HTML and CSS to create content for your website!

Remember, you can always use the code in this REPL as a guide, but try not to just blindly copy and paste! 

## Titles and Subtitles 

Add a title and a subtitle to each of your pages. They should be overlayed on the jumbotron and styled. 

>Hint 1: Think about where the title and subtitle should be placed. Should the div be above, below, or inside the jumbtron? What should the classes be called

>Hint 2: What kind of padding should the title and subtitle have? Should you add margin?


## Content

Create a section on each page where the main content will go. 

>Hint 1: The "main" content of each page should be at the same level of nesting as the jumbotron and the footer. 

>Hint 2: What kind of padding do you need?

>Hint 3: Make sure you can see the text!



## Blog Posts

Create a skeleton for blog posts.  

> Hint 1: Your blog posts should be in the main section 

> Hint 2: Your blog posts can be represented as a `.blog-item`

> Hint 3: Each blog item will probably contain the same sub elements that should be specifically styled:
  * `<img>`
  * `<h2>`
  * `<p>`
  * `<a>`


If you want to create a 2-column blog post structure, you may need to add this to your css.


```css
.main::after {
  content: "";
  display: table;
  clear: both;
}
```

(Replace .main with whatever class you gave to your main content `<div>`)

