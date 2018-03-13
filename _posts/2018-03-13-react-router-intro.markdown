---
layout: post
title:  "Getting started with React Router"
date:   2018-03-13 09:40:00 +0000
categories: react
---

React Router is a package that allows you to configure certain URLs to show certain components.

For example, if you had a user profile component you could setup a route so that when the user clicks User Profile in the navigation bar, the user profile component gets rendered.

To install React Router run `npm install react-router-dom` in your React project folder.

Then, in the relevant `.js` file, import the following elements `import {BrowserRouter, Route, Link} from 'react-router-dom';`

The key components of React Router are:
1. Routes are configured in a `<BrowserRouter>` component.
2. The `<Link>` component is used to redirect to a particular path, e.g. `/about`.
3. Each Route is configured using `<Route>` components which specify which paths redirect to which Components.

See the example code below, which would result in this behaviour.

![React router demo]({{ "/assets/router/router.gif" | absolute_url }})


<button class="codepenBtn" onclick="window.location.href='https://codepen.io/aerrity/pen/paVoBz?editors=0010'">Try this on CodePen</button>

{% gist 784c01f91e6e1798dc9d45c1ee735a26 %}
