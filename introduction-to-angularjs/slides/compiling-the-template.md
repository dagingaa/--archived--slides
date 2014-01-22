##  Compiling the template

````javascript
var $compile = ...; // injected into your code
var scope = {exp: "foo"}; // The JS object which holds our data we want to render
var parent = ...; // DOM element where the compiled template can be appended

var html = '<div ng-bind="exp"></div>'; // The static HTML template as a string

// Step 1: parse HTML into DOM element
var template = angular.element(html);

// Step 2: compile the template
var linkFn = $compile(template);

// Step 3: link the compiled template with the scope.
var element = linkFn(scope);

// Step 4: Append to DOM (optional)
parent.appendChild(element);
````

note:
- The $compile function is injected using dependency injection. It is a
  standard component of Angular.
- The scope is the object that stores all our data
- The parent is where the compiled DOMElement should be appended
- First we need to turn our string into a DOMElement
- This is then our static template which we must compile
- The compile function takes the static template and returns a linking function
- The compile function traverses the DOM and matches directives, custom HTML attributes
    - In this case ng-bind
- Adds the directive to a list of directives that match that element
- Once everything is found, sorts all directives by their priority
- Runs every directives own compile function (useful if your template generates
  or modifes DOM in itself)
- Each compile returns a linking function, which is then combined into one
  linking function and returned
- We call the combined linking function with our scope object, which in turn
  calls every individual linking function.
- Also registers listeners on the elements to keep the data in sync with the
  scope for each directive
