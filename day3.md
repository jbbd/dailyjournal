# DAY 3
## Javascript and the DOM

The document is a global object representing the HTML and content of a webpage.

DOM - Document Object Model. The DOM is the representation of a web page.

```javascript
const myHeading = document.getElementsByTagName('h1')[0];
```
document.getElementsByTagName() returns a collection, so you can access the value by the index.

collection - an array-like list of HTML elements (i.e. returned from getElementsByTagName). They cannot use certain Array methods.

Some selectors:
* .getElementById()
* .getElementsByTagName()
* .getElementsByClassName()

And CSS Query Selectors:
* document.querySelectorAll() - returns multiple
* document.querySelector() - returns single

You can get elements by ID, tag name, class name, and attributes with querySelectors: 

```javascript
document.querySelector('li');
document.querySelector('#myHeading');
document.querySelector('.errors');
document.querySelector('[title=label]')
```

* document.textContent - reads and changes text content.
* document.innerHTML - reads and alters elements.

Node - belongs to DOM.
Element - belongs to HTML.

Instead of looping, try using psuedo-selectors to access a node.

Example: 
```javascript
removeItemButton.addEventListener('click', () => {
  let ul = document.getElementsByTagName('ul')[0];
  let li = document.querySelector('li:last-child');
  ul.removeChild(li);

});
```