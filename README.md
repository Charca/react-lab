# react-lab
React and Flux training

> This is a very basic course that aims to gather some knowledge about the framework and how to quickly start using it.
> It's very bare-bones for now, so if you wish to contribute with links, examples, wording or pretty much anything, please open an issue or a PR in this repository. Thanks for reading!

## Table of Contents
1. [Introduction](#introduction)
2. [React and JSX](#react-and-jsx)
3. [Props and State](#props-and-state)
4. [Thinking in React](#thinking-in-react)
5. Flux
6. Routing
7. Testing
8. React and ES6
9. Final Exercise

## Introduction

Welcome to the React Lab. This course was created to onboard developers into the world of building web applications with React and Flux. We'll cover everything from the basics of building React components, to creating full web applications using different tools and techniques.

Each chapter is composed of a series of links with documentation and examples for you to read, and it ends with a few exercises to apply the knowladge gathered in the process.

You can dedicate as much time as you want and go as deeply as needed into each one of the links.

### Prerequisites

You need to have at least a basic level of how the JavaScript language works. You don't need to have any experience with other frameworks or libraries, but it'd help if you've had some exposure to common JS design patterns and OOP.

In order to follow some of the tutorials, you'll need to have Node.js with NPM installed. If you don't have it already, check out the [Node.js website](https://nodejs.org/) for instructions on how to set up your enviroment for your OS.

### Support

We have a [Gitter chat room](https://gitter.im/Charca/react-lab) available if you need support, or you can contact any of the collaborators to the project.


## React and JSX

React is a JavaScript library built by Facebook and open sourced in 2013. Since then it gained a lot of popularity and it's now among the top JavaScript libraries (Backbone, Angular, Ember...). It's also being used in production both by Facebook and Instagram, among other large companies.

React is not a complete solution for building web applications, but it's really useful for building user interfaces, and it can be combined with frameworks like Backbone to provide a full experience on the web. It can be used to create simple components like buttons and form elements, or large and complex views to wrap your entire application.

React uses an optional syntax called JSX, that is a mix between XML and HTML, and it serves to define your components in a declarative way. It also provides transformers to compile JSX code to vanilla JavaScript so it can be interpreted by the browser.

A simple React component looks like this:

```javascript
var HelloMessage = React.createClass({
  render: function() {
    return <div>Hello, {this.props.name}</div>;
  }
});

React.render(
  <HelloMessage name="Maxi" />,
  document.getElementById('container')
);
```

This example will render a `<div>` with the message "Hello, Maxi" into a container on the page.

### Reading / watching material
- [[Docs] React Documentation index](http://facebook.github.io/react/) - Read about React and play around with the simple examples on the page. Also note the difference between the JSX version and the Compiled JS.
- [[Blog] An Introduction to React.js](http://www.instrument.com/developers/an-introduction-to-react-js) - Read more about the features of React and JSX.
- [[Video] Hello World - First Component](https://egghead.io/lessons/react-hello-world-first-component) - Watch the first video the React Fundamental series by egghead.io, he'll show you how to create your first component.
- [[Video] The Render Method](https://egghead.io/lessons/react-the-render-method) - Watch the second video of egghead's series to learn more about the render method.

### Exercises
- Complete the [Getting Started example](http://facebook.github.io/react/docs/getting-started.html).


## Props and State

React components don't have models to store and manage data internally, but there are two ways of keeping track of the information the component needs to work: **props** and **state**.

In a nutshell, *props* (or properties) are provided to the component when it's created and it serves as the initial configuration of a component. Props can have predefined default values and types (for example a property `name` can have a default value of `"John"` and it may only accept values of the type `string`). The important thing about props is that they're **immutable**; once a component has been created, they cannot change during the life-cycle of that component.

*State* on the other hand can suffer mutations and change its value at any time. There's a default state that is created when the component is initialized, and every time state change for any reason, that component will re-render itself to reflect those changes.

You'll make use of props and state on most of your components, so it's very important to understand the difference.

### Reading / watching material

- [[Video] Introduction to Properties](https://egghead.io/lessons/react-introduction-to-properties) - Learn about the basics of props and propTypes.
- [[Video] State Basics](https://egghead.io/lessons/react-state-basics) - Learn about state and the difference with props.
- [[Docs] props vs state](https://github.com/uberVU/react-guide/blob/master/props-vs-state.md) - Learn more about the difference between props and state, and when you should use each one.

### Exercises

- Complete the [Official React Tutorial](http://facebook.github.io/react/docs/tutorial.html).


## Thinking in React

Working with React means working with components, and in order to understand how those components connect to each other, you have to first understand how they work in isolation.

Thinking in React means thinking how to structure your user interface by breaking it down into smaller components, and focus on the features of each one of them. Those components have to be loosely coupled and highly cohesive, and they have to be easy to integrate with the rest of your application.

### Reading / watching material

- [[Docs] Thinking in React](https://facebook.github.io/react/docs/thinking-in-react.html) - Learn how to start Thinking in React (TiR)
- [[Video] Thinking in React](http://tagtree.tv/thinking-in-react) - Watch this screencast to see the TiR approach in practice.

### Exercise

Use React thinking to build this simple mail app:

![Mini Mail App](assets/mail-app-comp.jpg)
> Comp created by Ionut Zamfir, check out his work on Dribble: [https://dribbble.com/ionuss](https://dribbble.com/ionuss)

#### Instructions

- Download the comp and use an image editor (like MS Paint or Gimp) to break it down into smaller components.
- Use a data source for the list, you can create a .json file or a JavaScript object/array with a structure like this:

```
[
	{
		name: 'Jonathan Doe',
		text: 'Lorem ipsum dolor sit amet...',
		status: 'online',
		avatar_url: 'johndoe.png'
	}
]
```

- Don't worry too much about the look and feel, just create a simple layout to display the information.
- *Optional:* If you want to add a bit of functionallity, filter the results by typing into the "Enter keywords" text field. (Tips on how to do that in the Thinking in React video)
- *Optional:* If you want to make it pixel perfect, you can download the free PSD [here](http://www.premiumpixels.com/freebies/mini-mail-application-psd/).