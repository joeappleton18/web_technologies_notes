# Practical 1 

![](../../../assets/block_2/workflow.png)


<cite> Figure 1 - Web Technologies Recommended Workflow </cite>



The purpose of this practical is to introduce you to the [basic workflow that we'll be using throughout this course](1_what_is_workflow.md).
In doing so you'll also learn the basics of HTML. 

Follow the videos below, to be walked through the practical 


# 1 Creating your HTML CV
This video introduces you to the basics of HTML and the workflow you'll be using throughout this
course. It will also introduce you the practical task:

<iframe width="560" height="315" src="https://www.youtube.com/embed/BAu6cdUrWHU" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

# 2 Uploading your work to GIT HUB

This video shows you how to upload your work to gitHUB, you should do this once you've completed your 
basic HTML CV.

<iframe width="560" height="315" src="https://www.youtube.com/embed/ANISOnDSjq8" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

# Practical 1 Notes

Introduction To HTML

- [What is HTML](#what-is-html)
- [Tools used To Create HTML Pages](#tools-used-to-create-html-pages)
- [HTML Elements](#html-elements)
- [HTML Attributes](#html-attributes)
- [HTML Comments](#html-comments)



##What is HTML?


>> [We're on HTML version 5](https://www.w3.org/TR/html5/)   

- Hyper Text Markup Language
- Designed for the creation of web pages and other information viewable in a browser
- We’re currently on version 5
- File extension, needs to be .html or .htm


##Tools Used To Create HTML Pages

>> [Cloud 9](https://c9.io/joeppleton18) for university 
>> [Visual Studio Code](https://code.visualstudio.com/)  for at home

##HTML Elements 

- An HTML document is made up of elements also know as HTML tags
	- elements are containers for content
	- everything from the start tag to the end tag
	- some types of element may contain other elements
	- An html document starts with the doctype `<!DOCTYPE html>`
	- The rest of the document is nested in-between  `<html>` tags

- HTML tags are enclosed in < brackets:

```html  
<tagname>content</tagname>  
```	

An complete HTML document example:


```html
<!DOCTYPE html>
<html>
	  <head>
			<title>my first page</title>
	  </head>
      <body>
			<h1>This is my first Web Page</h1>
			<p>I should write a paragraph about myself</p>
			<img src="image.jpg" alt="describe the image” >
			<a href="http://www.solent.ac.uk">University</a>
      </body>
</html>

```

[Read W3 Schools for an introduction to different tags](http://www.w3schools.com/html/html_intro.asp)


Let's breakdown the above example in some more detail:

- `<html> .. </html>` - all of the information is embedded between these tags

- `<head>...</head>` - contains descriptive information about the content to come
	- 	`<title>..</title>` - as it sounds, it is the title for the page

- `<body>...</body>` - The main content of the document 
- `<p>..</p>` -  a paragraph tag to hold a paragraph of text
-  	<a>...</a> -  this is a how we create a hyperlink, anything between the two hyperlink tags will be clickable 


##HTML Attributes

- Each element may have one or more attributes
  provide additional information about elements
  specified in the start tag
  
- Attributes come in name/value pairs like: name="value"

- Below, we use attributes to specify the source of an image and where a link should point to
  
  
```html
<img src="image.jpg" alt="describe the image" />
<a href="http://www.solent.ac.uk">University</a>

```

##HTML Comments 

HTML comments allow you to embed statements into an html which won't be shown to the user


```html
	<!-- this is an html comment -->

```






