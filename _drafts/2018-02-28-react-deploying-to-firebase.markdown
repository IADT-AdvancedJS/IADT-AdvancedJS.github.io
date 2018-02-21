---
layout: post
title:  "Deploying your React App to Firebase"
date:   2018-02-28 20:40:00 +0000
categories: react
---

Up until now, we have been hosting our React apps from our own computers, using `npm start` to host our app from a local webserver. Ultimately, we will need to host our React apps on the Internet. One way to do this is to use [Firebase](https://firebase.google.com), a backend as a service (BaaS) solution.

## Building your React app

Firstly, we need to build an optimised production version of our React app. Assuming you are in your React app folder, run `npm run build`. This will create a `build` folder containing an optimised version of your app ready for hosting.

## Getting started with Firebase

Next, go to [Firebase](https://firebase.google.com) and login (or create an account if you haven't already got one).

Once you are logged in, you should go to <https://console.firebase.google.com> and create a new project.

![Create new Firebase project]({{ "/assets/firebase/create-project.png" | absolute_url }})

Give the project a sensible name. For this tutorial, the project name chosen was `user-profiles`. Firebase will append some random text to this, giving something like `user-profiles-1c532`.

![Create new Firebase project details]({{ "/assets/firebase/create-project-details.png" | absolute_url }})

Then to install Firebase globally on your machine, run `npm install -g firebase-tools`.

Now you can use the Firebase command line tool to login to Firebase from the terminal using `firebase login`. You may need to visit the link provided at the terminal in order to sign-in with your Firebase/Google account.

## Deploying your React app to Firebase

To prepare your React app for deployment, go to your React project folder and run `firebase init`.

1. Use the up/down arrows and space to select 'hosting'. Hit enter.
![Selecting hosting]({{ "/assets/firebase/hosting.png" | absolute_url }})
2. Select the name of the Firebase project you want to deploy to, i.e. the name of your project from above.
![Selecting project]({{ "/assets/firebase/project-name.png" | absolute_url }})
3. When asked 'What do you want to use as your project directory?' Type `build` and hit enter.
![Selecting project directory]({{ "/assets/firebase/project-dir.png" | absolute_url }})
4. When asked to 'Configure as a single-page app', type `y` and hit enter.
![SPA]({{ "/assets/firebase/spa.png" | absolute_url }})
5. When warned that the file already exists, type `n` and hit enter.
![File exists warning]({{ "/assets/firebase/exists.png" | absolute_url }})

The Firebase setup is now done! We can deploy by running `firebase deploy`. You will then see the URL for your project! Try it in a browser, e.g. <https://user-profiles-1c532.firebaseapp.com/>.
