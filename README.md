# react-lab
React and Flux training

> This is a very basic course that aims to gather some knowledge about the framework and how to quickly start using it.
> It's very bare-bones for now, so if you wish to contribute with links, examples, wording or pretty much anything, please open an issue or a PR in this repository. Thanks for reading!

## Table of Contents
1. [Introduction](#introduction)
2. [React and JSX](#react-and-jsx)
3. React Components
4. Props and State
5. Thinking in React
6. Flux
7. Routing
8. Testing

## 1. Introduction

Welcome to the React Lab. This course was created to onboard developers into the world of building web applications with React and Flux. We'll cover everything from the basics of building React components, to creating full web applications using different tools and techniques.

Each chapter is composed of a series of links with documentation and examples for you to read, and it ends with a few exercises to apply the knowladge gathered in the process.

You can dedicate as much time as you want and go as deeply as needed into each one of the links.

### Prerequisites

You need to have at least a basic level of how the JavaScript language works. You don't need to have any experience with other frameworks or libraries, but it'd help if you've had some exposure to common JS design patterns and OOP.

In order to follow some of the tutorials, you'll need to have Node.js with NPM installed. If you don't have it already, check out the [Node.js website](https://nodejs.org/) for instructions on how to set up your enviroment for your OS.

### Support

We have a [Gitter chat room](https://gitter.im/Charca/react-lab) available if you need support, or you can contact any of the collaborators to the project.


## 2. React and JSX

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
- Complete the [Getting Started example](http://facebook.github.io/react/docs/getting-started.html)



