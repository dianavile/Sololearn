# HTML Fundamentals
HTML = a markup language, it use tags to identify content.
```
<p> I'm a paragraph < /p>
```
# Table of Content
- Modern Web Design
- Text formatting
- Headings, Lines, Comments
- Formatting text
- HTML Elements
- HTML Attributes
- Attribute Measurements
- Images
- Links
- List 
- Table
- Schedule

## Modern Web Design
__HTML__: Structure
__CSS__: Presentation
__JavaScript__: Behavior

## Text formatting
Browsers display < strong> as < b>, and < em> as < i>.
Yet, the meanings of these tags differ: 
- `< b>` and `< i>` define __bold__ and __italic__ text
- `< strong>` and `< em>`indicate the text is __"important"__
```
<html>
   <head>
      <title>first page</title>
   </head>
   <body>
      <p>regular text </p>
      <p><b> bold text </b></p>
      <p><big> big text </big></p>
      <p><i> italic text </i></p>
      <p><small> small text </small></p>
      <p><strong> strong text </strong></p>
      <p><sub> subscripted text </sub></p>
      <p><sup> superscripted text </sup></p>
      <p><ins> inserted text </ins></p>
      <p><del> deleted text </del></p>
   </body>
</html>
```

## Headings, Lines, Comments

### HTML Headings
HTML includes six levels of headings, which are ranked according to importance:
```
<html>
   <head>
      <title>first page</title>
   </head>
   <body>
      <h1>This is heading 1</h1>
      <h2>This is heading 2</h2>
      <h3>This is heading 3</h3>
      <h4>This is heading 4</h4>
      <h5>This is heading 5</h5>
      <h6>This is heading 6</h6>
   </body>
</html>
```
__NOTE:__ It is not recommended to use headings to make text big or bold, because search engines use headings to index the web page structure and content.

### Horizontal Lines
To create a horizontal line, use the < hr /> tag.
```
<html>
   <head>
      <title>first page</title>
   </head>
   <body>
      <h1>This is heading 1</h1>
      <h2>This is heading 2</h2>
      <h3>This is heading 3</h3>
      <h4>This is heading 4</h4>
      <h5>This is heading 5</h5>
      <h6>This is heading 6</h6>
      <p>This is a paragraph </p>
      <hr />
      <p>This is a paragraph </p>
   </body>
</html>
```
### Comments
The browser does not display comments:
<!-- This is a comment -->
Comments help document the HTML and add descriptions, reminders, and other notes.
<!-- Your comment goes here -->
```
Example:
<html>
   <head>
      <title>first page</title>
   </head>
   <body>
      <p>This is a paragraph </p>
      <hr />
      <p>This is a paragraph </p>
      <!-- This is a comment -->
   </body>
</html>
```
__NOTE:__ There is an exclamation point (!) in the opening tag, but not in the closing tag.

### Formatting Text
Example:
- About Me section for Blog contain a heading that's wrapped in a < h1> tag.
- Along with two paragraphs that format text using tags.

Example:
```
<h1><span>About Me</span></h1>
<p>
Hey! I'm <strong>Alex</strong>. Coding has changed my world  ...
</p>
<p class="quote">"Declare variables, not war"</p>
```
### HTML Elements
HTML documents are made up of `HTML elements`.
HTML elements consist of: `< opening tag> content < closing tag />`
HTML documents consist of `nested HTML elements`. 

Example:
- Body element includes `< p>`, `<br />` tag and content, `"This is a paragraph"`.    
```    
<html>
   <head>
      <title>first page</title>
   </head>
   <body> 
      <p>This is a paragraph <br /> line break </p>
   </body>
</html>
```
__NOTE:__ Some HTML elements (like the < br /> tag) do not have end tags.
HTML is scripting with elements within elements: like `<br />`
```
<html>
<head>
<title>Title</title>
</head>
<body>
<p>Some text</p>
</body>
</html>
```
### HTML Attributes
Attributes provide additional information about an element or tag, and modify them. 
Most attributes have a value; the value modifies the attribute.

