# publisher-illote-front-end

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lin
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


## THE WEBSITE(PLEASE OPEN ON YOUR PHONE ANDROID !!!)

url: https://illote-fe.firebaseapp.com


## THE QUESTION

## What can you recommend to improve the HTML pages that you have created?

  # answer: 
    "Because I'm using vue, I need to split routes component into separte chunk."

## What  you cannot implement on those case ? and please explain why
  
  # answer: 
    "The header of the website, because I dont have assets. FYI many of assets I get import from original illote website. I'm just clone cdn url."

## What is a DOM? What do you know about it?

  # answer: 
    "The DOM is an interface to an HTML document. It is used by browsers as a first step towards determining what to render in the viewport."

## Explain critical rendering path 

  # answer : 
    "6 steps when the browser request HTML Document to display style and interactive website. The 6 step was:
    1. Constructing the DOM Tree
    2. Constructing the CSSOM Tree
    3. Running JavaScript
    4. Creating the Render Tree
    5. Generating Layout
    6. Painting"

## What is the factors for fast page load time?
  # answer : 
    " 1.  HTTP request, every web have high request like image, style, or javascript. Reducing http your http request.
      2.  Minify your file, because if we request htpp more lager file more slow your request. With minify u can reduce number of file.
      3.  Asynchronus CSS or Javascript, because CSS or JavaScript file that is not asynchronous, 
        it will stop loading until it has fully loaded that particular file. 
        If that same file were asynchronous, the browser could continue loading other elements on the page at the same time."

## How to reduce the size of downloadable html  page size by the browsers?
  # answer : 
    "Minify our code, Reduce image using thumbor, and using browser chaching"

## When do DOMContentLoaded and Load events get fired ?
  # answer : 
    " The DOMContentLoaded event is fired when the document has been completely loaded and parsed, 
      without waiting for stylesheets, images, and subframes to finish loading. 
      But the load event can be used to detect a fully-loaded page. So After All page fully loaded."

## Would you place an async script tag right before body ?
  # answer : 
    "No, because make HTML DOM waiting until script done and make parser blocking. Because if your js have reference element first."
  
## Is it generally a good idea to position CSS links before script tags?
  # answer:
    "Yes, because CSS loaded first and make your website have nice view when rendering. 
      If script first you will have blank page and have a nice view until your script has been loaded."
  
## What versioning control do you familiar to use? Git or SVN or not any
  # asnwer: 
    " GIT "
## List some commands on the version control you usually use above and explain the purpose of each commands
  # answer:
    " git fetch: needed for looking what a new update on the server and every branch, 
      git add remote: add link remote to connect to the sever git, 
      git merge: needed for merge with update specific branch, 
      git push: push our work local to server git,   
      and git pull: it same like git fetch and then do git merge"

