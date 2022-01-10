# Intoductory HTML and JavaScript

## Introduction

- Today it is very easy to hop on your favorit internet browser and search for any website or web page you want, and within seconds it is there.
  - Behind the scenes however there are multiple steps that occur before you see this website on your browser.
    - After connecting to the web using you Internet Service Provider (ISP), you type in your website and you first contact the Domain Name System(DNS) servers.
    - From there, the DNS contacts a web server that owns the website you are looking for.
    - Then, that web server provides the web page to your browser.
  - What makes this even greater is that these steps happen on a geographical level on a global scale!

## Structure

- To define the structure of text on a web page, software developers use HTML
- Within HTML there are multiple **elements** used to determine what structure the text will have. 
- Here is a basic HTML layout for a simple web page using some core elements
```
<html>
	<body>
		<h1>This is the Main Heading</h1>
		<p>This text might be an introduction to the rest of the page. And if the page is a 
			 long one it might be split up into several sub-headings.<p>
		<h2>This is a Sub-Heading</h2>
		<p>Many long articles have sub-headings so to help you follow the structure of what 
			 is being written. There may even be sub-sub-headings (or lower-level headings).
			 </p>
		<h2>Another Sub-Heading</h2>
		<p>Here you can see another sub-heading.</p>
	</body>
</html>

```
Duckett, John. *HTML & CSS: Design and Build Websites.* John Wiley and Sons, 2014. 

- Notice how each element needs to have an opening tag and a closing tag using `<>` and `</>`
- Elements can also contain an attribute within them
  - These attributes must have a **name** and a **value** associated with them and the syntax would apear as so:
  ```
  <p lang="en-us">Paragraph in English</p>
  ```
Duckett, John. HTML &amp; CSS: Design and Build Websites. John Wiley and Sons, 2014. 

## Extra Markup

### Versions of HTML

- Along the way there have been many different versions and updates to HTML.
- This is because dynamics of websites change and programmers are hard wired to be looking for new ways to make things easier.
- The newest version of HTML is called HTML5 and within this syntax there have been changes to make things quicker.
  - In the past what would have taken 3 steps or 3 lines of code using 3 different elements embedded in other elements now takes fewer steps using less elements. 
- Since there are still multiple versions of HTML you can use based on how dated the web browser is, you must start your HTML coding by putting a **Doctype** on the first line.
  - For example, for HTML5 you would specify its Doctype by using `<!DOCTYPE html>`

### Inside HTML

- The more content on the web page the more lines of code you will have. 
- To help organize yourself and quickly reference what the code is doing you can use comments in your code with this syntax:
  - `<!-- comment goes here -->`
- To also make your life easier you can add `id` and `class` attributes.
  - Say you have multiple `<p>` tags but only want to make one specific tag a difference color or style is CSS, you would have to give it an `id` attribute.
  - For example:
``` 
<p id="mainParagraph"> This is the main paragraph </p>
```
  - You can also use the `class` attribute in a similar way to give more than one specific paragraph a certain CSS element.

```
<p class="important"> I want a couple paragraphs with certain styles </p>
```

- You can also use `<div></div>` tags to group a set of elements together in one block.
  - It is important you then give that `<div>` element an `id` attribute in order to style it in CSS.
- Lastly there is the `<meta>` element. 
    - This is an element that goes in the `<head>` section and explains the data within the data.
    - It is also an empty element so it does not need a closing tag.
    - It can have a `name` *attribute*, followed by a *value* of `description`, `keywords`, or `robots`.
    - It can also have a `http-equiv` *attribute*, followed by a *value* of `author`, `pragma`, or `expires`.
    - There are also many more *attributes* and *values* for the `<meta>` elements.
      - Common one is `<meta charset="UTF-8">`

## HTML5 Layout

- With HTML we now have elements like `<header>`, `<footer>`, `<nav>`, `<article>`, `<aside>`, and many more.
- These elements make it simpler to structure the web page and can contain `<div>` tags as well. 
- It will make it cleaner to look at and easier for the user to navigate.

## Process & Design

- If you are looking to make a website for consumers you would first need to start with a solid process and design.
- You should first determine your target market.
  - Think who is your target audience.
  - Why are they coming to your site.
  - What are they looking to get from your site.
  - When will they return back to your website.

- You will next want to create a **site map** which will show where each link will take you, what is within that link, and ultimately how to navigate the site.
- Next, a **Wireframe** is crucial to brainstorm and visualize what you want the main site to look like.
- This is a drawing of where you want your header, articles, images, and other elements of the page to be.
- Once all that is complete, keep in mind where you want to put information on your webpage.
  - If you want a certain link or article to catch the eye of the user first then keep in mind the color and font around it or within it.


## Javascript Programming

- Javascript is crucial to accessing and modifying content in HTML and CSS.
- It also allows you to make it more interactive 
- JS will also give you the ability to control the flow of the programming in the website.

### Writing a script

- The steps are as followed
  1. Define the goal
  2. Design the script
  3. Code each step

- For example, if the goal is to clean a hotel room you would ask these questions:
  - Does room need tidying?
  - Does minibar need restocking?
  - If you answer yes, you would be routed to the prompt to move on to next room.
  - If you answered no, you would be routed to how to clean room and restock minibar and the steps in that.

Duckett, John. *JAVASCRIPT & JQUERY: interactive front-end web development.* John Wiley and Sons, 2014. 

- In order for a computer to understand things you need to put in an **object** and **properties** of that object.
  - Each **property** then has a **name** and **value**.
- Now that these have been defined. There are **events** that can occur.