Example:
- The value of "center" indicates the content within p element should be aligned to the center
```
<p align="center"> 
   This text is aligned to center
</p>
```
__NOTE:__ Attributes are always specified in the start tag, and they appear in name="value" pairs.

#### Attribute Measurements
The easurement units for the `width` attribute:
Example: 
- modify the horizontal line to have a width of 50 pixels or percentage 50%.
```
<hr width="50px" />// width= 50 pixel
<hr width="50%" /> // width= 50%
```
#### The Align Attribute
The `align` attribute is used to `specify how the text is aligned`, to the right, center or left.
```
<p  align ="left">
    <p  align ="center">
        <p  align ="right">
```            

Example: 
- A paragraph aligned to the center
- A line aligned to the right:
```
<html>
   <head>
      <title>Attributes</title>
   </head>
   <body>
      <p align="center">This is a text <br />
         <hr width="10%" align="right" /> This is also a text.
      </p>
   </body>
</html>
```
#### Attributes
What happens when you apply contradictory attributes within the same element?
```
<p align="center">
   This is a text.
   <hr width="50%" align="left" />
</p>
```
### Images
#### The <img> Tag
The <img> tag is used to __insert an image__. 
It contains only attributes, and does not have a closing tag. 
The image's URL (address) can be defined using the src attribute.

HTML image syntax:
```
<img src="image.jpg" />
```

#### Image Location
Add the `image location` for the __src attribute__ (between quotation marks). 

Example:
- a photo named "tree.jpg" in the same folder as the HTML file:
```
<html>
   <head>
      <title>first page</title>
   </head>
   <body> 
      <img src="tree.jpg" alt="" />
   </body>
</html>
```
__NOTE:__ In case the image cannot be displayed, the `alt attribute` specifies an alternate text that describes the image in words. 
The alt attribute is __required__.

#### Image Resizing
To define the image size, use the `width` and `height` attributes.
The value can be specified in pixels or as a percentage:

Example:
```
<html>
   <head>
      <title>first page</title>
   </head>
   <body> 
      <img src="tree.jpg" height="150px" width="150px" alt="" />
      <!-- or -->
      <img src="tree.jpg" height="50%" width="50%" alt="" />
   </body>
</html>
```
__NOTE:__ Loading images takes time. Using large images slow down your page. 
Use them with care.

#### Image Border
Use the `border` attribute within the `image tag` to create a border around the image.
```
<img src="tree.jpg" height="150px" width="150px" border="1px" alt="" /> 
```
__NOTE:__ By default, an image has no borders. 
However, by default, Internet Explorer 9, and its earlier versions, 
display a border around an image unless a border attribute is defined.

### Links

#### The a Tag
Links are an integral part of every web page. 
You can add links to text or images to enable the user to click on them to direct to another file or webpage.
In HTML, links are defined using the `< a>` tag.
Use the `href` attribute to define the `link's destination address`: 
```
<a href=""></a>
```

### Create a Link
Clicking on "Learn Playing" redirects you to a website.
Links can be either absolute or relative.

Example:
```
<a href="http://www.sololearn.com"> Learn Playing </a>
```
will display as a link:`Learn Playing`

`href`= attribute of the link tag, which contains the URL location to link to

#### The target Attribute
The `target` attribute specifies where to open the linked document.
A __blank value__ = link opens in a new window or new tab.

`<a href="2.html" target="_blank">`
 
Example:
```
<a href="http://www.sololearn.com" target="_blank">
   Learn Playing
</a>
```

### Lists

#### HTML Ordered Lists
An ordered list starts with the `< ol>` tag.
Each list item is defined by the `< li>` tag.

Example:
```
<html>
   <head>
      <title>first page</title>
   </head>
   <body>
      <ol>
        <li>Red</li>
        <li>Blue</li>
        <li>Green</li>
      </ol>  
   </body>
</html>
```
__NOTE:__ The list items will be automatically marked with __numbers__.

