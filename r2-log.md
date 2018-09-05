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
