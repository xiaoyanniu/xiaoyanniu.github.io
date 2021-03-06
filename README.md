## Website Performance Optimization portfolio project

### Changes in the 3rd commit to file 'index.html'
• From line 55 - line 60, inlined the content in css/style-mobile.
• On line 68, reduced the size of image 'profilepic.jpg' from 14k to 8k.
• On line 98, replace image 'pizzeria_small.png' (39kb) with 'pizzeria_small.jpg' (10k)

### Changes in the 2nd commit to file 'Views/js/main.js'
• On line 423, added changeSliderLabel(size);
• On line 427, change document.querySelector("#randomPizzas") to document.getElementById("randomPizzas").
• On line 453, change document.querySelectorAll(".randomPizzaContainer") to document.getElementsByClassName("randomPizzaContainer").
• On line 456, remove the size parameter in the changePizzaSizes() function.
• On line 461, remove requestAnimationFrame(changePizzaSizes(size));
• On line 464, change requestAnimationFrame(changePizzaSizes(size)); to changePizzaSizes(size);
• On line 478, change the number back to 100
• On line 531, change document.querySelectorAll(".mover") to document.getElementsByClassName("mover").
• From line 532 to line 541, revised the code based on the first reviewer. 
• On line 561, change document.querySelector("#movingPizzas1") to document.getElementById("movingPizzas1")
• On line 562, change the number to 24

### Changes in the 2nd commit to file 'index.html'
• Inlined the content in css/style.css and removed <link href="css/style.css" rel="stylesheet">

### Changes in the 2nd commit to file 'Views/pizza.html'
• Inlined the content in css/style.css and removed <link href="css/style.css" rel="stylesheet">

### In the 1st commit, made the following changes to file 'index.html':
• Added media="print" to the css/print link to minimize use of render blocking resources
• Added async attribute to the google analytics script
• Removed the link to google web fonts (already available in style.css)
• Optimized and resized the pizzeria.jpg for the index.html to pizzeria_small.png
• Removed the links to the three small images and used the images saved in 'img' folder
• Moved Google Analytics out of the head and put it at the bottom

### In the 1st commit, made the following changes to file 'css/style.css'
• Added will-change property to html element
• Took the mobile media query out of the style.css and have it in the new file style-mobile.css

### In the 1st commit, changes to file 'Views/js/main.js'
• Took document.querySelector("#pizzaSize") out from function changeSliderLabel(size) and assign it to variable 'pizzaSz'
• Took document.querySelectorAll(".randomPizzaContainer") out from function changePizzaSizes(size) and assign it to variable 'randomPizza'
• Changed image 'pizzeria.jpg' to be 'pizzeria.png'
• Moved pizzasDiv = document.getElementById("randomPizzas") out of the for loop.
• Reduced the pizzas generated when the page loads from 100 to 20.
• Reduced the floating pizzas from 200 to 20.
• Added requestAnimationFrame to updatePositions() in a couple of places.
• Added requestAnimationFrame to changeSliderLabel(size).

### In the 1st commit, changes to file 'Views/css/style.css'
• Added will-change property to .mover element.
• Added will-change property to the html element.

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

To get started, check out the repository, inspect the code,

### Getting started

####Part 1: Optimize PageSpeed Insights score for index.html

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok http 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

####Part 2: Optimize Frames per Second in pizza.html

To optimize views/pizza.html, you will need to modify views/js/main.js until your frames per second rate is 60 fps or higher. You will find instructive comments in main.js. 

You might find the FPS Counter/HUD Display useful in Chrome developer tools described here: [Chrome Dev Tools tips-and-tricks](https://developer.chrome.com/devtools/docs/tips-and-tricks).

### Optimization Tips and Tricks
* [Optimizing Performance](https://developers.google.com/web/fundamentals/performance/ "web performance")
* [Analyzing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/analyzing-crp.html "analyzing crp")
* [Optimizing the Critical Rendering Path](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path.html "optimize the crp!")
* [Avoiding Rendering Blocking CSS](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css.html "render blocking css")
* [Optimizing JavaScript](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript.html "javascript")
* [Measuring with Navigation Timing](https://developers.google.com/web/fundamentals/performance/critical-rendering-path/measure-crp.html "nav timing api"). We didn't cover the Navigation Timing API in the first two lessons but it's an incredibly useful tool for automated page profiling. I highly recommend reading.
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/eliminate-downloads.html">The fewer the downloads, the better</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer.html">Reduce the size of text</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/image-optimization.html">Optimize images</a>
* <a href="https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching.html">HTTP caching</a>

### Customization with Bootstrap
The portfolio was built on Twitter's <a href="http://getbootstrap.com/">Bootstrap</a> framework. All custom styles are in `dist/css/portfolio.css` in the portfolio repo.

* <a href="http://getbootstrap.com/css/">Bootstrap's CSS Classes</a>
* <a href="http://getbootstrap.com/components/">Bootstrap's Components</a>

### Sample Portfolios

Feeling uninspired by the portfolio? Here's a list of cool portfolios I found after a few minutes of Googling.

* <a href="http://www.reddit.com/r/webdev/comments/280qkr/would_anybody_like_to_post_their_portfolio_site/">A great discussion about portfolios on reddit</a>
* <a href="http://ianlunn.co.uk/">http://ianlunn.co.uk/</a>
* <a href="http://www.adhamdannaway.com/portfolio">http://www.adhamdannaway.com/portfolio</a>
* <a href="http://www.timboelaars.nl/">http://www.timboelaars.nl/</a>
* <a href="http://futoryan.prosite.com/">http://futoryan.prosite.com/</a>
* <a href="http://playonpixels.prosite.com/21591/projects">http://playonpixels.prosite.com/21591/projects</a>
* <a href="http://colintrenter.prosite.com/">http://colintrenter.prosite.com/</a>
* <a href="http://calebmorris.prosite.com/">http://calebmorris.prosite.com/</a>
* <a href="http://www.cullywright.com/">http://www.cullywright.com/</a>
* <a href="http://yourjustlucky.com/">http://yourjustlucky.com/</a>
* <a href="http://nicoledominguez.com/portfolio/">http://nicoledominguez.com/portfolio/</a>
* <a href="http://www.roxannecook.com/">http://www.roxannecook.com/</a>
* <a href="http://www.84colors.com/portfolio.html">http://www.84colors.com/portfolio.html</a>
