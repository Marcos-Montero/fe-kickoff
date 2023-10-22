# HTML

- HTML stands for **Hypertext Markup Language**. It is a standard markup language used to create web pages.
- It is the **foundation of all websites** and is used to **create the structure** and **content** of a web page.

## Tags

It is **based on _Tags_** that, depending if they have content, can be
self closed `<tag />` or opened and closed `<tag>content</tag>`

## Attributres

Each tag can be modified by defining _attributes_ within the tag `<tag attribute1="" attribute2="" />`. There are plenty of them and they vary from one tag to another so **there's absolutely no sense on trying to learn them**. You will learn the most common ones by practicing and just searching in the online docs whenever you wonder how to do something.

<hr>

## The 25 tags you do need to know

### Structural tags

| Tag        | Description                                              |
| ---------- | -------------------------------------------------------- |
| `<html>`   | Defines the root of an HTML document                     |
| `<head>`   | Contains metadata about the document                     |
| `<link>`   | links the HTML document to other documents (CSS)         |
| `<body>`   | Contains the visible content of the document             |
| `<footer>` | Last section of the page, filled with legal, contact,... |

#### Basic struture example

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Title of the Document goes here</title>
    <link rel="stylesheet" href="./styles.css" />
  </head>
  <body>
    Everything that the user will actually see will go here
  </body>
</html>
```

<hr>

### Most used tags

| Tag           | Description                  |
| ------------- | ---------------------------- |
| `<h1>`-`<h6>` | headings of different levels |
| `<p>`         | paragraph                    |
| `<a>`         | link                         |
| `<div>`       | division                     |
| `<button>`    | button                       |
| `<section>`   | section                      |
| `<span>`      | small section                |
| `<img>`       | image                        |

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Example of Most used tags</title>
  </head>
  <body>
    <h1>This is a level 1 heading</h1>
    <h2>This is a level 2 heading</h2>
    <h3>This is a level 3 heading</h3>
    <h4>This is a level 4 heading</h4>
    <h5>This is a level 5 heading</h5>
    <h6>This is a level 6 heading</h6>
    <p>This is a paragraph.</p>
    <a href="https://www.example.com">This is a link</a>
    <div>This is a division.</div>
    <button>Click me!</button>
    <section>
      <h2>This is a section</h2>
      <p>This is a paragraph inside a section.</p>
    </section>
    <span>This is a small section.</span>
    <img src="https://www.example.com/image.jpg" alt="This is an image" />
  </body>
</html>
```

### Specific but common use cases: lists, tables & forms

#### Lists

| Tag    | Description    |
| ------ | -------------- |
| `<ul>` | Unordered list |
| `<ol>` | Ordered list   |
| `<li>` | List item      |

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Example of Unordered and Ordered Lists</title>
  </head>
  <body>
    <h1>Example of Unordered and Ordered Lists</h1>
    <h2>Unordered List</h2>
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ul>
    <h2>Ordered List</h2>
    <ol>
      <li>First item</li>
      <li>Second item</li>
      <li>Third item</li>
    </ol>
  </body>
</html>
```

#### Tables

| Tag       | Description       |
| --------- | ----------------- |
| `<table>` | Table             |
| `<tr>`    | Table row         |
| `<th>`    | Table header cell |
| `<td>`    | Table data cell   |

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Example Table</title>
  </head>
  <body>
    <table>
      <thead>
        <tr>
          <th>First Name</th>
          <th>Last Name</th>
          <th>Age</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>John</td>
          <td>Doe</td>
          <td>30</td>
        </tr>
        <tr>
          <td>Jane</td>
          <td>Smith</td>
          <td>25</td>
        </tr>
        <tr>
          <td>Bob</td>
          <td>Johnson</td>
          <td>40</td>
        </tr>
      </tbody>
    </table>
  </body>
</html>
```

#### Forms

| Tag          | Description                |
| ------------ | -------------------------- |
| `<form>`     | Form for user input        |
| `<input>`    | Input field                |
| `<select>`   | Dropdown list              |
| `<option>`   | Option in a dropdown list  |
| `<textarea>` | Multiline input field      |
| `<label>`    | Label for an input element |

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Example Form</title>
  </head>
  <body>
    <h1>Example Form</h1>
    <form>
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" /><br /><br />

      <label for="email">Email:</label>
      <input type="email" id="email" name="email" /><br /><br />

      <label for="age">Age:</label>
      <input type="number" id="age" name="age" /><br /><br />

      <label for="gender">Gender:</label>
      <select id="gender" name="gender">
        <option value="male">Male</option>
        <option value="female">Female</option>
        <option value="other">Other</option></select
      ><br /><br />

      <label for="message">Message:</label>
      <textarea id="message" name="message"></textarea><br /><br />

      <button type="submit">Submit</button>
    </form>
  </body>
</html>
```

### Connecting JavaScript to HTML

| Tag        | Description                 |
| ---------- | --------------------------- |
| `<script>` | Section for JavaScript code |

JavaScript (JS) The programming language for building any complex logic on the web.

You can use it by writing it directly in the html file or by importing a .js file into an .html file:

- write in the html file: `<script>js code here</script`
- import js cod from a .js file in html: `<script src="jsFile.js" />`

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Example HTML with JavaScript</title>
    <!-- JS file linked in the head -->
    <script src="example.js"></script>
    <script>
      // JavaScript code in the head
      console.log("Hello from the head!");
    </script>
  </head>
  <body>
    <h1>Hello, world!</h1>
    <p>This is an example HTML file that links to a JavaScript file.</p>
    <script>
      // JavaScript code in the body
      console.log("Hello from the body!");
    </script>
    <!-- JS file linked in the body -->
    <script src="example2.js"></script>
  </body>
</html>
```
