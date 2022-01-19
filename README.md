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
```
  <style>
    .icon-music{
      background-image: url('./img/audio_file.svg')
    }
  </style>
```
### Advantages and disadvantages of the SVG as ``` background-image ```
* Can be cached :)
* No CSS interation :(
* No DOM interation :(
* Animations only works if they're inside of the SVG file :(
* Comparing with the previous case, it has a little advantage that we can select the src in the CSS HTML selector so it doesn't have to load the image if the HTML element doesn't have the specific class :)

## SVG as iframe/object/embed
```
<iframe src="./../assets/img/alarm_clock.svg" frameborder="0"></iframe>
```
```
<object data="./../assets/img/alarm_clock.svg" type=""></object>
```
```
<embed src="./../assets/img/alarm_clock.svg" type="">
```

### Advantages and disadvantages of the SVG as ``` <iframe/> / <object/> /<embed/>```
* Slow rendering :(
* Differents behaviors depending on the browser :(
* Don't allow so many editions :(

## SVG as data-uri
In that case, whe can use both as image or as background-image

### SVG as data-uri in ``` background-image ```
```
<style>
    .icon-clock{
      height: 100px;
      width: 100px;
      background-image: url(data:image/svg+xml;base64,PHN2ZyB2ZXJzaW9uPSIxIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA0OCA0OCIgZW5hYmxlLWJhY2tncm91bmQ9Im5ldyAwIDAgNDggNDgiPgogICAgPGcgZmlsbD0iIzM3NDc0RiI+CiAgICAgICAgPHBhdGggZD0iTTM4LjUsNDQuNmwtNC00bDIuMS0yLjFsNCw0YzAuNiwwLjYsMC42LDEuNSwwLDIuMWwwLDBDNDAuMSw0NS4xLDM5LjEsNDUuMSwzOC41LDQ0LjZ6Ii);
    }
  </style>
``` 
### SVG as data-uri in ```` <img/> ````
```
<img src="data:image/svg+xml;base64,PHN2ZyB2ZXJzaW9uPSIxIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA0OCA0OCIgZW5hYmxlLWJhY2tncm91bmQ9Im5ldyAwIDAgNDggNDgiPgogICAgPGcgZmlsbD0iIzM3NDc0RiI+CiAgICAgICAgPHBhdGggZD0iTTM4LjUsNDQuNmwtNC00bDIuMS0yLjFsNCw0YzAuNiwwLjYsMC42LDEuNSwwLDIuMWwwLDBDNDAuMSw0NS4xLDM5LjEsNDUuMSwzOC41LDQ0LjZ6Ii" alt="Clock"/>
```

### Advantages and disadvantages of the SVG as ``` data-uri ``` 
* They're not cached :(
* No CSS interaction :(
* No DOM interaction :(
* The size of the data-uri sometimes can be bigger than the SVG code :(