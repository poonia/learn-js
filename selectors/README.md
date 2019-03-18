# Selectors 🏝

 
Different ways to get elements in the DOM using vanila javascript.

## **Generic selector methods**

**querySelectorAll()**

This method is to find all matching elements on a page. You can pass any valid CSS selector.

eg.-

    //Get all elements with the .text-primary class 
     var primaryTextElems = document.querySelectorAll('.text-primary');

    // Get all elements with the [data-counter] at tribute  
    var dataCounterElem = document.querySelectorAll( '[data-counter]');

*Browser Compatibility*
Works in all modern browsers, and IE9 and above.

**querySelector()**
This method is used to find the first matching element on a page. You can pass any valid CSS selector.
eg. -

    // Get first div on the document(using tag selector)
    var elem = document.querySelector('div');
    
    // The first element with the .text-primary class (using class selector)
    var primaryTextElem = document.querySelector('.text-primary');

    // The first element with a data attribute of counter equal to user  
    var dataCounterElem = document.querySelector('[data-counter="user"]');

If an element isn’t found using querySelector(), then it will returns null. You should put check of existent element before using it.

*Browser Compatibility*
Works in all modern browsers, and IE9 and above. Can also be used in IE8 with CSS2.1 selectors but not CSS3.

**matches()**

This method is use to check or match if an element exist with the provided slector or set of selectors. It returns true if the element is a match, and false when it’s not. 
eg.- 

    // Verify element exists before doing anything with it  
    if (document.matches('.text-primary')) {
		document.matches('.text-primary').classList.add('text-bold');
    }

*Browser Compatibility*
Works in all modern browsers, and IE9 and above.


## **Type-specific selector methods**

These methods are elements selector specific type. Like by Id, class, tags, etc.

**getElementById()**
This method  take selector as ID only and as the name says it will get element by their ID. 

**getElementsByName()**
This method returns a NodeList of elements with matching name attributes. 

**getElementsByTagName()**
This method will return `HTMLCollection` (array-like object similar to arguments) of elements with a matching tag name, in the order they appear.   `HTMLCollection`  is empty when no result is found regarding given tag name.

**getElementsByClassName()**
Similar to `getElementsByTagName` , this method also return `HTMLCollection` of the matching class name elements, in the order they appear .


*Browser Compatibility*
Works in all modern browsers, and IE8 and above.

***Note-***
`querySelector()` and `querySelectorAll()` methods can do everything those other methods do and more. But for this you need to be clear whether you need all matching elements or just the first one.