#### HTML Unordered List
An unordered list starts with the `< ul>` tag:
Example:
```
<html>
   <head>
      <title>first page</title>
   </head>        
   <body>
      <ul>
        <li>Red</li>
        <li>Blue</li>
        <li>Green</li>
      </ul>  
   </body>
</html>
```
__NOTE:__ The list items will be marked with __bullets__.
Use the <ul> tag, in which each item is represented by the `< li>` tag.

Example My Skills:
- My Skills section= unordered list of languages you know.
Example:
```
<h1><span>My Skills</span></h1>
 <ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
 </ul>
 ```
 
### Tables
Tables = `< table>` tag. 
Table rows =  `< tr>` tag.
Table columns= (table data) `< td>` tag.

Example: 
- a table with one row and three columns
 ```
<table>
   <tr>
      <td>Text 1</td>
      <td>Text 2</td>
      <td>Text 3</td>
   </tr>
</table>
 ```
__NOTE:__ Table data tags `< td>` act as `data containers` within the table.
They can contain __all sorts of HTML elements__, such as `text, images, lists, other tables`.
    
#### The Border and Colspan Attributes
A `border` can be added using the border attribute:
```
<table border="2">
```
Example:
- A `table cell` can __span two or more columns__:
 ```
<table border="2">
   <tr>
      <td>Red</td>
      <td>Blue</td>
      <td>Green</td>
   </tr>
   <tr>
      <td><br /></td>
      <td colspan="2"><br /></td>
   </tr>
</table>    
 ```
 
#### Colspan Color
Use the `rowspan` attribute, to make a cell span > 1 row.

Example:
- The `colspan` attribute:
```
<table border="2">
   <tr>
      <td>Red</td>
      <td>Blue</td>
      <td>Green</td>
   </tr>
   <tr>
      <td>Yellow</td>
      <td colspan="2">Orange</td>
   </tr>
</table>
```

#### The align and bgcolor Attributes
Use the `align` attribute inside table tag, to change table's position:
```
<table align="center"> 
```
- Use the `bgcolor` attribute, to a background color for a table cell. 
```
<table border="2">
   <tr>
      <td bgcolor="red">Red</td>
      <td>Blue</td>
      <td>Green</td>
   </tr>
   <tr>
      <td>Yellow</td>
      <td colspan="2">Orange</td>
   </tr>
</table>
```
__NOTE:__ In the case of styling elements, CSS is more effective than HTML.

#### Schedule
Use table tags to add a table to your blog that represents your daily learning schedule.
The `< th>` tags represent the table headers. 
 ```   
<h1><span>My Coding Schedule</span></h1>
<table>
<tr>
  <th>Day</th>
  <th>Mon</th>
  <th>Tue</th>
  <th>Wed</th>
  <th>Thu</th>
  <th>Fri</th>
</tr>
<tr>
  <td>8-8:30</td>
  <td class="selected">Learn</td>
  <td></td>
  <td></td>
  <td></td>
  <td></td>
</tr>
<tr>
  <td>9-10</td>
  <td></td>
  <td class="selected">Practice</td>
  <td></td>
  <td></td>
  <td></td>
</tr>
<tr>
  <td>1-1:30</td>
  <td></td>
  <td></td>
  <td class="selected">Play</td>
  <td></td>
  <td></td>
</tr>
<tr>
  <td>3:45-5</td>
  <td></td>
  <td></td>
  <td></td>
  <td class="selected">Code</td>
  <td></td>
</tr>
<tr>
  <td>6-6:15</td>
  <td></td>
  <td></td>
  <td></td>
  <td></td>
  <td class="selected">Discuss</td>
</tr>
</table>
 ```
__NOTE:__ The empty `< td>` tags represent empty table cells, necessary to maintain the table's structure.

### Inline and Block Elements

#### Types of Elements
In HTML, most elements are defined as `block level` or `inline elements`.
__Block level__-elements: start from a new line.
Example: 
 ```
 `<h1>, <form>, <li>, <ol>, <ul>, <p>, <pre>, <table>, < div>`
 ```
__Inline__ elements are `displayed without line breaks`:
Example: 
 ```
`<b>, <a>, <strong>, <img>, <input>, <em>, <span>`
 ```
