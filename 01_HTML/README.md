# Let's learn about HTML

## Course Module 1: The Basics of HTML

### Part 1: The Foundation of the Internet

HTML, or HyperText Markup Language, is considered the skeleton of the entire internet. It's the basic structure that all web pages are built on. This might seem like a big statement, but when you delve into HTML, you'll understand that it's actually constructed from just 145 simple words, known as 'tags'. 

### Part 2: Understanding HTML Tags

In HTML, every tag is enclosed within less than and greater than signs, like so: `<tagname>`. This is known as an opening tag. Most tags will also include a corresponding closing tag, formatted with a forward slash before the tag name: `</tagname>`. 

Each usage of a tag in HTML is referred to as an 'element'. These elements are what you see when you browse a website. While the terminology might be confusing initially, it will become clear as we progress. In a nutshell, remember that a 'tag' refers to the textual representation, while an 'element' is the actual component you see on the website.

### Part 3: Tag Attributes

HTML tags can also have 'attributes', which are additional properties specified within the opening tag. These attributes are key in customizing the function and appearance of HTML elements. An example is the 'type' attribute in an input tag that specifies whether it's a regular button or a submit button. For an exhaustive list of attributes, refer to the [Mozilla Developer Network](https://developer.mozilla.org/en-US/).

### Part 4: Essential HTML Tags

Although there are 145 tags, you'll only need a handful to start building a functional website. 

- `<!DOCTYPE html>`: This tag is always at the very top of your HTML files and instructs the browser to render the content according to standard HTML rules. 

- `<html></html>`: This tag encapsulates all the content of your website. Only the DOCTYPE tag resides outside of it. 

- `<head></head>`: This tag houses the metadata, providing the browser with information about your page. It's placed inside the top of the `<html>` tag.

- `<title></title>`: While optional, this tag is highly recommended. It specifies the text to display on the browser tab. It should be nested within the `<head>` tags. 

- `<body></body>`: This tag encompasses the actual content of your webpage - everything the users can see and interact with. It is placed directly after the `<head>` tag.

By implementing these tags, you essentially have a functional website that can be hosted and displayed on the internet.

### Part 5: Common Display Tags

As you get started with HTML, you'll frequently use these display tags:

- `<div></div>`: Known as the division tag, it separates and styles elements. It primarily acts as a container for other tags or text.

- `<p></p>`: The paragraph tag is used to define text paragraphs. Browsers usually apply default spacing for these tags.

- `<h1></h1>`: This is the heading tag, influencing the size of enclosed text. Numbers 1-6 can be used to denote different heading levels, with 'h1' being the main point and 'h6' the smallest sub-point.

- `<img />`: This tag embeds an image. It needs the 'src' attribute to specify the image source, like so: `<img src="images/picture.png" />`.

- `<a></a>`: The anchor tag is used to create hyperlinks. The 'href' attribute specifies the destination URL, for instance, `<a href="https://www.samhuckaby.com">sam’s website</a>`.

- `<button></button>`: This creates a clickable button. Any text between the tags will be displayed on the button.

- `<input />`: This tag is used to create input fields where users can enter data. By default, it's a text field. However, the 'type' attribute can modify this to a variety of inputs like numbers, emails, etc.

While there are many more tags, the ones listed above make up about 95% of what you'll use in most web projects.

![An HTML tag with each part labelled](Anatomy_of_html_tags.png)

## Course Module Review and Exercises

### Module Review

Test your understanding of the concepts we've covered in this module by answering the following questions:

1. Which of the following tags does NOT have an opening tag?
   - div
   - button
   - a
   - img

2. Which optional attribute can you add to an input tag to change how it is displayed?
   - kind
   - type
   - prop
   - use

3. Which tag surrounds all of the rest (except the DOCTYPE)?
   - html
   - body
   - head
   - div

4. What symbols surround HTML tags?
   - < and >
   - ( and )
   - { and }
   - [ and ]

### Module Exercises

**Exercise 1: Hello World**
Follow these steps to create your first HTML page:

1. Open a new file in your text editor of choice.
2. Enter the following lines into the file:
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Exercise 1</title>
	</head>
	<body>
		<p>Hello World</p>
	</body>
