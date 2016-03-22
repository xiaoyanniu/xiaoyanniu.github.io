# Changes to file 'js/main.js'
1. Took document.querySelector("#pizzaSize") out from function changeSliderLabel(size) and assign it to variable 'pizzaSz'
2. Took document.querySelectorAll(".randomPizzaContainer") out from function changePizzaSizes(size) and assign it to variable 'randomPizza'
3. Changed image 'pizzeria.jpg' to be 'pizzeria.png'
4. Moved pizzasDiv = document.getElementById("randomPizzas") out of the for loop.
5. Reduced the pizzas generated when the page loads from 100 to 20.
6. Reduced the floating pizzas from 200 to 20.
7. Added requestAnimationFrame to updatePositions() in a couple of places.
8. Added requestAnimationFrame to changeSliderLabel(size).


# Changes to file 'Views/css/style.css'
1. Added will-change property to .mover element.
2. Added will-change property to the html element.