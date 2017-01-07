## Website Performance Optimization portfolio project

## Project overview

The objective is to optimize a specified online portfolio for speed. In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques picked up in the [Critical Rendering Path course].

## Getting started

### Part 1: Optimize PageSpeed Insights score for index.html

#### Specification
Identify and perform optimizations to achieve a PageSpeed Insights score of 90 for both mobile and desktop.

#### Steps taken
* Changed Google Analytics script to async version
* Changed Google Webfonts from external link to inline CSS
* Changed style.css from external link to inline CSS

#### PageSpeed Insights Score
* 94/100 Mobile
* 96/100 Desktop

#### To check the PageSpeed Insights score and recommendations
* Open a browser tab or window
* Go to [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/)
* Paste in the URL of index.html
* Click on ANALYZE

### Part 2: Optimize Frames per Second in pizza.html

#### Specifications
* Identify and perform optimizations ensuring a consistent frame rate at 60fps when scrolling
* Time to resize pizzas in pizza.html is less than 5 ms as shown in the browser console
* Provide comments in views/js/main.js for pizza.html that effectively explain longer code procedures
* Provide a README file to describe the optimizations.

#### Steps taken
* Optimized the pizza image with the help of PageSpeed Insights.
* Refactored the ```changePizzaSizes()``` function to eliminate a forced synchronous layout.
* Refactored the ```updatePositions()``` function to eliminate another forced synchronous layout.
* Incorporated a ```requestAnimationFrame``` into the scroll function to smooth rendering.
* Used the ```will-change``` directiev efficiently.
* The code for generating sliding pizza is refactored. 

#### To check the frame rate and resize time of the optimized version
* Open up Google Chrome browser
* Open pizza.html on your browser
* To open the DevTools
  - Select the Chrome menu at the top-right of your browser window, then select Tools > Developer Tools.
  - Right-click on any page element and select Inspect Element
  - Use CTRL + SHIFT + I (or CMD + OPT + I on Mac)
  - Press F12
  - More [shortcuts](https://developers.google.com/web/tools/iterate/inspect-styles/shortcuts)
* To check the resize time
  - If the console drawer is not visible, click on **>_** at the top-right of the DevTools window
  - Click the left or size side of the slider
  - The message `Time to resize pizzas:` followed by the time in milliseconds will display on the console

* To check the frame rate
  - Click on Timeline in the DevTools menu
  - To start recording a new timeline, click the record toolbar button at the top-left (below the search button) of the DevTools window, or press CTRL + E
  - While recording, scroll the Cam's Pizzeria page up and down a few times
  - Click the record toolbar button or press CTRL + E to stop recording
  - Select an area of interest in the overview by dragging.  Zoom and pan the timeline with the mousewheel or WASD keys

