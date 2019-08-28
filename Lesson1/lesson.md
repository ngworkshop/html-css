author: Lorenzo Franceschini
summary: CodeLabs teaching HTML - CSS - Lesson 1
id: html-css-1
categories: html, css, web
environments: Web
status: Draft

# Introduction to HTML and CSS

## HTML, DOM and the Browser
Duration: 0:20:00

### Warm up

All of us already know what is a web page and which technology are involved.
At this point of our study-path, we know that a web page is created by using HTML, CSS and JavaScript.

Let's start refreshing some ideas behind HTML and how our Browser works behind the scene.

HTML defines the structure of a web page using several semantic elements that define the purpose of texts, images and others resources within page. This brings us the principle of SoC (Separation of Concerns) where every techonoly is used for a spefic purpose:
- HTML: Semantic Structure of the Content
- CSS: Presentation of the Content
- JavaScript: Behaviour of the Elements

Thanks to SoC we can have advantages like: scalable website (or application), more readable and mantainable software, etc... . 

### The Structure

HTML stand for HyperText Markup Language built as a language for the World Wide Web and use by the browser to interpret and show to us, text, images and link to other documents.

An HTML page is a file with the ".html" extension. Inside we can write HTML tag elements to define the structure and the content of the page:

```html
<element-name attr=value>content</element-name>
```

