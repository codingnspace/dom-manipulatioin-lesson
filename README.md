# Building Interactive Webpages Part II

## Recap
1) DOM = Document Object Model

Your HTML files are the blueprint while the DOM is the physical (or "real") structure

2) You need knowledge of the DOM in order to select pieces or elements of the webpage that you want to add interaction to.

3) There are 3 ways to add interaction to a webpage

  * [CSS Pseudo Class Selectors](https://www.w3schools.com/css/css_pseudo_classes.asp)
```
button {
  background-color: blue;
  color: white;
}

button:hover {
  background-color: red;
}
```
[code exercise #1](https://codepen.io/pearl1991/pen/NoEEXv) | [code exercise #2](https://codepen.io/pearl1991/pen/XOyyOQ)

  * [DOM Manipulation](https://www.theodinproject.com/lessons/dom-manipulation)
  ```
  // Use DOM Selectors to Query the DOM
  document.querySelector('div') // selects the first div in the DOM
  document.querySelector('.cat-pic') // selects the first element that has a "cat-pic" class
  document.querySelector('#dog-pic-1') // selects the element that has a "dog-pic-1" id
  ```
  [code exercise](https://codepen.io/pearl1991/pen/GzPNmP)
  
  ```
  // creating new HTML elements
  var div = document.createElement('div')
  var p = document.createElement('p')
  
  // Adding HTML nodes to the DOM
  var body = document.querySelector('body')
  body.appendChild(p)
  body.appendChild(div)
  
  // replacing text and elements
  p.textContent = "Hello World"
  div.innerHTML = '<span>Hello World</span>'
  ```
  [code exercise](https://codepen.io/pearl1991/pen/QYzGYE)
  * Event Listeners 
  ```
  var btn = document.querySelector('button')
  
  btn.addEventListener('click', function() {
     alert("I've been clicked!")
  })
  ```
  [code exercise](https://codepen.io/pearl1991/pen/XOoNQV)
  
  ## Advanced Eve
