#cssWatch.js
This is a fork from darcyclarke's Watch.js project. Please see: https://github.com/darcyclarke/Watch.js for full details.


This plugin lets you listen for when a CSS property, or properties, changes on element. It utilizes `Mutation Observers` to mimic the `DOMAttrModified` (Mutation Events API) and `propertychange` (Internet Explorer) events.

There is both a jQuery-specific plugin as well as a library agnostic version of this plugin available. 

#### jQuery Usage
```javascript

// Watch for width or height changes and log values
$('div').cssWatch('width height', function(){
	console.log(this.style.width, this.style.height);
});
````

#### Default Usage
```javascript

// Watch for width or height changes and log values
var div = document.querySelectorAll('div');
cssWatch( div, 'width height', function(){
	console.log(this.style.width, this.style.height);
});
````

#### Bower Usage
```
bower install ranma2913/cssWatch.js --save
````

#### Dependancies 
This library utilizes the Polymer team's [Mutation Observers](https://github.com/polymer/MutationObservers) and [WeakMap](https://github.com/Polymer/WeakMap) Polyfills. They are included by default which bulks the library a bit. Depending on future usage, I may choose to references these as bower dependancies. 


## License
Copyright (c) 2013 Darcy Clarke  
Dual licensed under the MIT and GPL licenses.  
