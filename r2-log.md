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