A HTML tag element is identified by a couple of tags (opening tag and closing tag) in the source code with a string within angle brackets and some key-value pairs that define the element attributes. An **attribute** is an additional information of the HTML element, such as the CSS Class, the ID for identification or attributes for sizing and value. Some of those attributes are shared by all the elements, others are specified to only a few set of tag elements.
[Here](https://html.com/attributes/) you can find a complete list of HTML tag attributes.

The web page is a parent-child relationship tree. With the html tag as the root element, divided by head and body section.
The head section contains only meta data and link to other resource like stylesheet (CSS) and script (JavaScript). This section is ignored by the rendering process, so no tag element inside head will be visible to our device.
The body section contains all the visible parts of our web page.

![](./assets/dom-tree.png)

![](./assets/web-structure.gif)

An element that is directly contained by another element is said to be the **child** of that element, and this is the **parent**. Elements that have the same parent are called **siblings**. All the elements within a given element are called **descendats**. A child is just a special kind of descendats, it's relative of the context. To be considered as a child, an elements needs to be directly under its parent element in the structure.
Understand the structure and the relationship between elements is crucial to understand how CSS works.

Try to find the errors:

```
<!DOCTYPE html>
<html lang="en">
	<body>
		</header>
			<h1>My Portfolio Web Page</h1>
			<p>A simple show gallery of my projects</p>
		</header>
		<section>
			<a href='#' alt='first-project'><h6>More info...</h6></a>
			<p>In this project called <b>The One, I encountered different problems, like:
			<ul></p>
				<li>...</li>
				<li>...</li>
				</ul>
			</ul>
		</section>
		<div>
			<aside>
				<!-- To-Do: .... -->
			</aside>
			<aside>
				<!-- To-Do: .... -->
			</aside>
		<div>
	</body>
</html>
```

You need to know that HTML is not so observant to the rules, and some errors can be tolerated by the HTML, like to omit the closing p tag, or omit html tag. I always reccomend to keep consistency and clarity when you write your code.

### The Browser

The main goal of every browser is to present on a device the resource you have request to a server. Tipically you request a web page from a web server. A browser, thanks to its rendering engine, can be show a lot of different kind of resources like: PDF, Images, Video or... an HTML Page.
When your browser start to read and parse an HTML page, it construct an in-memory structure called **DOM**, it acts like a tree.
Every HTML elements will be inside this structure and it can be thought like an object called **Node Element**, and the attributes of the HTML element will be the initial value of this node, called them **Property**. Then we have another tree called Render Tree, that contains styling information together with visual rules. Every leaf of this tree is a rectangle with visual attributes. The browser start as soon as possible to display the contents on the user device in the "layout-process" step.

### How we write HTML Code

We can write HTML in every editor on our computer or with a lot of online tools to make some test/mock and experiment for our studies.



## HTML Tag Elements
Duration: 0:15:00

### The source code in HTML

When we writing HTML source code, we define a set of HTML Elements by using TAG ELEMENT.

The most common tag elements are: 

```
<html></html>
<title></title>
<head></head>
<body></body>
<div></div>
<h1></h1>
<h2></h2>
...
<h6></h6>
<p></p>
<a></a>
<img>
<b></b>
<i></i>
<strong></strong>
<em></em>
```

Probably you are familiar to this rules:

- not every HTML tags needs to be closed, some tags are self closing;
- some HTML tags needs to be unique like html, title, head and body;
- some HTML tags can have the same visual effect like b and strong but have different results for SEO;
- some HTML tags are mandatory like: !DOCTYPE, html and title. Those are the minimun tags to have a valid HTML page;
- certain tags can be omitted like html, head and body [LINK](https://html.spec.whatwg.org/multipage/syntax.html#syntax-tag-omission);
- every HTML tags can be enanched with **Attributes**, like a unique identifier with **id** attribute;
- avoid break your text with br, instead use the p tag;
- we can add metadata to enhance search engine optimization, browser compatibilty and reach better performance in some devices;
- to organize better your page section, header, nav, article, footer with div, ul/ol and span are your best friend;
- not every mistakes are browser-breaking mistakes but they produce bad design and poor SEO performance.

One of the main purpose of HTML is to diplay text, images and link to other documents. The way to do it, is by using two tag elements: img and a (anchor tag):

```html
<p><span class="fa fa-heart"></span>Lorem Ipsum dolor sit amet, consectetur adipiscing elit. Phasellus pretium sodales urna, non mattis turpis tincidunt sit amet. Sed vel vulputate lacus. Donec sed ornare mauri...</p>
<img src='assets/my_logo' alt='brand-logo' width='64px' height='64px'>
<a href='about.html' target='_self'>About Us</a>
```

### Span

The span element is a generic inline element used most of times to add icons to our text or for grouping and applying styles to inline elements.

### Paragraph
### Heading
### Div
### Image
### Anchor
### List
### Preformatted Text
### Blockquote
### Organize Content: Article, Section, Aside, Div, Header, Footer, Nav
### Data: Form, Label, Input, Button, Select, Radio and checkbox
### Tables

## HTML Validation
Duration: 0:10:00

### Challenge

Positive
: Try to validate your HTML code by click [HERE](https://validator.w3.org/nu/#textarea):

Can you find the most minimum HTML valid code?

Let's define the basic structure:

```html
<!DOCTYPE html>
<html>
<head></head>
<body></body>
</html>
```

Now try to validate it. What's wrong with this code? Try to fix it, then try to find the most minimum code to get a green checking message.

## (HTML) Attributes vs. (DOM) Properties
Duration: 0:10:00

It's important to understand that the relationship between attributes and properties are not one-to-one relationship. Some HTML attributes don't have corresponding properties, like "colspan" and some DOM properties don't have corresponding HTML attributes like "textContent".

Positive
: Attributes are defined by HTML. Properties are defined by the DOM (Document Object Model). Attributes initialize DOM properties and then they are done. Property values can change; attribute values can't. The HTML attribute and the DOM property are not the same thing, even when they have the same name.

### Challenge

Positive
: Try to create an input element with some attributes (use at least id) and use the console.dir with document.getElementById to display all node's properties. If you want, try to add a value attribute and use document.getElementById and getAttribute to take the current value and the initial value.:

## Box Model

## Inline Vs Block Elements
Duration: 0:10:00

Every HTML Element is displayed as Inline or as Block, so the first rule to remember is: "never put a block element inside an inline element"

## CSS