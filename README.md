# pomodoro

A simple pomodoro timer to help you stay on task. Choose the length of time for your timer. Once time is up you will receive an alert letting you know that the chosen time period has elapsed.

For more information about the pomodoro technique, check out this article by [todoist](https://todoist.com/productivity-methods/pomodoro-technique)

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users are able to:

- Choose between a 20 minute pomodoro, a 5 minute short break or a 30 minute long break.
- Receive an alert when time is up

### Screenshot

![](./images/screenshot.jpg)

### Links

- Live Site URL: [Live Demo](https://alekzandriia.github.io/pomodoro)
- Solution URL: [Source Code](https://github.com/alekzandriia/pomodoro)

## My process

This timer app uses the setInterval() method, which repeatedly calls a function or executes a code snippet with a fixed time delay between each call.

The interface is created using HTML input elements.
Radio buttons are used to allow the user to choose one option at a time. In this case, the options are the amount of time the timer will run for.

A pomodoro is traditionally a 25 minute period of work, followed by a 5 minute break. After 4 pomodoros, you can take a longer 30 minute break.

The user can choose to set the timer for:

- 25 minutes (work)
- 5 minutes (short break)
- 30 minutes (long break)

When the user selects one of the options:
The time remaining (in seconds) is saved to a timer variable
This seconds are used to calculate the corresponding time in minutes and hours
The webpage is updated to show the time remaining in minutes (because that unit of time makes the most sense)

The Play/Pause button listens for a click event, and responds by either calling the start() function or the stop() function (depending on its current state).

The start function is used to initiate the setInterval method on the updateTime() function.
The stop function is used to clear the interval, and stop the function from continuing to run.

updateTime() keeps track of the time elapsed in seconds, then calculates the minutes, and hours. It displays this time on the page in real time.
The countdown begins with the amount of time chosen by the user (in seconds), and decrements by 1 for each second that passes.
Once the timer reaches 0, the timer is halted with clearInterval and the user receives a pop-up alert window to notify them that time is up.

The user can then select the next timer that they want to start, and press the start button to continue.

Further development
It might be nice to keep track of the number of pomodoros the user has completed so that they can be notified when they are due for a long break.
Animations would be a great way to add some gamification which motivates the user to keep going.
I would also like to see how I can play with the alert (custom sound, vibrate the device, etc).

### Built with

- Semantic HTML5 markup
- CSS3
- Flexbox
- Google fonts
- JavaScript

### What I learned

How to style a set of custom radio buttons by hiding the default input and adding styles to the input labels instead.

How to use setInterval to execute functions repeatedly.

### Continued development

- It might be nice to keep track of the number of pomodoros the user has completed so that they can be notified when they are due for a long break.
- Customization is always a welcome features: allow the user to customize the length of the timers, and allow the user to change the colour scheme.
- Animations would be a great way to add some gamification to motivate the user to keep going.
- I would also like to see how I can play with the alert (custom sound, vibrate the device, etc).

### Useful resources

Styling Checkbox Input
[Styling Custom Radio Buttons](https://www.youtube.com/watch?v=GDh9uToZkYg)
[MDN Set Interval](https://developer.mozilla.org/en-US/docs/Web/API/setInterval)

## Author

- Website - [Alekzandriia](https://www.alekz.dev)
- Twitter - [@alekzandriia](https://www.twitter.com/alekzandriia)
