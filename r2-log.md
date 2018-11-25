# #100DaysOfCode Log – Round 2 – Natalie Cardot

My #100DaysOfCode challenge log. Started August 3, 2018.

## Log

### R2D1

**Today's Progress:** Made a fully styled "cat clicker" app as practice for a lesson on the model-view-controller design pattern.

**Link to Work:** [Cat Clicker](https://nataliecardot.com/cat-clicker-vanilla-js/index.html)

### R2D2

**Today's Progress:** Went through a lesson on promises, brushed up on some basic computer science concepts, and researched dependency management tool options.

### R2D3

**Today's Progress:** Worked through another lesson on promises, with a focus on promise chaining.

### R2D4

**Today's Progress:** Worked through a lesson about Ajax with XHR, which covered how to create an XHR object, its required methods and properties, and how asychronous requests are sent.

### R2D5

**Today's Progress:** Worked through lessons covering Ajax with jQuery and with the Fetch API.

### R2D6

**Today's Progress:** Learned about features of single-page apps, as a prelude to getting into JavaScript frameworks.

### R2D7

**Today's Progress:** Learned about factory functions, the function constructor, regular expressions, and the Backbone.js library.

### R2D8

**Today's Progress:** Finished a lesson on the basic structure of Backbone.js.

### R2D9

**Today's Progress:** Started a lesson providing a conceptual overview of AngularJS.

**Notes:**
* **Module:** container that stores different components of an app
* **Template:**	HTML with additional markup. AngularJS provides templating system that lets you format HTML structure of application (view part of MVC framework architecture that AngularJS uses)
* **Directives:** markers on template that tell AngularJS HTML compiler to attach special behavior to a DOM element.
* **Controller:** where you set up initial state (condition regarding stored inputs) and logic for view (template)
* **Service:** closely tied with controller, contains view-independent logic
* **Model:** data shown to the user in the view and with which the user interacts
* **Scope:** binds template and controller together. When user interacts with template and changes some data, scope watches for this change and updates controller; or if data changes in the controller, template is updated
* **View:** what user sees (DOM)
* **Routing:** uses ngRoute module, which acts based on URL. Captures URL and renders view based on the defined routing rules
* **Example case:** If you had a "save for later" checkbox that should appear on each individual item page and have its own page that lists all items that have been saved, you'd need these components: Because "save for later" will have its own page where customers can view items they've saved for later, a new entry in router is needed. Checkbox will be added to item template (view), but page listing all items will need its own template; new template must be created. Items controller will have new property to track whether saved or not, but save for later page needs controller. Service keeps track of everything.
* **Two-way data binding:** Prized feature of AngularJS. Typically a framework retrieves data and feeds it into template (a one-way info fetch), in a compile step. AngularJS works similarly, but there's another update step: info added, deleted, or change in browser updates underlying data object. In other words, it has live bindings, and whenever input values change, values of expressions are recalculated automatically and DOM is updated accordingly.

### R2D10

**Today's Progress:** Continued a lesson providing a conceptual overview of AngularJS.

**Notes:**

* **Yeomann:** tool for project scaffolding used to quickly generate an entire project's file structure. Not specific to AngularJS but used with generator plugins.
* To create a module, need an array of dependencies. If none, leave brackets blank.
* **Bootstrapping:** In AngularJS this is the equivalent of initializing (starting) your app. One way is with the ng-app directive. The other is, after creating your app with `angular.module("myApp", []);`, do so from the JavaScript with `angular.bootstrap(document, ['myApp']);`.
* **ng-app directive:** in an HTML element tells your AngularJS app two things: that that element contains your application. If you put it in a div rather than the body, it will only be loaded inside that div. Second, it says to load the module with name in quotes, which would be like `angular.module("myApp", []);` in the JavaScript file. For example `<body ng-app="myApp">`
* Templates in AngularJS: plain HTML. Dynamic parts of template are set in a controller, using expressions. Expressions are double curly braces containing variables or simple mathematical operations.

### R2D11

**Today's Progress:** Finished a lesson providing a conceptual overview of AngularJS and started a lesson on Ember.

**Notes:**

###### AngularJS
* **ui-router:** angular-route.js module (that Yeomann gives you option to use when you generate an AngularJS app with `yo angular`) doesn't allow for nested views. Use the community-built routing module ui-router for that. Single-page applications typically have many different views (screens) you can interact with, and a router handles loading them based on the URL. Bower used to install in example, with `bower install -S angular-ui-router`. -S saves ui-router to the Bower config file.

###### Ember

* Dependencies: Git, Node.js, npm (for fetching required Dependencies),  
* Focus is on convention over configuration
* Comes with its own build tool (build tools are programs that automate the creation of executable [able to be run by a computer] applications from source code)
* `ember-cli` (entered into npm CLI), Ember.js command line utility, is recommended by Ember as de facto way to build and develop a new app. Also use to create new template and component files and maintain and update new routes.
* Use `ember-cli` and `ember new <app name>` to generate a new app. ember-new creates new directory, creates initial commit, runs npm install, and built-in server
* `ember serve` starts development server

### R2D12

**Today's Progress:** Finished a lesson on the basic features of Ember.

**Notes:**

* **Components:** like custom HTML elements. Default DOM element of `div`. The functionality (per the default file structure generated with `ember new` command) goes in app/components, while the components HTML file goes in templates/components.
* When an Ember app is loaded, router's job is to match URL against a list of routes. When it finds that route, it loads that route's route file and loads the associated template.
* Use `ember g route <url to match>` to generate a route (`g` is an alias for `generate`). This creates a route file at app/routes/route-name.js, a template for the route at app/templates/route-name.hbs, and a unit test file at tests/unit/routes/route-name-test.js. It also adds the route to the router. Loads data (model) for that route. Can use dynamic data set by route file.
* Ember provides a number of hooks we can use in a route file.
* Ember templates can be thought of as containers (in addition to chunks of standalone HTML). The base container is the application template; it contains all other templates. Sitewide HTML (such as navigation, header, footer) should go in the application template.
* A dynamic segment is a portion of a URL that starts with a : and is followed by an identifier.
* Ember templates are powered by the Handlebars templating language. A Handlebars template is a block of HTML that has Handlebars expressions that look like `{{ brick_color }}`. Handlebars is a standalone templating language that can be used outside of Ember.
* A Service is an Ember object that lives for the duration of an application and can be made available in di  fferent parts of one. Services are useful for features that require shared state or persistent connections, e.g., user/session authentication, geolocation, WebSockets (WebSocket is a protocol for creating a fast two-way channel between a web browser and a server), and third-party APIs (note: an API is a software intermediary that allows two applications to talk to each other).

### R2D13

**Today's Progress:** Began a lesson on the service worker.

**Notes:**
###### Service worker
* Script (JavaScript file) that runs in the background, intercepting requests as the browser makes them, to improve offline experience
* With a service worker you can easily set an app up to use cached assets first, providing a default experience even when offline
* Heavy use of [promises](https://codeburst.io/javascript-learn-promises-f1eaa00c5461) (proxies for a value not necessarily known when promise created, and which can be in one of three states: pending, fulfilled, rejected. It's also settled if it's no longer pending (fulfilled or rejected).
* Requires HTTPS
* As a JavaScript web worker, sits separately from page and can't access DOM directly
* AppCache was previous attempt at addressing network connectivity issues (now deprecated)
* Service worker will control any URL that begins with scope (from the registration URL). Trailing slash is important. If scope is  '/my-app/', URL must begin with /my-app/.
* Add an event listener for a fetch event to add service worker, with self.addEventListener('fetch', function(event) { ... }). Also needs to be registered from the page (or won't work). When a user navigates to a page within your service worker's scope, it controls it. The network request for its HTML goes to the service worker and triggers a fetch event. But you also get a fetch event for every request triggered by that page: CSS, JS, images, etc.
* Cache API provides global caches object. To create or open a cache, use caches.open('my-stuff').then(function(cache) { ... The cache box contains request/response pairs from any secure origin. You can use it to store fonts, scripts, images--just about anything--from our own origin as well as elsewhere on the web.
* Add items using cache.put(request, response), cache.addAll([ '/foo', '/bar' ]) (it's atomic: if any fail to cache, none are added), cache.match(request), or caches.match(request)

### R2D14

**Today's Progress:** Finished a lesson on the service worker.

**Notes:**
###### Service worker
* When to store caches: when a browser runs a service worker for the first time, the install event is fired. Browser won't allow service worker to take control of a webpage till its install phase has completed, and we're in control of what that involves. It's a good opportunity to get everything we need from network and create a cache for it. In service worker file, add event listener for install event. Within the function, use event.waitUntil() (signals progress of install), and pass it a promise. If/when the promise resolves, the browser will know install is complete; if it rejects, it knows install has failed, and service worker should be discarded.
* If you make a change to CSS, the service worker isn't automatically updated. You must make a change to the service worker in order for the browser to treat the updated service worker as a new version. Because it's new, it'll get its own install event, in which it will fetch the JS, HTML, and updated CSS, and place them in a new cache. Must change the name of the cache for it to place in new cache; doesn't do so by itself (make new one; don't want to disrupt preexisting cache already in use by old service worker and pages it controls). Once new service worker is released and ready to take over, we delete old cache, so next page load gets resources from new cache (i.e., updated CSS).
* Activate event: ideal time to discard old caches. Use `caches.delete(cacheName);`
* Use `caches.keys()` to get names of all caches.

### R2D15

**Today's Progress:** Started restaurant reviews app project:
* Forked and cloned project repository
* Reviewed files/rubric

### R2D16

**Today's Progress:** Got restaurant reviews app map working with MapBox access key, made layout responsive and mobile friendly

### R2D17

**Today's Progress:** Made minor restaurant reviews app styling improvements and comment/code cleanup.

### R2D18

**Today's Progress:** Made minor restaurant reviews app styling improvements and comment/code cleanup.

### R2D19

**Today's Progress:** Added ARIA attributes to restaurant reviews app for improved accessibility.

### R2D20

**Today's Progress:**
* Worked on restaurant reviews app by adding ARIA attributes and fixing a minor bug.
* Watched part of a [video](https://www.youtube.com/watch?v=ksXwaWHCW6k&feature=youtu.be) on the service worker for review/preparation to implement it in the project.

**Notes:**
###### Service worker
* Can't directly access the DOM; instead they communicate with the pages it controls by responding to messages sent by the POST message interface, which can manipulate DOM if needed
* Programmable network proxy that allows you to control how network requests from your page are handled
* Terminated when not used, restarted when needed again
* Need HTTPS unless using localhost; if you upload to remote server, ensure it has HTTPS installed and enabled
* In addition to caching assets, used for push notifications, background data sync/preload (new API that lets you defer actions in the cache until user has stable connection [Instagram works like this when offline])
* Lifecycle: register -> install (triggers "install") event -> activate (triggers "activate" event)

### R2D21

**Today's Progress:** Added additional ARIA attributes and a service worker (attempt) to restaurant reviews app.

### R2D22

**Today's Progress:** Continued working on implementing the service worker in restaurant reviews app.

### R2D23

**Today's Progress:** Continued working on implementing the service worker in restaurant reviews app.

### R2D24

**Today's Progress:**
* Got service worker working in restaurant reviews app and submitted the project to Udacity.
* Restyled my cat clicker app and added it to my site
* Added a project placeholder to my site for an improved (more symmetrical) appearance

### R2D25

**Today's Progress:** Fixed some things I missed (section header element order) and resubmitted restaurant reviews app project (it passed!). Also continued restyling my site, including changing the hero image and optimizing its responsiveness.

### R2D26

**Today's Progress:** Finished restyling my site: Made it fully secure by removing the contact form, made the newly added contact information responsive at all breakpoints, and added new favicons.

### R2D27

**Today's Progress:** Started a lesson on React.

**Notes:**
* __Composition__ is combining simple functions together to create complex functions. This is a key way in which React constructs UI.
* __Declarative vs imperative__ programming: Declarative is saying what you want done and leaving the work to another entity, whereas declarative means doing the work. For example, to maintain a comfortable temperature in the car, an imperative method would be fiddling with the knobs continuously, whereas a declarative method would be if you had a voice-activated system to which you could *declare* what temperature you wanted the car to be. You declare state and markup then React does the imperative work of keeping the DOM in sync.

  Declarative: expresses logic of computation without describing its control flow (control flow is order in which individual statements, instructions or function calls of an imperative program are executed or evaluated)
  Imperative: uses statements that change a program's state.

  If you have code with logic that says that if something is red then make it blue, it could be declarative or imperative. If it does so by directly manipulating the DOM, it's imperative. If it simply says it should change the color, and an element is not touched to accomplish this, it's declarative. See more detailed example in [this article](https://codeburst.io/declarative-vs-imperative-programming-a8a7c93d9ad2).

  React is declarative: You declare state and markup, then React does imperative work of keeping the DOM in sync with your app.

* Redux is an open-source JavaScript library for managing application state--a "predictable state container." Stated differently, it helps you manage the data you display and how you respond to user actions.

* Routing is the process of selecting a path for traffic in a network

### R2D28

**Today's Progress:** Contined a lesson on React.

**Notes:** Whereas front-end frameworks like Angular and Ember use two-way data binding (if a model changes the data, data updates in the view; alternatively, if the user changes the data in the view, then the data is updated in the model), React has a unidirectional data flow: down the "tree" from the parent component to a child component.

### R2D29

**Today's Progress:** Finished an introductory lesson on React and got a refresher on the .map() and .filter() methods, which are heavily used in React.

### R2D30

**Today's Progress:** Started lesson on rendering UI with React.

**Notes:**
* To describe UI, React uses elements rather than templates.
* React's .createElement() method takes in a description of an element and returns a plain JavaScript object. `React.createElement( /* type */, /* props */, /* content */ );` Created elements describe DOM nodes, not HTML. When HTML is parsed by browser into DOM, the HTML “element” is called object or node, and HTML attributes become properties of the object/node. When passing properties into createElement(), use DOM property name, e.g., className instead of class.
* In React the process of deciding what to render is completely decoupled from actually rendering it; the decoupling makes it possible to render things on the server, VR environments
* ReactDOM is the glue between React and the DOM. Its single use is the ReactDOM.render() method to render our element onto a particular area of a page. You can render an element into a DOM node called root. Apps built with React typically have a single root DOM node. For example, an HTML file may contain a <div> with the following: `<div id='root'></div>` By passing this DOM node into getElementById(), React will end up controlling the entirety of its contents.
* VirtualDOM: When using React's createElement() method, real elements aren't being created; rather, they're objects that describe real DOM nodes. To create something in the DOM with createElement(), must render it using  ReactDOM.render().

### R2D31

**Today's Progress:** Continued lesson on rendering UI with React.

**Notes:**
* React.createElement( type, props, content); creates a single React element of a particular type. We'd normally pass in a tag such as a div or span to represent that type, but the content argument can be another React element.  However, even when .createElement() there are nested elements, it returns just one root element.
* JSX is a sytax extension to JavaScript that allows us to write JavaScript code that looks more like HTML, which makes describing the nested relationships of elements more simplistic and elegant than many createElement() calls. It is similar to XML, Extensible Markup Language, which is a markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable. XML was designed to store and transport data and to be self-descriptive. (A markup language is a system for annotating a document in a way that is syntactically distinguishable from the text.)
* Whenever you want JSX to evaluate JavaScript, must wrap it in curly braces.
* React component:

  A single view of a user interface (in this case the way through which a user interacts with an application or a website), the 'tree' or 'trunk', is divided into logical chunks, such as branches. The tree becomes the starting component (e.g., a layout component) and each chunk in the UI will become a subcomponent that can be divided further into subcomponents (that is, subbranches).

  React provides a base component class that we can use to group many elements together and use them as if they were one element.

  Components refer to reusable pieces of code ultimately responsible for returning HTML to be rendered onto the page. They are like factories used to create React elements--by creating custom components (or classes), we can easily generate custom elements. Formatted like:

  ```javascript
  // reminder: Pascal case is used for class and constructor names
  class ContactList extends React.component {
  // Only method required in a class is render(). It is render's jobto return the JSX or the elements that that component renders
    render() {
      const people = [
        { name: 'Mike' },
        { name: 'Stacey' },
        { name: 'Trish' }
      ]

    return <ol>
      {people.map(person => (
        <li key={person.name}>{person.name}</li>
      ))}
      </ol>
    }
  }
  ```

  Since React's main focus is to streamline building app's UI, there is only one method that is vital in any React component class: render().

  A React component is basically any part of a UI that can contain React nodes (via React.createElement() or JSX).

  Think of component classes as factories that produce instances of components. These component classes should follow the single responsibility principle and manage only one task.

### R2D32

**Today's Progress:** Continued lesson on rendering UI with React.

**Notes:**
* Create React App installs the packages react, react-dom, and react-scripts. react-scripts installs Babel (so can use latest JS syntax and JSX), webpack (to generate the build), and webpack-dev-server, which provides auto-reload behavior.
* Webpack's main purpose is to bundle JavaScript files for usage in a browser. It is a module bundler. A module is a reusable piece of code that encapsulates implementation details and exposes a public API so it can be easily loaded and used by other code. Stated differently, a module is an object referring to the functionality that will be exported from a file. Or, a module can be thought of as a container that holds related code which can then be exported to another file.

### R2D33

**Today's Progress:** Optimized both of my to-do list projects for mobile and added mobile and tablet incompatibility messages for my two pixel art maker versions.

### R2D34

**Today's Progress:** Futher optimized media query styling for my arcade game project and started Codecademy's React course.

**Notes:**
* Positioning is static by default; for top, left, etc., to work in CSS, you need to set position to relative.
* To vertically center without flexbox, one way is to wrap everything you want to center in a div (if there are multiple items, such as an img and p element) set top to 50%, set position to relative, and use transform: translateY: -50%;
* Another way to vertically center is to set the enclosing parent element (such as a div) to display: table, and set the child element (such as a p element) to display: table-cell, with vertical-align: middle. Margins won't work with this; instead you can use padding (one possibility).
* Multi-line JSX must be enclosed in parentheses and there can only be one outermost element. An easy solution is to wrap everything in a div.
* If you try to render a JSX element twice, and it's the same in both instances, nothing will happen; it only renders elements that have changed.
* A key feature of React is the virtual DOM. In React, for every DOM object, there is a corresponding virtual DOM object, a representation of a DOM object, like a lightweight copy. It has the same properties as a real DOM object, but unlike the real thing, it cannot directly change what's on screen. Real DOM manipulation is slow, but since manipulating the virtual DOM does not draw anything on the screen, it's much faster. Manipulating the virtual DOM is like editing a blueprint of a home's layout, as opposed to moving rooms within it. When a JSX element is rendered, every virtual DOM object is updated, with little efficiency cost because it updates so quickly. Once React knows which virtual DOM objects have changed, then React updates those objects, and those objects alone, on the real DOM. This is the reason for React's reputation for performance.
* With JSX, must use className instead of class atttribute name because JSX gets translated into JavaScript, and class is a reserved word in JavaScript. When JSX is rendered, JSX className attributes are automatically rendered as class attributes.
* JSX element and rendering example:
```javascript
const myDiv = <div className="big">I AM A BIG DIV</div>;

ReactDOM.render(myDiv,
document.getElementById('app'));
```
* When you write a self-closing tag in HTML, it is optional to include a forward-slash immediately before the final angle-bracket, but it is required with JSX.
* Any code between the tags of a JSX element will be read as JSX, not as regular JavaScript! To treat text between JSX tags as ordinary JavaScript, wrap it in curly braces.

### R2D35

**Today's Progress:** Contined Codecademy's React course.

**Notes:**
* When you insert JavaScript into JSX, it's part of the same environment as the rest of the JavaScript in your file; you can access variables from inside of a JSX expression even if those variables were declared on the outside.
* It's common to use variables to set attributes when writing JSX. Put each attribute on its own line for readability. Object properties are also often used to set attributes.
* JSX elements can have event listeners like HTML elements can. You can create an event listener by giving a JSX element a special attribute, such as `<img onClick={myFunc} />` or `<button onClick={yo}></button>`, where `yo` is a previously defined variable. See React's [supported events](https://reactjs.org/docs/events.html#supported-events) (remember capturing is synonymous with trickling).
* If statements cannot be used in JSX expressions because JSX is just syntactic sugar for JavaScript function calls & object construction, and when it's compiled to JavaScript, the if statements don't fit in, as explained [here](https://react-cn.github.io/react/tips/if-else-in-JSX.html). A common way to include conditionals is to place them outside of the JSX tags.
* Ternary operator can be used between JSX tags. Example:

  ```javascript
  const headline = (
    <h1>
      { age >= drinkingAge ? 'Buy Drink' : 'Do Teen Stuff' }
    </h1>
  );
  ```

* Map is best for creating lists of JSX elements. Example:

  ```javascript
  const strings = ['Home', 'Shop', 'About Me'];

  const listItems = strings.map(string => <li>{string}</li>);

  <ul>{listItems}</ul>
  ```

  Note: {listItems} will evaluate to an array because it's the returned value of .map()--JSX `<li>`s don't have to be in an array, but they can be.

* JSX attribute key is used to keep track of lists. Example: `<li key="li-01">Example1</li>` A list needs key if 1) when a list is rendered, whether a list item was checked off or not needs to be "remembered" (as is the case with a to-do list), and 2) a list's order might be shuffled
* React applications are comprised of components. A component is a small, reusable chunk of code that is responsible for one job, which is often to render some HTML. Example of code that creates and renders a component:

  ```javascript
  // Importing React library and saving it to a variable named 'React'
  import React from 'react'; // Methods used for pure React purposes (e.g., components, writing JSX elements)
  import ReactDOM from 'react-dom'; // Methods for interacting with the DOM

  class MyComponentClass extends React.Component {
    render() {
      return <h1>Hello world</h1>;
    }
  };

  ReactDOM.render(
    <MyComponentClass />,
    document.getElementById('app')
  );
  ```

* Every component must come from a component class, which is like a factory that creates components. To make a component class, use a base class from the React library: React.Component, which is a JavaScript class. To create your own component class, you subclass that React.Component base class. To do so, use the syntax `class YourComponentNameGoesHere extends React.Component {}`.
* A component class is like a factory that builds components, which it builds by consulting a set of instructions, which must be provided between the curly braces in ES6 class syntax. The only required property to include is the render() method (the property's name is render, and its value is a function). The render method (referring to either the entire property or the function part alone) must contain a return statement.
* To make a React component, you write a JSX element, giving it the same name as a component class. JSX elements can be either HTML-like or component instances; JSX uses capitalization to distinguish between the two, which is why you must use Pascal case for the component class name. Here's an example of an instance of a component class: `<MyComponentClass />`
* Whenever you make a component (an instance if the component class), that component inherits all of the methods of its component class. MyComponentClass has the method MyComponentClass.render(); <MyComponentClass /> also has a method named render.
* To call a component's render method, you pass that component as a first argument to ReactDOM.render():

  ```javascript
  ReactDOM.render(
    <MyComponentClass />,
    document.getElementById('app')
  );
  ```

  This instructs the component instance to call _its_ render method.

* A render method must contain a return statement, but it also is a good place for any simple calculations that need to happen right before a component renders. This logic must be within the render method's curly braces. Example:
```javascript
class Random extends React.Component {
  render() {
    const n = Math.floor(Math.random() * 10 + 1);
    return <h1>The number is {n}!</h1>;
  }
}
```
* To use a conditional inside a render() function, it must be before the return statement.
* The `this` keyword is often used in the body of component class declarations. The simple explanation of what it refers to is an instance of the component class (actually, this is almost always the case, but it could technically be something else). The more complex explanation is that it refers to the object on which this's enclosing method, in this case .render(), is called:
```javascript
class IceCreamGuy extends React.Component {
  get food() {
    return 'ice cream';
  }

  render() {
    return <h1>I like {this.food}.</h1>;
  }
}
```
* Reminder: The set syntax binds an object property to a function to be called when there is an attempt to set that property. The get syntax binds an object property to a function that will be called when that property is looked up.
* Reminder: An event handler is a function that gets called in response to an event.

### R2D36

**Today's Progress:** Continued Codecademy's React course.

**Notes:**
* In React, you define event handlers as methods on a component class.
* "Component instance," "React component," and "component" are synonymous, while component class is not (it's like a factory for making components).
* In addition to HTML-like JSX elements, render methods can also return another kind of JSX: component instances. Example:
```javascript
class OMG extends React.Component {
  render() {
    return <h1>Whooaa!</h1>;
  }
}

class Crazy extends React.Component {
  render() {
    return <OMG />;
  }
}
```
* One component can render another component by placing it (the component instance) in its render function. But since when you're using React.js, every JavaScript file in your application is invisible to every other JavaScript file by default, you have to import the variable if it has been declared in another file with an import statement: `import { NavBar } from './NavBar.js';`
* React's module system comes from ES6. This behavior is not specific to React.
* A module is a piece of a program that specifies which other pieces it relies on and which functionality it provides for other modules to use (called its interface). The relations between modules are called dependences. To separate modules this way, each needs its own private scope.
* A package is a chunk of code that can be distributed (copied and installed). It may contain one or more modules and has information about which other packages it depends on.
* NPM is two things: an online service where one can download (and upload) packages and a program (bundled with Node.js) that helps you install and manage them.
* JavaScript execution in Node.js is single threaded. In computer programming, single threading is the processing of one command at a time. The opposite of single threading is multithreading. Node.js uses multiple threads in the background to execute asynchronous code. "Blocking" methods are those that execute synchronously while "nonblocking" methods execute asynchronously---Node.js is _nonblocking_; all functions (callbacks) are delegated to the event loop and they are (or can be) executed by different threads.
* In computing, input/output or I/O (or, informally, io or IO) is the communication between an information processing system, such as a computer, and the outside world, possibly a human or another information processing system.
* Node Package Manager (NPM) provides two main functionalities:
  - Online repositories for node.js packages/modules, which are searchable on search.nodejs.org
  - Command line utility to install Node.js packages, do version management and dependency management of Node.js packages.

  NPM helps JavaScript developers load dependencies effectively. To load dependencies we just have to run this command in command prompt:

  `npm install`

  This locates a JSON file named as package.json in the root directory and installs all dependencies defined within it.
* When you import a variable from a file that is not the current file, then an import statement isn't quite enough. You also need an export statement, written in the other file, exporting the variable that you hope to grab. There are a few different ways to use export. To do a named export: In one file, place the keyword `export` immediately before something that you want to export. That something can be any top-level `var`, `let`, `const`, function, or class. When you use named exports, you always need to wrap your imported names in curly braces, such as:

  `import { faveManifestos, alsoRan } from './Manifestos';`

### R2D37

**Today's Progress:** Continued Codecademy's React course.

**Notes:**
* A component can pass information to another component. Information that gets passed from one component to another is known as "props."
* Every component has something called a props object.
* To see a component's props object, you use `this.props`.
* Reminder: `JSON.parse()` takes a JSON string and transforms it into a JavaScript object. `JSON.stringify()` takes a JavaScript object and transforms it into a JSON string. (When sending data to a web server, the data has to be a string.)
* To pass props to a component (again, this means component instance, not component class), you give it an attribute of any name you wish.

  Example: `<MyComponent foo="bar" />`

  If you want to pass information that isn't a string, then wrap that information in curly braces. Here's how you would pass an array:

  `<Greeting myInfo={["top", "secret", "lol"]} />`

* To make a component display passed-in information: 1) Find the component class that is going to receive that information. 2) Include `this.props.name-of-information` in that component class's render method's return statement. Example:

  ```javascript
  class Greeting extends React.Component {
    render() {
      return <h1>Hi there, {this.props.firstName}!</h1>;
    }
  }
  ```

* `props` could refer to two pieces of passed-in information or it could refer to the object that stores those pieces of information.
* The most common use of `props` is to pass information to a component from a different component.
* It is common to pass functions, especially event handler functions, as props.
* You define an event handler as a method on the component class, just like the render method.

### R2D38

**Today's Progress:** Continued Codecademy's React course.

**Notes:**
* To pass a method defined on a component class to another component (that is, a component instance), you pass it as a prop. Give the component in the render method an attribute and value. The attribute can have any name. The value would use `this` and curly braces. Example:

  ```javascript
  import React from 'react';
  import ReactDOM from 'react-dom';
  import { Button } from './Button';

  class Talker extends React.Component {
    talk() {
      let speech = '';
      for (let i = 0; i < 10000; i++) {
        speech += 'blah ';
      }
      alert(speech);
    }

    render() {
      return <Button talk={this.talk} />;
    }
  }

  ReactDOM.render(
    <Talker />,
    document.getElementById('app')
  );  
  ```

  However, for the method to be called, you must attach it to the event recipient (in this example, a button) as an event handler. Give the JSX element a special attribute name like `onClick` or `onHover` with an attribute value of the event handler (the method).

  Example (goes with previous one):

  ```javascript
  import React from 'react';

  export class Button extends React.Component {
    render() {
      return (
        <button onClick={this.props.talk}>
          Click me!
        </button>
      );
    }
  }
  ```

### R2D39

**Today's Progress:** Continued Codecademy's React course.
* When you pass an event handler as a prop, there are two names that you have to choose: the name of the event handler itself, which should be (per the convention) something like `handleClick` if you're listening for a keypress event, and the prop name, which should be something like the word "on" plus the event type, like "onKeypress" if you're listening for a keypress event.

### R2D40

**Today's Progress:** Continued Codecademy's React course.

**Notes:**
* Every component's props object has a property named children. `this.props.children` returns everything between a component's opening and closing JSX tags.
*  Components often have self-closing tags, such as `<MyComponentClass />`. but you could write `<MyComponentClass></MyComponentClass>`, and it would still work. `this.props.children` would return everything between `<MyComponentClass>` and `</MyComponentClass>`.
* You can display a default message by giving your component class a property called defaultProps, which should be set to equal an object, inside of which object you can set properties. Example:

  ```javascript
  class Example extends React.Component {
    render() {
      return <h1>{this.props.text}</h1>;
    }
  }

  Example.defaultProps = { text: 'Crickets chirping.' };
  ```

* Dynamic information is info that can change.
* A component can obtain dynamic info from props and state.
* State represents mutable data that ultimately affects what is rendered on the page.
* Whereas props are passed in from the outside, a component is given the state property and manages the state internally. It can be declared in a constructor method, or directly in the class, as a class field that isn't supported in JS yet but can be used thanks to Babel's transpiling.
* When defining a component's initial state, avoid initializing it with props; state will only be initialized with props when the component is first created. This is an anti-pattern (a pattern that may be commonly used but is ineffective or error prone).

### R2D41

**Today's Progress:** Worked through a Udacity lesson on state management in React.

**Notes:**
* If your component doesn't keep track of internal state (it only has a render() method), you can declare it as a stateless functional component. Stateless functional components usually have props passed to them.
To access these props, give your stateless functional component a parameter. This parameter will automatically be equal to the component's `props` object.
It's customary to name this parameter `props`.  Example (ES6 arrow function with implicit return).

  ```javascript
  const Email = (props) => (
    <div>
      {props.text}
    </div>
  );
  ```

* _**Reconciliation**_ is the process through which React updates the DOM. When a component's state changes, React must calculate if it's necessary to update the DOM, which it does by creating a virtual DOM and comparing it with the current DOM.
* You can't update state directly (e.g., `this.state.username = 'Natalie'`), because React won't know it changed. To solve this problem, React provides helper method setState (`this.setState()`) Two ways to use it. The first is passing it a function, with previous state passed in as its first argument (in this case, the state update would be asynchronous). _Use functional setState when the new state of your component depends on previous state._

  ```javascript
  this.setState((prevState) => ({
    count: prevState.count + 1
  }))
  ```

  The second way to use setState is to pass in an object, which will be merged with current state to form the new state of the component. _Use object setState whenever the new state of your component does not depend on its previous state._

  ```javascript
  this.setState({
    subject: 'Hello! This is a new subject'
  })
  ```

* Whenever you invoke `setState()`, React rerenders entire application (also calls render() with new state) and updates UI; UI is a function of state.
* If the initial state of a component contains multiple properties, they can be independently updated with `this.setState()`.

### R2D42

**Today's Progress:** Worked through a Udacity lesson on state management in React.

**Notes:**
* PropTypes package allows you to define an intended data type and warns during development if a prop passed to a component doesn't match what's expected. Use `npm install prop-types` or, if using Yarn to manage packages, `yarn add prop-types`. After running either command restart the server with `npm start` (an alias for `npm run start`).
* Normally when using forms in a web app, form state lives in the DOM, but the whole point of React is to more effectively manage state within your application; if form state typically lives within DOM, but React is about state management, how do we handle forms in React? With what React calls "controlled components." _Controlled components_ are components that render a form, but the source of truth for that form's state resides inside the component rather than inside the DOM. They're called controlled components because React is controlling the state of a form. Benefits of controlled components include support for instant input validation, allowing you to conditionally enable or disable form buttons, and enforcement of input formats. Example of controlled component usage:

  ```javascript
  class NameForm extends React.Component {
    state = { email: '' }
    handleChange = event => {
      this.setState({email: event.target.value})
    }
    render() {
      return (
        <form>
          <input type = "text" value={this.state.email} onChange={this.handleChange} />
        </form>
      )
    }
  }
  ```

* The Chrome extension React Developer Tools (from Facebook) allows you to inspect your component hierarchy along with their respective props and states.
* _When to use a controlled component:_ If you want form data to update UI in any way besides just updating input field itself, make the form a controlled component---where React is controlling the state of the input field. (For example, when you have a search contacts feature [contacts added with form])
* String.prototype.match(): match() method retrieves the matches when matching a string against a regular expression.
* Controlled component: a component that renders a form, but the source of truth for that form lives in a component rather than in the DOM. Controlled components unique benefit (as compared to uncontrolled components): they allow you to update UI based on form itself, since form state lives inside the component
* If you're accessing from this.props and/or this.state frequently, you can simplify with [object destructuring](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Object_destructuring). For instance instead of using this.state.query you can use const { query } = this.state, and just use query where you reference it.
* Reminder:  All values in JavaScript are truthy unless they are defined as falsy (i.e., except for false, 0, "", null, undefined, and NaN).
* With controlled components:
  - Each update to state has an associated handler function
  - Form elements receive their current value via an attribute
  - Form input values are stored in component's state
  - Event handlers for controlled element update component's state
* render() is for rendering only; don't place AJAX request (reminder: XHR and fetch are both types of AJAX requests, and fetch is superior because it uses promises and therefore has a more succint, simple syntax) inside of it.
* Lifecycle events are special methods each component can have that allow us to hook into different points in a component's life to run some code. These methods include:
  - componentWillMount: invoked immediately before component is inserted into DOM
  - componentDidMount: invoked immediately after component is inserted into DOM
  - componentWillUnmount: invoked immediately before a component is removed from the DOM
  - componentWillReceiveProps: will be invoked whenever component is about to receive new props
* To fetch or do an Ajax request for remote data (from a database), use componentDidMount(), which  is invoked immediately after a component is mounted. Initialization that requires DOM nodes should go here. If you need to load data from a remote endpoint, this is a good place to instantiate the network request. Setting state in this method will trigger a re-rendering.
* The render() method should be a "pure function"; it should take input via props, return a description of your UI (JSX), and nothing else. You shouldn't make Ajax requests in the render method for this reason and because you don't have complete control over when the render() method will be invoked.
* Typical site (non-single-page application): When user visits it, browser requests a page from site's server. Server generates HTML and returns it. Each time user navigates site, broswer requests new page from server, and server again returns HTML for it. Using JS to render UI is sometimes calle da single-page application. Single-page application doesn't mean there's only one page in the app; it means the browser doesn't need to go back to the server for new pages; instead, JavaScript can handle the transition between them. There's only a single, initial page sent from server.
* React Router is a tool used to create a single-page app with a router. It is a collection of navigational components that compose declaratively with your application.

### R2D43

**Today's Progress:** Started Udacity Project 6, a React app and continued Codecademy's React course.

**Notes:**
* React components always have to call super in their constructors to be set up properly. Example with initial state also set in the constructor:

  ```javascript
  constructor(props) {
    super(props);
    this.state = { mood: 'decent' };
  }
  ```

* Reminder: Never separate methods within a class with a comma, as to distinguish between classes and object literals.
* To read a component's state, use the expression `this.state.name-of-property`.
* By default, `npm install` will install all modules that are listed as dependencies (that satisfy version specifications) in package.json (refer to R2D32 notes for a reminder of what a module is) into node_modules (if it doesn't exist in the current directory, npm adds it). You can hide node_modules from view (from the working directory, that is) and tell Git not to track it by adding it to .gitignore file.
* package-lock.json automatically created for any operations where npm modifies either the node_modules tree or package.json. One of its purposes as described in [npm documentation](https://docs.npmjs.com/files/package-lock.json) is to "describe a single representation of a dependency tree such that teammates, deployments, and continuous integration are guaranteed to install exactly the same dependencies."
* Semantic versioning (semver): You can give npm permission to install a newer patch release with tilde and a minor release with caret in package.json. See [this article](https://bytearcher.com/articles/semver-explained-why-theres-a-caret-in-my-package-json/) and [npm's article](https://docs.npmjs.com/getting-started/semantic-versioning) for further details.

### R2D44

**Today's Progress:** Continued React app project.

**Notes:**
* "A floating action button (FAB) performs the primary, or most common, action on a screen. It appears in front of all screen content, typically as a circular shape with an icon in its center." See [this page](https://material-ui.com/demos/buttons/) for more on FABs.

### R2D45

**Today's Progress:** Continued React app project.

### R2D46

**Today's Progress:** Continued React app project.

**Notes:**
* With 2017 release of npm 5, creation of a package.json file and the `--save`  command (which adds dependencies to package.json) became the default when running `npm install`. Before then, packages were installed with `npm install`, but dependencies weren't added to package.json; `--save` was needed to add them to it. See https://stackoverflow.com/questions/19578796/what-is-the-save-option-for-npm-install

### R2D47

**Today's Progress:** Continued React app project.

**Notes:**
* Parsing JSON with `response.json()` means converting the string received by the web server into a JSON object. (Encoding JSON is the opposite of parsing it.)

### R2D48

**Today's Progress:** Continued React app project.

### R2D49

**Today's Progress:** Started neighborhood maps React app project (project 7 for my nanodegree, the last one).

**Notes:**
* "Build tools are programs that automate the creation of executable applications from source code. Building incorporates compiling, linking and packaging the code into a usable or executable form. In small projects, developers will often manually invoke the build process. This is not practical for larger projects, where it is very hard to keep track of what needs to be built, in what sequence and what dependencies there are in the building process. Using an automation tool allows the build process to be more consistent." (From [techopedia](https://www.techopedia.com/definition/16359/build-tool))
* "`npm run build` does nothing unless you specify what "build" does in your package.json file. It lets you perform any necessary building/prep tasks for your project, prior to it being used in another project." From [SO](https://stackoverflow.com/questions/43664200/what-is-the-difference-between-npm-install-and-npm-run-build)

### R2D50

**Today's Progress:** Continued neighborhood maps React app project.

### R2D51

**Today's Progress:** Continued neighborhood maps React app project. Worked on implementing Foursquare's API to get venue details.

**Notes:**
* Hypertext is a word, phrase or chunk of text that can be linked to another document or text.
* The Hypertext Transfer Protocol (HTTP) is designed to enable communications between clients (such as web browsers) and servers (such as an application on a computer that hosts website).
* HTTP methods: GET, POST, PUT, HEAD, DELETE, PATCH, OPTIONS
* GET method: used to request data from a certain resource. The query string (name/value pairs) is sent in the URL of a GET request. Default fetch HTTP method.
* HEAD method: almost identical to GET, but without the response body.
* POST and PUT methods: both used to send data to a server to create or update a resource. The difference between POST and PUT is that PUT requests are idempotent (can be applied multiple times without changing the result beyond the initial application)---calling the same PUT request multiple times will always produce the same result, whereas calling a POST request repeatedly might have side effects from creating the same resource multiple times.
* `get`: (getter) get syntax binds an object property to a function that will be called when that property is looked up
* `set`: (setter) set syntax binds an object property to a function to be called when there is an attempt to set that property.

### R2D52

**Today's Progress:** Continued neighborhood maps React app project. Added map with Google Maps API and fixed Foursquare API component code. (Both now functional.)

### R2D53

**Today's Progress:** Continued neighborhood maps React app project. Cleaned up Foursquare Places API fetch request code.

### R2D54

**Today's Progress:** Continued neighborhood maps React app project. Added markers to the map.

### R2D55

**Today's Progress:** Continued neighborhood maps React app project. Started implementing markers' info windows.

### R2D56

**Today's Progress:** Continued neighborhood maps React app project. Finished implementing markers' info windows.

### R2D57

**Today's Progress:** Continued neighborhood maps React app project. Started creating a sidebar.

**Notes:**
* These will bypass an if block: false, falsy values null, undefined, 0, NaN, an empty string. See [MDN](https://developer.mozilla.org/en-US/docs/Glossary/Falsy#Examples) and [SO](https://stackoverflow.com/questions/5113374/javascript-check-if-variable-exists-is-defined-initialized).

### R2D58

**Today's Progress:** Continued neighborhood maps React app project. Continued creating a sidebar.

**Notes:**
* It's a good idea to use round brackets for a React return statement to avoid problems due to automatic semicolon insertion. If you place your opening round bracket on the same line as return (`return (`), no semicolon can be automatically inserted until that bracket is closed.

### R2D59

**Today's Progress:** Continued neighborhood maps React app project. Added search capability to the sidebar.

### R2D60

**Today's Progress:** Continued neighborhood maps React app project. Added an animation for markers, added ARIA roles and tabindex values, and deployed the project to GitHub Pages.

### R2D61

**Today's Progress:** Finished and submitted my neighborhood maps React app project.

### R2D62

**Today's Progress:** Added some finishing touches my neighborhood maps React app project. It was accepted; I graduated from the Udacity Front-End Nanodegree program today!

### R2D63

**Today's Progress:** Deployed my restaurant reviews app and cleaned up its CSS.

### R2D64

**Today's Progress:** Added my last three projects to my portfolio site.

### R2D65

**Today's Progress:** Finished Codecademy's Learn ReactJS: Part I course, and started Learn ReactJS: Part II.

**Notes:**
* In React, since class methods are not bound by default in JavaScript, whenever you define an event handler that uses `this`, you need to add `this.methodName = this.methodName.bind(this)` to your constructor function. The [React docs](https://reactjs.org/docs/handling-events.html) state "Generally, if you refer to a method without () after it, such as onClick={this.handleClick}, you should bind that method."
* `this.setState` automatically calls render. That's why you can't call `this.setState()`` from inside of the ``.render()` method; it would create an infinite loop.
* "Stateful" describes any component that has a state property; "stateless" describes any component that does not.
* For a component to pass props to another component, it has to render it, and in the component receiving the prop, it needs to use `this.props.name-of-prop`
* A component should never update this.props. `props` and `state` store dynamic information. Dynamic information can change, by definition. If a component can't change its `props`, then what are `props` for? A React component should use `props` to store information that can be changed, but can only be changed by a _different_ component. A React component should use `state` to store information that the component _itself_ can change.
* A child component can update a parent component's state.
1. The parent component class defines a method that calls this.setState().
2. The parent component binds the newly defined method to the current instance of the component in its constructor. This ensures that when we pass the method to the child component, it will still update the parent component.
3. Once the parent has defined a method that updates its state and binds this to it in the constructor, the parent then passes that method down to a child. For example, in the return statement of the render method, `<ChildClass onClick={this.handleClick} />`
4. The child receives the passed-down function, and uses it as an event handler.
* See [this Codecademy's summary](https://www.codecademy.com/courses/react-102/lessons/child-updates-sibling/exercises/stateless-inherit-stateful-recap?action=resume_content_item) of the steps for a stateless component to inherit from a stateful component.
* Inline styles (styles written as JSX element attributes) in React have double curly braces. The outer ones inject JavaScript into JSX, while the inner ones create an object literal.
* If you want to use more than a few styles, a nice alternative to inline styles is to store the styles in a variable and inject it into JSX.
* In React, style property names are camelCase.
* In React, if you write a style value as a number, then the unit "px" is assumed; if you want a font size of 30px, you can simply write `{ fontSize: 30 }`

### R2D66

**Today's Progress:** Continued Codecademy's Learn ReactJS: Part II.

**Notes:**
* Separate presentational components from business/container/display components: In this programming pattern, the container component does the work of figuring out what to display. The presentational component does the work of actually displaying it. If a component does a significant amount of work in both areas, then that's a sign that you should use this pattern See [this Medium article](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0) for more details on this React programming pattern.
* In addition to validation, propTypes is also useful for documentation--to quickly understand what's inside a component.
* propTypes usage example (note capitalization discrepancy, abbreviation of `bool` and `func`):

  ```javascript
  Runner.propTypes = {
  message:   React.PropTypes.string.isRequired,
  style:     React.PropTypes.object.isRequired,
  isMetric:  React.PropTypes.bool.isRequired,
  miles:     React.PropTypes.number.isRequired,
  milesToKM: React.PropTypes.func.isRequired,
  races:     React.PropTypes.array.isRequired
  };
  ```

### R2D67

**Today's Progress:** Continued Codecademy's Learn ReactJS: Part II.

**Notes:**
* A traditional form doesn't update the server until a user hits "submit," but you want to update the server any time a user enters or deletes any character. Use onChange with an event handler method. Example (note value attribute--this is so what appears in input field matches what `this.state.userInput` is set to [which is an empy string in this case])

  ```javascript
  import React from 'react';

  export class Example extends React.Component {
  	constructor(props) {
  		super(props);

  		this.state = { userInput: '' };

  		this.handleChange = this.handleChange.bind(this);
  	}

  	handleChange(e) {
  	  this.setState({
  	    userInput: e.target.value
  	  });
  	}

  	render() {
  	  return (
  	    <div>
          <input
    	      onChange={this.handleChange}
            value={this.state.userInput}
    	      type="text"
          />
          <h1>{this.state.userInput}</h1>
        </div>
  	  );
  	}
  }
  ```
* Reminder: when using this.setState, a component needs to have an initial state set.
* From earlier: "Controlled components are components that render a form, but the source of truth for that form's state resides inside the component rather than inside the DOM. They're called controlled components because React is controlling the state of a form." Codecademy also says "An uncontrolled component is a component that maintains its own internal state. A controlled component is a component that does not maintain any internal state. Since a controlled component has no state, it must be controlled by someone else."
* Normally an input element keeps track of its own state, making it an uncontrolled component. Example of getting what's entered from the input with JavaScript:

  ```javascript
  let input = document.querySelector('input[type="text"]');
  let typedText = input.value;
  ```
* A controlled component has no memory. If you ask it for information about itself, it must obtain that information through `props`.
In React, when you give an `<input />` a `value` attribute, it _becomes_ controlled and stops using its internal storage.
* Often, you don't need a form or submit eflement; only an input element, since React rerenders on each character change.
* There are three categories of lifecycle methods: mounting, updating, and unmounting. A component mounts when it renders for the first time. Mounting lifecycle methods, in order: 1. componentWillMount 2. render 3. componentDidMount
* Mounting lifecycle events only execute the first time that a component renders.
* You can call `this.setState` from within `componentWillMount`.

### R2D68

**Today's Progress:** Continued Codecademy's Learn ReactJS: Part II.

**Notes:**
* If you need to do something only the first time that a component renders, it's probably a job for a mounting lifecycle method.
* `render` belongs to two categories: mounting lifecycle methods and updating lifecycle methods
* When a component renders for the first time, `componentDidMount` gets called immediately after the HTML from render has finished loading.

### R2D69

**Today's Progress:** Continued Codecademy's Learn ReactJS: Part II.

**Notes:**
* Updating methods (called in order whenever a component instance updates [a component updates every time that it renders, **starting with the second render**]):
1. `componentWillReceiveProps` - called before (2nd and subsequent) rendering begins, and only if component will receive props. Automatically passed one argument: `nextProps`, a preview of the upcoming `props` object that the component is about to receive. A common use of this method is comparing incoming props to current props or state, and deciding what to render based on that comparison.
2. `shouldComponentUpdate` - gets called after `componentWillReceiveProps`, but still before the rendering begins. If `shouldComponentUpdate` returns `true`, nothing noticeable happens, but if it returns false, the component will not update and none of the remaining lifecycle methods for that updating period will be called, including `render`. Receives two arguments: `nextProps` and `nextState`, which are usually compared to the current `this.props` and `this.state`, using the comparison's results to decide what to do.
3. `componentWillUpdate`- gets called in between `shouldComponentUpdate` and `render`. Receives two arguments: `nextProps` and `nextState`. You cannot call `this.setState` from its body; its main purpose is to interact with things outside of the React architecture. If you need to do non-React setup before a component renders, such as checking the window size or **interacting with an API**, this method is a good time to do that.
4. `render`
5. `componentDidUpdate` - called after any rendered HTML has finished loading. Automatically passed two arguments: `prevProps` and `prevState`, references to component's `props` and `state` before the current updating period began that you can compare to current `props` and `state`. Often used for interacting with things outside of React environment, such as browser and APIs, making it similar to `componentWillUpdate`.

### R2D70

**Today's Progress:** Completed Codecademy's Learn ReactJS: Part II and Introduction to JavaScript (a newly added portion of the course, covering higher-order functions).

**Notes:**
* There's only one unmounting lifecycle method: `componentWillUnmount`. A component's unmounting period occurs when a component is removed from the DOM, which could happen if the DOM is rerendered without the component, or if the user navigates to a different website or closes their web browser.
* `async` and `defer` are boolean attributes. Example: `<script async src="script.js"></script>`. They are useless if you place the script tag at the bottom of the page before the closing body tag. (If you place the script tag there, the script is loaded and executed after the rest of the page has been parsed and loaded. This is the _next best_ [slower because the script isn't loaded asynchronously] thing performance-wise to using `async` or `defer` attributes (if you need to support older browsers that don't yet have `async` or `defer` enabled), and makes the page appear to the user sooner than if the script were placed in the head, in which case it would interrupt HTML parsing.)
* With either attribute, the script is fetched asynchronously, but with `async`, the HTML parsing is interrupted to execute the script as soon as the script is finished being fetched. On the other hand, with `defer`, the script is only executed _after_ the HTML parsing is complete.
* To optimize page loading speed, it's best to put scripts in the head and add a `defer` attribute.
* **async/await**: Placing the `async` keyword before a function ensures that it returns a promise. If the `async` function returns a value, that value will also get wrapped in a promise, which means you'll have to use `.then` to access it. Example:

  ```javascript
  async function add (x, y) {
    return x + y
  }

  add(2,3).then(result => {
    console.log(result) // 5
  })
  ```

The keyword `await` can only be used within an `async` function. The keyword `await` makes JavaScript wait until the promise settles and returns its result.
* Higher-order functions are functions that accept other functions as arguments (or in other words, passed into a function's parameter. Parameters are temporary variable names within functions. The argument can be thought of as the value that is assigned to that temporary variable) and/or return functions as output. You can assign a function to a variable, e.g.:

  ```javascript
  const announceThatIAmDoingImportantWork = () => {
    console.log("I’m doing very important work!");
  };

  const busy = announceThatIAmDoingImportantWork;
  ```

### R2D71

**Today's Progress:** Continued Codecademy's Introduction to JavaScript (a newly added portion of the course, covering higher-order functions).

**Notes:**
* Functions passed as arguments to another function (higher-order functions are what functions that accept other functions as arguments are called) are called callback functions.
* When we pass a function in as an argument to another function, we don't invoke it. Invoking the function would evaluate to the return value of that function call/invocation. With callbacks, we pass in the function itself by typing the function name without the parentheses (that would evaluate to the result of calling the function).
* Example of higher-order function with callback (it takes in a function as an argument, saves a starting time, invokes the callback function, records the time after the function was called, and returns the time the function took to run by subtracting the starting time from the ending time.:

  ```javascript
  const timeFuncRuntime = funcParameter => {
   let t1 = Date.now();
   funcParameter();
   let t2 = Date.now();
   return t2 - t1;
  }

  const addOneToOne = () => 1 + 1;

  timeFuncRuntime(addOneToOne);
  ```
  Anonymous functions can also be arguments:

  ```javascript
  timeFuncRuntime(() => {
    for (let i = 10; i>0; i--){
      console.log(i);
    }
  });
  ```

### R2D72

**Today's Progress:** Finished the portion of Codecademy's Introduction to JavaScript covering higher-order functions, and started the portion on advanced objects (another newly added part of the course).

**Notes:**
* In JavaScript functions are first-class objects, meaning they can be stored in a variable, object, or array; passed as an argument to a function; or returned from a function.
* Within the scope of a method, you don't automatically have access to other properties in that method's object. If you invoke a method that is supposed to console log the value of a property on the method, you'll get a reference error. Example:

  ```javascript
  const goat = {
    dietType: 'herbivore',
    makeSound() {
      console.log('baaa');
    },
    diet() {
      console.log(dietType);
    }
  };
  goat.diet();
  // Output will be "ReferenceError: dietType is not defined"
  ```
However, you _can_ access that property with `this`; it references the calling object, providing access to the object's properties.

```javascript
const goat = {
  dietType: 'herbivore',
  makeSound() {
    console.log('baaa');
  },
  diet() {
    console.log(this.dietType);
  }
};

goat.diet();
// Output: herbivore
```

*  Using `this` in a method with an arrow function works differently. Arrow functions shouldn't be used in methods when using `this`. Arrow functions don't provide their own `this` binding; it retains the value of the enclosing lexical context (in global code, it's the global object, which is `window` in browsers). `this` is lexically scoped, meaning it uses `this` from the code containing the arrow function; it always references the owner of the function it is in. The methods `call()`, `apply()`, and `bind()` will not change the value of this in arrow functions. In this example, the value of `this` is the global object, an object that exists in the global scope, which doesn't have a `dietType` property and thus returns `undefined`.

```javascript
const goat = {
  dietType: 'herbivore',
  makeSound() {
    console.log('baaa');
  },
  diet: () => {
    console.log(this.dietType);
  }
};

goat.diet(); // Prints undefined
```

* With a constructor function, the value of `this` is bound to the new object being created.
* When you use `this.` in the global scope, you create a public property on the window object. For example: `this.table = 'window table';`

### R2D73

**Today's Progress:** Continued Codecademy's Introduction to JavaScript portion covering advanced objects (another newly added part of the course).

**Notes:**
* ES6 shorthand for methods:
Instead of:

  ```
  checkEnergy: function() {
    console.log(`Energy is currently at ${this.energyLevel}%.`)
  ```

You can do:

  ```
  checkEnergy() {
    console.log(`Energy is currently at ${this.energyLevel}%.`)
  ```

* When discussing privacy in objects, it is defined as the idea that only certain properties should be mutable. Some languages have privacy built in for objects, but not JavaScript. Developers follow naming conventions that signal to other developers how to interact with a property. A common one is to prepend a property with an underscore to indicate that the property should not be altered. For example:

  ```
  const bankAccount = {
    _amount: 1000
  }
  ```

This doesn't mean you can't reassign it: `bankAccount._amount = 1000000;`.
Getters and setters are used to respect the intention of a prepended property. Getters can return the value of internal properties and setters can safely reassign property values.
* Getter methods do not need to be called with a set of parentheses. Syntactically, it looks like we're accessing a property.
* Some notable advantages of using a getter method:
1. Getters can perform an action on the data when getting a property.
2. Getters can return different values using conditionals.
3. In a getter, we can access the properties of the calling object using this.
* Another thing to keep in mind when using getter (and setter) methods is that properties cannot share the same name as the getter/setter function. If we do so, then calling the method will result in an infinite call stack error. One workaround is to add an underscore before the property name.
Getter example:

  ```javascript
  const person = {
    _firstName: 'John',
    _lastName: 'Doe',
    get fullName() {
      if (this._firstName && this._lastName){
        return `${this._firstName} ${this._lastName}`;
      } else {
        return 'Missing a first name or a last name.';
      }
    }
  }

  // To call the getter method:
  person.fullName; // 'John Doe'
  ```

### R2D74

**Today's Progress:** Continued Codecademy's Introduction to JavaScript portion covering advanced objects (another newly added part of the course).

**Notes:**
* Setter methods reassign values of existing properties within an object
* Setters need at least one parameter.
* Using the setter method looks syntactically like reassigning a property: `robot.someSetterMethod = 9001;`
*  A factory function is a function that returns an object and can be reused to make multiple object instances. Factory functions can also have parameters allowing us to customize the object that gets returned.
* Example of a factory function for a monster, and usage of it to make a specific monster (note you can also use a destructuring technique called proprty value shorthand [see MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Object_initializer#Property_definitions), simply putting one word since both are the same)

  ```javascript
  const monsterFactory = (name, age, energySource, catchPhrase) => {
    return {
      name: name,
      age: age,
      energySource: energySource,
      scare() {
        console.log(catchPhrase);
      }
    }
  };

  const ghost = monsterFactory('Ghouly', 251, 'ectoplasm', 'BOO!');
  ghost.scare(); // 'BOO!'
  ```

  Another example of a factory function and its usage:

  ```javascript
  const robotFactory = (model, mobile) => {
  return {
    model,
    mobile,
    beep() {
      console.log('Beep boop');
    }
  };

  };

  const tinCan = robotFactory('P-500', true);

  tinCan.beep(); // Beep boop
  ```

* Note that the `return` statement is affected by automatic semicolon insertion (ASI). No line terminator is allowed between the `return` keyword and the expression. To get around this you can use parentheses.

### R2D75

**Today's Progress:** Continued Codecademy's Introduction to JavaScript portion covering advanced objects (another newly added part of the course).

**Notes:**
* Extracting key-value pair from object and saving it as a property:

  ```javascript
  const vampire = {
    name: 'Dracula',
    residence: 'Transylvania',
    preferences: {
      day: 'stay inside',
      night: 'satisfy appetite'
    }
  };

  // Normal (slightly longer) way
  const residence = vampire.residence;
  console.log(residence); // Prints 'Transylvania'

  // With destructured assignment
  const { residence } = vampire;
  console.log(residence); // Prints 'Transylvania'

  // Using destructured assignment to grab nested properties
  const { day } = vampire.preferences;
  console.log(day); // Prints 'stay inside'
  ```

*  In destructured assignment we create a variable with the name of an object's key that is wrapped in curly braces `{ }` and assign to it the object. Syntax: `const { propertyName } = obj;`
* See [built-in object methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object#Methods) and [object methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object#Methods_of_the_Object_constructor)
* The object that a method belongs to is called the calling object.

### R2D76

**Today's Progress:** Completed Codecademy's Introduction to JavaScript portion covering advanced objects (and therefore refinishing the course), and started Codecademy's Learn Ruby course.

**Notes:**
* In both JavaScript and Ruby, the remainder, or modulo, operator `%` returns the remainder of a division operation. For example, `5 % 2` returns `1`.
* Ruby: the `print` command takes whatever you want and prints it to the screen. `puts` also does so, but it also adds a blank line after whatever is printed.
* Everything in Ruby is an object, and therefore everything in Ruby has certain built-in abilities called methods.
* Recall that in JavaScript, everything is an object except for the six primitives: boolean, null, undefined, number, string, and symbol.
* To comment in Ruby use `#` or `=begin` and `=end` (on their own lines, and note no space after the equals sign) for multi-line comments.
* One type of variable in Ruby is a local variable. Local variables should start with a lowercase letter and words should be separated by underscores, like `counter` and `masterful_method`. Ruby won't stop you from starting your local variables with other symbols, such as capital letters, `$s`, or `@s`, but by convention these mean different things, so it's best to avoid confusion by doing what the Ruby community does. You declare a variable just by saying it and set it with `=`.
* Getting input: `variable_name = gets.chomp`: `gets` is the Ruby method that gets input from the user. When getting input, Ruby automatically adds a blank line (or newline) after each bit of input; chomp removes that extra line. [See lesson](https://www.codecademy.com/courses/learn-ruby/lessons/putting-the-form-in-formatter/exercises/getting-input?action=resume_content_item).
* Use `#{}` for string interpolation with variables:

  ```ruby
  n = "cheese"
  puts "#{n}"
  puts "I love #{n}!"
  ```

* In Ruby, the "environment" refers to the collection of all variables and their values that exist in the program at a given time.
* Control flow allows for a flexible program that changes behavior based in reaction to the evironment. We can select different outcomes depending on information the user types, the result of a computation, or the value returned by another part of the program.
* Ruby doesn't care about whitespace. Indentation isn't necessary, but it's a convention that Rubyists follow. Two spaces is common.
* To use control flow to check if something is the opposite of the conditional, use an `unless` statement. Example:

  ```ruby
  x = 1
  unless x > 0 # This is like saying "if x is not greater than 0"
   puts 'x is less than 0'
  else   
   puts 'x is greater than 0'
  end
  ```

* `==` and `!=` are called comparators or relational operators.
* In both Ruby and JavaScript, `!` (not) is a boolean operator.
* In Ruby (as elsewhere) expressions in parentheses are always evaluated before anything outside parentheses. You can combine boolean operators: `(x && (y || w)) && z`
* An exclamation point at the end of something modifies that variable in place (without it, Ruby would make a copy of the variable and modify that instead). Example:

print "Thtring, pleathe!: "
user_input = gets.chomp
user_input.downcase! # With !, user_input will be lowercase next time it's used

if user_input.include? "s"
  user_input.gsub!(/s/, "th")
else
  puts "Nothing to do here!"
end

puts "Your string is: #{user_input}"

### R2D77

**Today's Progress:** Continued Codecademy's Learn Ruby course.

### R2D78

**Today's Progress:** Continued Codecademy's Learn Ruby course.

**Notes:**
* Assignment operators: `+=`, `-=`, `*=`, and `/=`
* Ruby doesn't have the increment and decrement operators `++` and `--`
* In JavaScript, you can use increment and decrement operators. They can come before or after the operand. When they follow the operand, as with `x++`, the value will be returned _before_ the operand is increased/decreased. Example:

  ```javascript
  let a = 1;
  console.log(a++);   // 1
  console.log(a);     // 2
  ```

  If you’d rather make the variable increment/decrement before returning, you simply have to use the increment/decrement operator before the operand

### R2D79

**Today's Progress:** Read about how webpack works.

### R2D80

**Today's Progress:** Started Codecademy's course Learn Sass and SoloLearn's Git course.

### R2D80

**Today's Progress:** Read various things about Sass and continued and SoloLearn's Git course.

### R2D81

**Today's Progress:** Continued Codecademy's Learn Sass course.

**Notes:**
* Nesting is the process of placing child selectors and properties in the scope of a parent selector. This allows a programmer to draw DOM relationships and avoid repetition.
* Variables make it easy to update code and reference values by allowing you to assign an identifier to a value.
* Sass data types: color (even '10px' is considered a number), numbers, strings (with single, double, or no quotes), booleans, and null, lists, and maps
* Lists can be separated by either spaces or commas. Example: `1.5em Helvetica bold;` You can also surround a list with parentheses and create lists made up of lists. A list variable: `$standard-border: 4px solid black;`
* Maps are very similar to lists, but instead each object is a key-value pair. The typical map looks like: `(key1: value1, key2: value2);` In a map, the value of a key can be a list or another map.
* In Sass, the `&` character is used to specify exactly where a parent selector should be inserted. It also helps write psuedo classes in a much less repetitive way.
* A CSS pseudo-element is a keyword added to a selector that lets you style a specific part of the selected element(s). For example, the selector `p::first-line` would style the font of the first line of a `p` element.
* A CSS pseudo-class is a keyword added to a selector that specifies a special state of the selected element(s). For example, the selector `button:hover` would change a button's color when the user's pointer hovers over it.
* In Sass, the mixin directive lets you make groups of CSS declarations that you want to reuse throughout your site. It is particularly useful for vendor prefixes. Example:

  ```
  @mixin backface-visibility {
    backface-visibility: hidden;
    -webkit-backface-visibility: hidden;
    -moz-backface-visibility: hidden;
    -ms-backface-visibility: hidden;
    -o-backface-visibility: hidden;
  }
  ```

  To use this mixin as a declaration:
  ```
  @include backface-visibility;
  ```

  Mixins also have the ability to take in a value, such as $visibility in this example:

    ```
    @mixin backface-visibility($visibility) {
      backface-visibility: $visibility;
      -webkit-backface-visibility: $visibility;
      -moz-backface-visibility: $visibility;
      -ms-backface-visibility: $visibility;
      -o-backface-visibility: $visibility;
    }
    ```

  You should only ever use a mixin if it takes an argument (so the first mixin example is actually a discouraged use).

  You can have a default value for a mixin's argument that would be overridden if a value is passed in when the mixin included in a declaration, but that applies if no value is specified (and the round brackets are left empty). Example:

  ```
  @mixin backface-visibility($visibility: hidden) {
    // Backface properties
  }
  ```

  A mixin can take multiple arguments. When they are explicity defined, the arguments can be out of order.

  If a mixin definition has a combination of arguments with and without a default value, you should define the ones with no default value first.

  Mixins can be nested.
* Sass allows you to pass in multiple arguments in a list or a map format. See [Codecademy lesson](https://www.codecademy.com/courses/learn-sass/lessons/mixins-and-parent-selector/exercises/mixins-ii?action=resume_content_item) for details.
* In Sass, string interpolation is the process of placing a variable string in the middle of two other strings. In a mixin context, interpolation is handy when you want to make use of variables in selectors or file names. Notation:

  ```
  @mixin photo-content($file) {
    content: url(#{$file}.jpg); //string interpolation
    object-fit: cover;
  }

  //....

  .photo {
    @include photo-content('titanosaur');
    width: 60%;
    margin: 0px auto;
  }
  ```

* Sass allows uage of the `&` selector inside of mixins. The flow works like this:
1. The `&` selector gets assigned the value of the parent at the point where the mixin is included.
2. If there is no parent selector, then the value is null and Sass will throw an error.
[See Codecademy lesson for more](https://www.codecademy.com/courses/learn-sass/lessons/mixins-and-parent-selector/exercises/mixin-parent-selector?action=resume_content_item).

* Sass functions allow you to iterate through lists and maps, operate on color values, apply styles based on conditions, and assign values that result from math operations.
* Sass arithmetic operators are `+`, `-`, `*`, `/`, and `%` (modulo, the remainder of a division operation).
* When multiplying, keep in mind that `10px * 10px` would, like in regular math, be `100px * px` (squared units), so you'd have to do `10px * 10` to get `100px`.

### R2D82

**Today's Progress:** Completed Codecademy's Learn Sass course.

**Notes:**
* Each loops in Sass iterate on each of the values in a list. Syntax:

  ```
  @each $item in $list {
    // Rules and/or conditions
  }
  ```

  Usage example:

  ```
  $list: (orange, purple, teal);

  @each $item in $list {
    .#{$item} {
      background: $item;
    }
  }
  ```

* For loops in Sass can be used to style numerous elements or assign properties all at once. Syntax:

  ```
  @for $i from $begin through $end {
     // Rules and/or conditions
  }
  ```

  Where:
  1. `$i` is just a variable for the index, or position, of the element in the list.
  2. `$begin` and `$end` are placeholders for the start and end points of the loop.
  3. The keywords `through` and `to` are interchangeable in Sass.

* In Sass, `if()` is a function that can only branch one of two ways based on a condition. You can use it inline, to assign the value of a property:

  ```
  width: if($condition, $value-if-true, $value-if-false);
  ```

  For cases with more than two outcomes, the `@if`, `@else-if`, and `@else` directives allow for more flexibility:

  ```
  @mixin deck($suit) {
    @if($suit == hearts || $suit == spades) {
      color: blue;
    }

    @else-if($suit == clovers || $suit == diamonds) {
      color: red;
    }

    @else {
      // Some rule
    }
  }
  ```

* Sometimes `/` can function as a separator or division operator.
* The @extend directive allows classes to share a set of properties with one another. Usage example:

  ```
  .foo {
    color: black;
    border: 1px solid black;
  }

  .bar {
    @extend .foo;
    background-color: red;
  }
  ```

* An underscore is added to the beginning of Sass files to indicate that the file is only a partial file and should be imported to another file rather than compiled. Otherwise, if they use variables or mixins defined elsewhere, they will fail to be referenced correctly. Partial files are imported (using the `@import` directive) to a main stylesheet (often called `styles.scss` or `main.scss`). The advantage of using partial files is it's a good way to modularize your CSS and make it easier to maintain. To import a partial file using an `@import` statement, the underscore prefix is omitted, for example: `@import "variables";`
* An example of file structure: in a folder named sass, have a subfolder called `components` (containing files such as `_buttons.scss`, `_carousel.scss`, and `cover.scss`), another called `helpers` (with files such as `_variables.scss`, `_functions.scss`, and `_mixins.scss`), another called `layout` (containing files like `_grid.scss` [CSS grid system], `_header.scss`, and `_footer.scss`), and one called `pages`, with files like `_home.scss`, `_contact.scss`, with styles specific to those pages.
* Sass extends the existing CSS `@import` rule to allow including other SCSS and Sass files.
cally, all imported SCSS files are imported into a main SCSS file which is then combined to make a single CSS output file.
The main/global SCSS file has access to any variables or mixins defined in its imported files. The `@import` command takes a filename to import.
By default, `@import` looks for a Sass file in the same or otherwise specified directory, but there are a few circumstances where it will behave just like a CSS `@import` rule:
1. If the file's extension is `.css`.
2. If the filename begins with `http://`.
3. If the filename is a `url()`.
4. If the `@import` has any media queries.
* Sometimes, you may create classes solely for the purpose of extending them and never actually use them inside your HTML.
Sass anticipated this and allows for a special type of selector called a placeholder, which behaves just like a class or id selector, but uses the `%` notation instead of `.` or `#`.
Placeholders prevent rules from being rendered to CSS on their own and only become active once they are extended anywhere an id or class could be extended.
Placeholders are a nice way to consolidate rules that never actually get used on their own in the HTML.
* You should extend rather than use mixins unless your mixin takes an argument, because extend output is cleaner.