#### The div element 
The `< div>` element is a __block-level__-element, used as a __container__ for _other HTML elements_.
Together with CSS styling, this element can be used to __style blocks of content__:
```
<html>
  <body>
    <h1>Headline</h1>
    <div style="background-color:green; color:white; padding:20px;">
      <p>Some paragraph text goes here.</p>
      <p>Another paragraph goes here.</p>
    </div>
  </body> 
</html>
   ```
__NOTE:__ `<div>`-element = a __block-level__-section in a document 

#### The span element 
The `<span>` element = an __inline__-element, used as a __container__ for _text_.
Together with CSS, the `<span>` element can be used to __style text parts__:
``` 
<html>
  <body>
    <h2>Some 
      <span style="color:red">Important</span>
    Message</h2>
  </body>
</html>
```
__NOTE:__ `<span>`-element= an __inline__-section in a document.

### Types of Elements
Other elements, like:
- APPLET - embedded Java applet
- IFRAME - Inline frame
- INS - inserted text
- MAP - image map
- OBJECT - embedded object
- SCRIPT - script within an HTML document
can be used either as __block level__ elements or __inline__ elements. 

__NOTE:__ You can insert  __inline__ elements inside __block__ elements: `<span>` elements inside a `<div>` element. 
 But you can not insert __block level__ elements into __inline__ elements.
 
### The form Element
HTML forms are used to collect information from the user.
The form is submitted to a web page on a web server.
Forms are defined using the `<form>` element:
```
<body>
   <form>…</form>
</body>
```
Use the __action attribute__ to point to a webpage to load after the user submits the form:
```
<form action="http://www.sololearn.com"> 
</form>
```
### The method and name Attributes: `GET` or `POST`
The method attribute specifies the __HTTP method__ used when forms are submitted:
 `GET`
 = form data visible in page address.
 ```
<form action="url" method="GET">
 ```

`POST`
 = form to update data, or include sensitive information (passwords).

 ```
<form action="url" method="POST">
 ```
 __NOTE:__ POST offers better security, the submitted data is not visible in the page address.

The `name`-attribute =specifies a name for a form. 
To take in user input, you need the corresponding form elements, such as text fields. 
The `<input>` element has many variations, depending on the type attribute, like `text, password, radio, URL, submit`. 

Example:
- A form requesting a username and password:
 ```
<form>
   <input type="text" name="username" /><br />
   <input type="password" name="password" />
</form>
 ```
### Form Elements
The input type  `radio` allows the user to select only one number of choices:
 ```
<input type="radio" name="gender" value="male" /> Male <br />
<input type="radio" name="gender" value="female" /> Female <br />
 ```
The type `checkbox` allows the user to select > 1 option:
  ```
<input type="checkbox" name="gender" value="1" /> Male <br />
<input type="checkbox" name="gender" value="2" /> Female <br />
 ```
 EXAMPLE: 
  ```
<form method="POST" action="#">
<input type="text" name="name">
   <input type="submit" name="submit">
</form>
 ```
The `submi`t button submits a form to its action attribute:
 ```
<input type="submit" value="Submit" /> 
 ```
 __NOTE:__ After the form is submitted, the data should be processed on the server using a programming language, like PHP.
 
### Contact Form
- Include Name, Email, Message fields and a Submit button.
Example:
 ```
<h1><span>Contact Me</span></h1>
<form>
  <input name="name" type="text" /><br/>
  <input name="email" type="email" /><br/>
  <textarea name="message"></textarea>
  <input type="submit" value="SEND" class="submit" />
</form>
 ```
 __NOTE:__ To submit a real form and process the data, you'd need to create server-side code. 
 
### HTML Colors!
HTML colors are expressed as `hexadecimal values` : `0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F`
It consists of 16 values, from `0`(=lowest value) to `F`(=highest value). 

#### HTML Color Model
Colors are displayed in combinations of __red, green, and blue__ light `(RGB)`.
Hex values are written using the hashtag symbol (#), followed by either 3/6 hex characters.

#### Color Values
All RGB combinations together give a potential number of over 16 million colors, which can be mixed to form additional colors.

