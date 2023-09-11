# User Guide


# What is PyScript - Features

PyScript is a software platform that combines the power of the web with the power and simplicity
of the most popular programming language in the world to provide an ecosystem that let users create
and distribute applications in seconds, while having fun.


## How does it work?

The PyScript library provides HTML tags for embedding and executing Python code in your browser. PyScript is built using Pyodide, the WebAssembly port of CPython, which is compiled using Emscripten.

PyScript turns the browser into a code deployment tool that anyone can learn to use.

Example
In this example, we are using the <py-script> HTML tag to generate a Matplotlib figure and display it as an image. Click Preview to see the rendered HTML.

To try it in your browser, copy the code below into an online HTML editor like W3School’s Tryit Editor, which allows you to modify, run, and even save your code. Watch the video below to see it in action!


## Features

### Run Python code in the browser

#### In the main thread

#### In a web worker

### Environment Setup

#### Install Python Packages

#### Download files and assets

### Error reporting

### Pythonic Web APIs

### Access to Javascript


# Serving your application

Now what we have written our first application, it's important talk about how we can access it.

In the example above, we were able to visualize it by simply opening the local file from our
system directly with the browser. While that's a very simple and fast way to open our application,
it is not very recommended because browsers will forbid many features when accessing files this way,
for security reasons. When this is the case, you may see your Python code in the text of the webpage,
and the [browser developer console](https://balsamiq.com/support/faqs/browserconsole/) may show an
error like *"Cross origin requests are only supported for HTTP."*

In short, when browsers visualize a web page, they expect them to be served by a
web server. Here are a few options that we can use to fix this issue:

**NOTE:** If you are an experienced developer and already know how to host and serve files on a [static]
web server, feel free to skip to the next section.

TODO: It seems better to not go too deep into "how to serve a PyScript application" but to point to a dedicated
section where we can add more options and actually point to other resources as well.

### Using pyscript.com

If you clicked on <a href="https://fpliger.pyscriptapps.com/hello-world-minimal-example/latest/" target="_blank">the link above</a>
you've already saw how pyscript.com can be used to host PyScript applications.

All you need to do is to create a free account and copy or start creating new projects.

### Using a Local Server

A very common fix for this is to use a [simple local server](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Tools_and_setup/set_up_a_local_testing_server) to make your html file available to the browser.


If you have python installed on your system, you can use it's basic built-in server for this purpose via the command line.
Change the current working directory of your terminal or command line to the folder where your HTML file is stored.
From this folder, run `python -m http.server 8080 --bind 127.0.0.1` in your terminal or command line. With the server
program running, point your browser to `http://localhost:8080` to view the contents of that folder. (If a file in
that folder is called `index.html`, it will be displayed by default.)
