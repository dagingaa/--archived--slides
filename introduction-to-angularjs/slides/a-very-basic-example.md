##  A very basic example

````html
<div ng-app>
    <label>Name:</label>
    <input type="text" ng-model="yourName" placeholder="Enter a name here">
    <h1>Hello {{yourName}}!</h1>
</div>
````

<div class="example">
    <div ng-app>
        <form>
            <label>Name:</label>
            <input type="text" ng-model="yourName" placeholder="Enter a name here">
        </form>
        <h1>Hello {{yourName}}!</h1>
    </div>
</div>

note:
- Probably the easiest example of using AngularJS
- Demonstrates setting up an app, two-way data binding, directives and scopes
- ng-app
    - Instantiates an Angular application. Multiple can live on the same page
    - Everything inside this DOMElement will be compiled by Angular
    - Looks for directives and data-bindings
    - In this case it finds ng-model directive and a data-binding
- ng-model
    - Takes a string representing a property on a javascript object
    - Angular talks in scopes, so this property is then stored on the scope
    - A scope is not globally accessible
    - The string does not have to be preregistered on the scope
- {{ }}
    - a data-binding that prints whatever is in the scope property yourName
    - Is bound to the scope variable, and will update when it changes
- Now let's dive a little bit deeper into how this actually works

