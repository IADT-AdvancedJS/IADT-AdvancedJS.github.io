---
layout: post
title:  "EXERCISE - User Profile Web App"
date:   2018-02-21 10:05:00 +0000
categories: react
---

Work towards building something that functions like [this](https://user-profiles-1c532.firebaseapp.com/).

Start from [this code]({{ site.baseurl }}{% post_url 2018-02-20-react-fetch-50-randomusers %}).

Hints:
1. For now, don't worry about styling. You can do this at the end.
2. Used controlled components for the various user inputs, i.e. store their values in state.

Steps:
1. Display the first name of 50 users.
2. Display their first name and two letter nationality code.
3. Display their first name, two letter nationality code and profile image.
4. Add the _gender_ filter dropdown menu. Use `console.log()` to ensure you can handle selection of `all`, `male` and `female`.
5. Modify your render code to only render users who's gender matches that selected (stored in state).
6. Repeat 5. and 6. for nationality
7. Add the _sort by name_ radio buttons. Use `console.log()` to ensure you can handle selection of `yes` and `no`.
8. Modify your render code to sort the users before you display them, when `yes` is selected (stored in state).
9. Add the _search by name_ text input. Use `console.log()` to ensure you can handle changes to this text field and log what is typed.
10. Modify your render code to only display users who's name starts with the text that has been typed in (stored in state).
