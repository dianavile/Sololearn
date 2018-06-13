# HTML5

## Doc type declaration:
```
<!DOCTYPE HTML>
```

### Character encoding (charset) declaration:
```
<meta charset="UTF-8">
```
The default character encoding in HTML5 is UTF-8.

### New Elements in HTML5
```
<article>
<aside>
<audio>
<canvas> 
<datalist>
<details>
<embed>
<footer>
<header>
<nav>
<output>
<progress>
<section>
<video>
```

### Valid HTML5 doctype:
```
<!DOCTYPE  HTML>
<html>
<head>
<title>Title</title>
</head>
<body>
The content of the document
</body>
</html>
```

## New in HTML5
### Forms
- The Web Forms 2.0 specification allows for creation of more powerful forms and more compelling user experiences.
- Date pickers, color pickers, and numeric stepper controls have been added.
- Input field types now include email, search, and URL.
- PUT and DELETE form methods are now supported.

### Integrated API (=Application Programming Interfaces) 
- Drag and Drop
- Audio and Video
- Offline Web Applications
- History
- Local Storage
- Geolocation
- Web Messaging


## The List of Content Models
In HTML, elements typically belonged in the `block level` or `inline content` model. 
HTML5 introduces 7 main content models:

- 1) Metadata
- 2) Embedded
- 3) Interactive
- 4) Heading
- 5) Phrasing
- 6) Flow
- 7) Sectioning 

The HTML5 content models are designed to make the markup structure more meaningful for browser and web designer.

### Content Models

__Metadata:__ `Content that sets up presentation or behavior of rest of the content`. = in the head of the document.
_Elements:_`<base>, <link>, <meta>, <noscript>, <script>, <style>, <title>`

__Embedded:__ `Content that imports other resources into the document.`
_Elements:_ `<audio>, <video>, <canvas>, <iframe>, <img>, <math>, <object>, <svg>`

__Interactive:__ Content specifically intended for user interaction.
_Elements:_ `<a>, <audio>, <video>, <button>, <details>, <embed>, <iframe>, <img>, <input>, <label>, <object>, <select>, <textarea>`

__Heading:__= a section header.
_Elements:_ `<h1>, <h2>, <h3>, <h4>, <h5>, <h6>, <hgroup>`

__Phrasing:__ `This model has a number of inline level elements in common with HTML4.`
_Elements:_ `<img>, <span>, <strong>, <label>, <br />, <small>, <sub>`

__NOTE:__ The same element can belong to more than one content model.

The various content models overlap in certain areas, 
depending on how they are being used:

__Flow content:__Contains the majority of HTML5 elements that would be included in the normal flow of the document.

__Sectioning content:__scope of headings, content, navigation, and footers.
Elements: `<article>, <aside>, <nav>, <section>`


### Page Structure in HTML5
A generic HTML5 page structure looks like this:

```
<header>
<nav>
<article>
<section> 
<footer>
```
__NOTE:__ You may not need some of these elements, depending on your page structure.

### The header Element
In HTML4, we would define a header like this:
`<div id="header">`

In HTML5, a `<header>` tag is used.
The <header> element is appropriate for use inside the body tag.
    
```
<!DOCTYPE html>
<html>
   <head></head>
   <body>
      <header>
        <h1> Most important heading </h1>
        <h3> Less important heading </h3>
      </header>
   </body>
</html>
```
__NOTE:__ Note that the `<header>` is completely different from the `<head>`tag.

### The footer element 
The `<footer>` Element = to refer the section located at the bottom of the web page.

`<footer>…</footer>`

The footer contains the following information:
- Contact Information
- Privacy Policy
- Social Media Icons
- Terms of Service
- Copyright Information
- Sitemap and Related Documents

### The nav Element
The <nav> Element tag = a section with navigation links to other pages or within the page. 

``` 
<nav>
   <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Services</a></li>
      <li><a href="#">About us</a></li>
   </ul>
</nav>
```
__NOTE:__ Not all of the links in a document should be inside a `<nav>` element. This element is intended only for major blocks of navigation links. 
The `<footer>` element often has a list of links that don't need to be in a` <nav>` element.

### Article, section & Aside
#### The article Element
The `<article>`-element = a self-contained piece of content to be used and distributed separately from the rest of the page or site. This could be a forum post, a magazine or newspaper article, a blog entry, a comment, an interactive widget or gadget, or any other independent piece of content. 

The `<article>` element replaces the `<div>` element that was widely used in HTML4, along with an `id` or `class`.
```
<article> 
   <h1>The article title</h1> 
   <p>Contents of the article element </p>
</article>
```
__NOTE:__ When an <article> element is nested, the inner element represents an article related to the outer element. 
For example, blog post comments can be <article> elements nested in the <article> representing the blog post.
    
#### The section Element 
A `<section>`- element = a logical container of _page_ or _article_. 
Sections can be used to divide up content within an article. 
Each <section> should be identified, by including a heading (h1-h6 element) as a child of <section>.
      
Example:
- a homepage with a section for introducing the company, news items, and contact information.
```
<article>
   <h1>Welcome</h1>
   <section>
      <h1>Heading</h1>
      <p>content or image</p>
   </section>
</article>    
```
__NOTE:__ If it makes sense to separately syndicate the content of a <section> element, use an <article> element instead.

#### The aside Element
The <aside> Element = secondary (tangential) content, separate from but indirectly related to the main content.
This is represented in sidebars.
When an <aside> tag is used within an <article> tag, the content of the <aside> should be specifically related to that article.
    
Example:
```    
<article>
   <h1> Gifts for everyone </h1>
   <p> This website will be the best place for choosing gifts </p>
   <aside>
      <p> Gifts will be delivered to you within 24 hours </p>
   </aside>
</article>
``` 
### The Audio element
__Audio on the Web__: Before HTML5, there was no standard for playing audio files on a web page.
The HTML5 ` <audio>`  element specifies a standard for embedding audio in a web page.

#### How to specify the audio source file's URL. 
METHOD 1: use __source attribute__:
``` 
<audio src="audio.mp3" controls>
   Audio element not supported by your browser
</audio>
```     

METHOD 2: use __<source> element inside <audio> element__:
``` 
<audio controls>
   <source src="audio.mp3" type="audio/mpeg">
   <source src="audio.ogg" type="audio/ogg">
</audio>
 ``` 
Multiple <source> elements can be linked to different audio files. The browser will use the first recognized format.    

### Audio on the Web
The <audio> element creates an audio player inside the browser.
``` 
<audio controls>
   <source src="audio.mp3" type="audio/mpeg">
   <source src="audio.ogg" type="audio/ogg">
   Audio element not supported by your browser. 
</audio>
 ``` 
__NOTE:__The text between the <audio> and </audio> tags will display in browsers that do not support the <audio> element.    
