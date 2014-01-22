##  A closer look at the template
````html
<label>Name:</label>
<input type="text" ng-model="yourName" placeholder="Enter a name here">
<h1>Hello {{yourName}}!</h1>
````

note:
- Uses regular HTML super-powered with new directives to, along with the
  model and controller, renders a view tha the user sees in the browser
- It consists of the static DOM, HTML, CSS and angular specific elements and
  element attributes
- The angular bits direct Angular to transform this static template DOM
  into a dynamic view
- To transform a static template into a dynamic view, Angular must compile it
