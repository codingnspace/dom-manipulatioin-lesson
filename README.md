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
  
  ## Advanced Topics
  ```
  // 1) Selecting more than one HTML node
  var allDivs = document.querySelectorAll('div') // results in a nodeList of all divs in the HTML document
  
  // Working with nodeList (think of them as arrays)
  // use a for loop to access and individual nodes within the nodeList
  for (var i = 0; i < allDivs.length; i++) {
    allDivs[i].innerHTML = '<p>New Paragraph</p>'
  }
  
  // 2) Removing Elements
  // basic syntax / how to:
  // parentNode.removeChild(childNode)
  
  var body = document.querySelector('body')
  var div = document.querySelector('div)
  
  body.removeChild(div) // removes the div (child) from the body (parent)
  
  // 3) Adding and removing attributes
  // attributes are things like src, class, id, href
  // basic syntax:
  // node.setAttribute('attribute_name', 'new_attribute_value')
  
  btn.setAttribute('class', 'newClass') 
  div.setAttribute('style', 'color: blue; background: white');  
  
  btn.removeAttribute('class') // removes all the classes
  
  // using classList - another alternative
  btn.classList.remove('newClass') // removes single class
  btn.classList.add('anotherNewClass')
  btn.classList.contains('testClass') // returns true or false
  btn.classList.toggle('active') 
  // if btn doesn't have class "active" then add it, or if
  // it does, then remove it
  ```
  [code exercise #1](https://codepen.io/pearl1991/pen/qgLRBJ?editors=1010) | [code exercise #2](https://codepen.io/pearl1991/pen/jdXybB?editors=1010) | [code exercise #3](https://codepen.io/pearl1991/pen/JxwEOz)
