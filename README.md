# Uncommon HTML Bug: Handling Non-Existent Elements

This repository demonstrates a subtle but important bug in HTML:  attempting to manipulate a DOM element that doesn't exist. The code shows the wrong approach and then the corrected solution.  This is particularly relevant when dynamically adding or removing elements, or dealing with asynchronous operations that might not have fully loaded the DOM.

## Bug Description
The `bug.html` file attempts to modify the `innerHTML` of an element ('nonExistentElement') that does not exist in the HTML structure.  This leads to a silent failure; no error is thrown, and the text is not changed. 

## Solution
The `bugSolution.html` demonstrates the correct approach. Before manipulating the element, it checks whether the element exists using `document.getElementById()`, handling the potential absence gracefully. 