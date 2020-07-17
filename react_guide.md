# My React Guide

### ReactJS - How it born
* Traditionally, before React, pages were static, you send request to server and server sends an page written in **HTML, CSS & JS**, and every time you request something from server, this process happened again and again, since there were also different browsers, they also handle **DOM** in a different way, they have to reload a page to update something.
* Then **jQUERY** can and they unified the handling of **DOM** with a specific syntax, resulting in dynamic content generation without reloading the page, across all browsers.
* But now, websites tend to become bigger and greater like facebook, where so much info is traded back and forth,resulting in getting **JS** files bigger and bigger.
* **Backbone.js** came to the rescue which helped in orgainising JS files, application continued to grew bigger and we got **SPA - Single Page Application**.
* Initially we were having a separate web page written in HTML, CSS & JS for everything containing jQUERY, for manipulating pages, **AJAX** also got introduced.
* Now we were loading a page once and then we were manipulating the DOM, we were able to login, logout without sending requests to server everytime.
* In 2010, **AngularJS** came, which changed the way to build web applications. It modified all the code into containers, organized it so well, and there was like *"this is the way web applications should be built."*, the concept of **MVC/MVVM** was introduced. Complex applications started simple to code, AngularJS gained so much popularity, but there was one problem...
* **The applications were being messy, data was overflowing everywhere. If a button is clicked it changes some section, which in return changes other section, which also changes other things. It was being hard to find bugs and maintain app.**
* Facebook ads were getting bigger and bigger the developers were facing hard time to cope up with things. And there were so many backend wires, they all were getting messy
* Facebook came up with the solution and it worked really well for them and in 2013, ReactJS born.
* And seeing this Google realized that AngularJS is not benifitting complex applications anymore, they completely **Re-write** the library and named it **Angular without JS**, meantine many developers moved to ReactJS.

## ReactJS - It's birth
* **React got famous due to 4 key features/concepts**

* **Don't touch the DOM. I'll do it.**
    * For changing DOM 2 methods are used, it is quite expensive to change DOM

    * Imperative : It is an imperative paradigm you directly change individual parts of your app in response to various user events. everything has to manually written and wired up.

    **Instead of this Imperative approach REACTJS came with Declarative approach**

    * Declarative : we define the blueprint, that how the page will look like, just give what to display, the object/data and it will take care of everything.

* **Build websites like LEGO blocks**
    * React is all about components. you have different different components like *navigation component*, *profile component*, *picture component* etc
    * These components are reusable, you can copy the code in other project, people began to share components like *react bootstrap, blueprintjs* etc
    * **Components** are basically JS functions that receieve inputs or attributes which we call props and return HTML like thing, wrapped in JS. These components are built with HTML tags and each component then is arranged together to build our entire app.

* **Unidirectional Data Flow**
    * State, components, JSX together make Virtual DOM, which is tree like object which acts like a blueprint of our app. And then this virtual DOM is responsible for changing browsers' DOM.
    Data only moves from up to down.
    * When there is a state change, it changes in our components, and then these changes are reflected in Virtual DOM.
    * Also results in Easy debugging that this can be the component causing problem, narrowing down bug searching.

* **UI, the rest is up to you**
    * A library is like a Kitchen, Here React is Like a stove, if you want to make a soup, you can use whatever other tool like spoon, spatula etc, to make whatever you want. It is independent of another framework/library/backend etc
    * The components, blueprints, VirtualDOM is all what React cares about.
    * React gives a blueprint of what the UI should look like and other frameworks like **React Native** can take reference and can change view according IOS/Android app, also **React 360** for VR, **Electron** for desktop apps.

## The Job of a React Developer
* Decide the components
* Decide the State and where it lives
* What changes when state changes

## Some Key Points
* Classes are used because they support states, which can be used to change anything on the screen, this is achieved with the help of the constructor keyword

* you can only modify state by using *this.setState* method, and as soon as the state changes, we re-render the component

* JSX tries to mimic HTML to create VirtualDOM
* Lifecycle methods are those methods that are called at different stages (automatically by react) when this (specific component) gets rendered

* When we build components, they take something called props, i.e the parameter for functional components

* *{props.children}* is all then content that is wriiten between opening and closing tag of your component, by default they are null

* & we can also acces props in the class in which it is used (of course by any component) by using this.keyword

* setState is asynchronous function call

* In react components, *this* keyword is bounded by default in context of the current component state but when we write our own methods and functions, using *this* keyword in same context as before, gives an error, because they behave differently in custom-made methods.
* Reason - because JS by default doesn't set the scope of this keyword, it has to explicitly defined in constructor, because it is the first thing which runs when class component runs.
* Problem - That means we have to bind this keyword for every class method we make
* Solution - ES6 Arrow function, because it comes with *lexical scoping*, that means when it encounters *this* keyword it automatically binds this keyword to the place where it was defined first