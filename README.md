# TODO Vanilla JS

A simple TODO example using vanilla JS but featuring HTML import and web components.

Please use Google-Chrome. No polyfills are provided so it may not work on other browsers (yet).

## How to test

Clone/download this repository. 

Due to the fact that this example uses HTML import, you must use a web-server to load the page (eg: ```python -m SimpleHTTPServer 8000```) and open the index.html.

## Architectural Design

The App is divided in 3 components: todo-form, todo-list and todo-item. The form contains a todo-list. The todo-list contains a list of todo-item. The user enters new TODOs using the todo-form. 

The data flow is as follow: the parent component is allowed to call methods from it's children. But the only way a child is allowed to interact with it's parent is by dispatching events. So it's a "one way data-flow" design.
