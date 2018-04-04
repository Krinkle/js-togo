# 08: Hello Web

This exercise aims to explain the difference between three things: the JavaScript programming language, the Node.js environment, and the environment provided to scripts in a web browser.

## JavaScript

The previous exercises have focussed on the characteristics of the JavaScript programming language. The following are all part of this language: The syntax for creating variables, functions, and arrays; the syntax we use for conditional statements and loops; the behaviors for object inheritance and accessing properties; the mathematical functions; and more.

The language does not provide ways to obtain input from elsewhere or ways to communicate with other systems. In order to do that, there needs to be an environment that mediates between your program, the computer, and the outside world.

## Node.js

Node.js (pronounced *node jay es*") is a system you can use to run JavaScript programs from the command-line. It runs your program in an special environment with built-in variables and functions that provide access to useful abilities. For example, the `process.argv` property of the [`process`](https://nodejs.org/api/process.html) module enables a program to read parameters from the command-line, and the [`console`](https://nodejs.org/api/console.html) module enables a program to write text back to the command-line. There are also modules for interacting with the hard drive, the system clock, the Internet, and more.

## Web browser

Modern web browsers also include a JavaScript engine. And browsers provide ways for HTML web pages to load and execute a JavaScript program. When a web browser executes a JavaScript program, it runs the program in a special environment with built-in variables and functions for interacting with the web page, as well as various other utilities. For example, the [Location](https://developer.mozilla.org/en-US/docs/Web/API/Location) interface enables a script to know the web address (URL) of the current web page, and the [Document](https://developer.mozilla.org/en-US/docs/Web/API/Document) and [Window](https://developer.mozilla.org/en-US/docs/Web/API/Window) interfaces which provide ways to inspect or modify the current page.

## Hello Web

Today we will create a basic HTML web page, and a program ("script") that runs in the web browser's JavaScript environment associated with that web page.

I assume basic understanding of HTML. However, if you're unfamiliar or need a refresher, I can recommend the following resources:

* [Learn HTML at Codecademy](https://www.codecademy.com/learn/learn-html)
* [Intro to HTML at Code.org](https://curriculum.code.org/csd-1718/unit2/3/)
* [Getting started with the Web at MDN](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web)
* [HTML Basics at MDN](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics)

Copy the following snippet to your editor and save it in a file in the current directory. Make sure to end the file name with `.html`. For example, `page.html`.

```html
<!DOCTYPE html>
<html>
<p>Hello Web!</p>
</html>
```

The `<html>` element contains the contents of our page. It ends at `</html>`. The above snippet contains only a paragraph. To render our page, open the page in your web browser by dragging-and-dropping the file from your file explorer to a new browser window.

Feel free to expand the page with some more content. For example, add a heading, or a link, and perhaps add some emphasis to your text with bolding. (Hint: `<h1>`, `<a href>`, and `<strong>`).

As you change the file, save regularly and refresh the browser window to render the updated version.

## `<script>`

The final part of this introduction is to embed a JavaScript program in our web page. To do this, we write the program inside a `<script>` element. For example, add the following before `</html>`:

```html
<script>
var name = 'Alice';
window.alert(name);
</script>
```

This uses the built-in `alert()` method of the [Window](https://developer.mozilla.org/en-US/docs/Web/API/Window) interface, to create a model dialog that displays the specified string text. Try it out!

Feel free to change or this embedded program to display different values. For example:

* Try creating multiple variables, combining them into one, and displaying the combined string with `alert()`.
* Try performing mathematical functions like addition or multiplication, and displaying the result.
