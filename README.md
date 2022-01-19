# How to use SVG
Explanation about how SVG can be used in an page

## SVG as image
SVG can be used in an HTML page with the ``` <img/> ``` tag.
```
<img src="./img/alarm_clock.svg" alt="Clock">
```
### Advantages and disadvantages of the SVG as ``` <img/> ```
* They can be cached :)
* No interation with CSS :(
* No interation at DOM :(
* Animations only work if they're in the SVG file (don't work if we would make then with JS, for example) :(

## SVG as background
SVG also can be used as background image in any HTML element

### Advantages and disadvantages of the SVG as ``` background-image ```
* Can be cached :)
* No CSS interation :(
* No DOM interation :(
* Animations only works if they're inside of the SVG file.
* Comparing with the previous case, it has a little advantage that we can select the src in the CSS HTML selector so it doesn't have to load the image if the HTML element doesn't have the specific class.