</html>
```
3. Save the file as “index.html”.
4. Locate it on your computer and open it with your preferred web browser.
5. Note that the page’s title is “Exercise 1”.
6. Modify index.html so that the browser tab says “My MTG Deck”.

**Exercise 2: Deck Display**
Now, we'll modify our HTML file to display more information about your MTG deck.

1. Open “index.html” from the first exercise.
2. Remove the “Hello World” and its paragraph tags.
3. Add a 1st-level heading (`<h1>`) with the text “Deck Description”.
4. Under (and outside) that h1, add a paragraph with a short MTG deck description.
5. Below that, add another 1st-level heading (`<h1>`) called “Win-con”.
6. Add a paragraph under that h1 that describes one or more win conditions for the deck described under the first heading.
7. Add another 1st-level heading (`<h1>`) with the text “Deck Cards”.
8. Add a list of 5-10 MTG card names separated with commas (for now, don't add the entire deck).
9. Save and open the page in a browser to ensure it looks right.

**Exercise 3: The Commander**
Next, let's add a visual element to your page, featuring the commander of your deck.

1. Above the first heading, add an `<img />` tag.
2. Find an image online of a commander card for your deck and copy the image’s URL.
3. Modify your new `<img />` tag to add a “src” attribute and assign it the value of the URL you copied, like so: `<img src=”[your url here]” />`.
4. *Bonus*: Can you add the name of the Commander in large text under the image?

## Course Module 2: Advanced HTML Elements and Expanding Beyond HTML

### Part 1: Advanced HTML Elements

As you progress in your HTML journey, there are several advanced elements that you will use in specific scenarios. Often, these elements are styled or modified to achieve a unique appearance or functionality, deviating from their standard HTML look and feel.

- `<form></form>`: The form element encapsulates a logical unit of inputs. For example, if you're creating an app for Magic The Gathering (MTG) deck, you might have a form that collects deck details such as the name, description, price, and cards in the deck. When the form is submitted, all the input values are sent together to a location defined by the 'action' attribute, using the HTTP request method specified by the 'method' attribute.

- `<ul></ul>`: The 'unordered list' element, along with its counterpart, `<ol></ol>` (ordered list), provide HTML list functionality. Ordered lists are numbered, while unordered lists typically feature bullet points. Unordered lists are commonly styled into menus with CSS due to their inherent design of displaying list items next to each other.

- `<label></label>`: The label tag provides a name for an input element, usually within a form. Although it offers little visual benefit, it's recommended for accessibility purposes (commonly referred to as 'a11y'). A neat feature is that clicking on a label moves the focus to its associated input element.

### Part 2: Transitioning from HTML

HTML forms the backbone of any website, akin to the sculptor's clay. But relying solely on HTML will result in static, simplistic, and relatively unappealing websites. The true power of HTML emerges when it's combined with other technologies, such as CSS and JavaScript.

- `<link />`: The link tag, among its various uses, is essential for integrating stylesheets into your website. Stylesheets are CSS files that instruct the browser on how to display your tags. The link tag is placed in the `<head>` section of your website and requires two attributes: 'href' and 'rel'. An example would be: `<link href="path/to/stylesheet.css" rel="stylesheet" />`.

- `<script></script>` or `<script src="" />`: The script tag is used to incorporate external files (predominantly JavaScript) into your website. This tag usually resides in the `<head>` section of the website, but it can also be placed at the bottom of the `<body>` section, causing the file to load simultaneously with the website content.

It's important to note that items added to the `<head>` are loaded into the browser's memory before the page is displayed to the user, while items in the `<body>` load as the page is displayed. While this loading process is generally fast, larger files may cause a noticeable delay.

In this course, we'll primarily load files into the `<head>` section as the necessary files are known beforehand, and we won't be dynamically generating anything.

## Course Module Review and Exercises

### Module Review

Test your understanding of the concepts we've covered in this module by answering the following questions:

1. Which tag lets you load CSS “stylesheets” into your website?
   - `<form></form>`
   - `<style></style>`
   - `<link />`
   - `<script />`

2. What is the primary difference between `<ol>` and `<ul>`?
   - `<ol>` is much older than `<ul>`
   - `<ul>` makes ugly links and `<ol>` makes orphan links
   - `<ul>` is unordered and `<ol>` is ordered
   - `<ol>` isn’t real but `<ul>` is

3. When is a `<script>` tag in the body loaded?
   - Never
   - Before the website is shown to the user
   - At the time the website is shown to the user
   - Right as the user closes the website

### Module Exercises

**Exercise 1: Magic Powers**
In this exercise, we'll add some styling to our HTML page using an external CSS framework.

1. Open the index.html file that you have been working in.
2. Add a new script tag at the bottom of the `<head>` section with no attributes.
3. Add an `src` attribute and give it the value “https://cdn.tailwindcss.com”.
4. Add an attribute to your opening `<body>` tag called “class” and give it the value “bg-blue-600”.
5. Add a “class” attribute to all of your `<h1>` tags and give all of them the value "text-2xl text-white".
6. Save your file and reload the website in your browser.

*Note*: Tailwind is a JavaScript library that lets you give CSS styles to your website using only classnames. We will discuss CSS in the next section, but this exercise should give you a taste of what CSS is capable of. Keep in mind that pure CSS is much more powerful and flexible than Tailwind.
